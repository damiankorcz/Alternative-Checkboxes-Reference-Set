# ⚠️ This is not final. Very much WIP. Don't rely on this yet

The Reference Set CSS will work with:
- The default Obsidian theme.
- Themes with Style Settings that have implemented a Style Settings toggle for their Alternative Checkboxes implementation (Progress on that documented here: [[09 Style Settings Toggle Review]]).
- Themes without Style Settings which have implemented the `@container style()` query surrounding their Alternative Checkboxes implementation; effectively working like a toggle which can be overwritten from the CSS snippet. (Progress on that documented here: [[10 @container Style Queries Toggle Review]]).
- Potentially, any theme that doesn't have it's own Alternative Checkboxes implementation (this will depend on how much the theme alters the checkboxes).
# 🧰 Improve Support for Using Other Alternative Checkbox Sets

Implementing an option to toggle your theme's implementation of Alternative Checkboxes allows users to use their own implementation with ease and promotes. Here is how you can make this possible regardless if your theme uses the Style Settings plugin or not.

## Theme uses the Style Settings plugin

You can prefix your existing selectors related to the Alternative Checkboxes with the following or nest all of them within the brackets.

```css
body.enable-alternative-checkboxes {

/* Encapsulate all code relevant to Altenative Checkboxes here */

}
```

Add a toggle in the Style Settings code:

```yaml
-
    id: enable-alternative-checkboxes
    title: Enable Alternative Checkboxes
    description: Disable this if you are using your own implementation via a CSS Snippet.
    default: true
    type: class-toggle
-
```

The Style Settings toggle will allow users to disable your implementation (effectively resetting the styling to match the default checked checkbox) and use their own CSS snippet. By default, it's set to enabled to assure the functionality remains unchanged for existing users of your theme.
## Theme doesn't use the Style Settings plugin

This option allows the Reference Set CSS to disable your Alternative Checkboxes implementation with a simple change to the `--theme-alternative-checkboxes` variable.

```css
body {
  --theme-alternative-checkboxes: enable;
}

@container style(--theme-alternative-checkboxes: enable) {
  /* all the code for the checkboxes */
}
```

For the `@container style()` query to function you'd require...

# 🌟 Creating Custom Alternative Checkbox Sets Based on the Reference Set


## Alternative Checkbox Setup Breakdown
Here is how one Alternative Checkbox from the Reference Set CSS is defined:
```css
/* - [/] Incomplete */
div.HyperMD-task-line[data-task="/"],
ul >li[data-task="/"] {
	--icon-method: mask;
	    
    --icon-mask-position: center;
    --icon-mask-size: contain;
    
    /* Icon used: https://lucide.dev/icons/square-dashed */
    --icon-mask-image: url("data:image/svg+xml;base64,PHN2Z...");
    
    --icon-content: "/";
    --icon-content-weight: var(--font-bold);
    --icon-content-font: var(--font-monospace);
    --icon-content-alignment: center;
    
    --icon-color: var(--text-normal);
    --icon-background-color: transparent;
    --icon-background-color-hover: transparent;
    --icon-border: unset;
	--icon-border-radius: unset;
	
	--line-text-color: inherit;
	--line-background-color: unset;
	--line-border: unset;
	--line-border-radius: unset;
}
```
**This example includes all available variables. You don't need to include all of them per checkbox since there are defaults set in the Reference Set CSS. Only include the ones you want to overwrite e.g. change the icon with the `--icon-mask-image` variable.**

## Breakdown
Each line has a specific function:

```css
div.HyperMD-task-line[data-task="/"]
```
 Used to inject the variables for the specific checkbox in Live Preview. Change the character in between the quotes to the character you want to use for your checkbox. Certain symbols need to be escaped to work correctly e.g. `[data-task="\""]` for a `- ["] Quote` checkbox.


```css
ul > li[data-task="/"]
```
 Used to inject the variables for the specific checkbox in Reading Mode. Change the character in between the quotes to the character you want to use for your checkbox. Certain symbols need to be escaped to work correctly e.g. `[data-task="\""]` for a `- ["] Quote` checkbox.


```css
--icon-method: mask;
```
Used to set which icon setup is used. There are 2 options: 
- `mask` allows you to use a Base64 embedded icon.
- `content` allows you to use text, symbols and / or emoji instead of the icon.


```css
--icon-mask-position: center;
```
Only used when `--icon-method: mask;` is set; it's the default option. Used to align the icon (horizontally and vertically) within the checkbox container.
**CSS Reference:** https://developer.mozilla.org/en-US/docs/Web/CSS/mask-position


```css
--icon-mask-size: contain;
```
Only used when `--icon-method: mask;` is set; it's the default option. Used to change the size of icon within the checkbox container.
**CSS Reference:** https://developer.mozilla.org/en-US/docs/Web/CSS/mask-size


```css
--icon-mask-image: url("data:image/svg+xml;base64,PHN2Z...");
```
Only used when `--icon-method: mask;` is set; it's the default option. Used to input the Base64 embedded icon.
**CSS Reference:** https://developer.mozilla.org/en-US/docs/Web/CSS/mask-image


```css
--icon-content: "/";
```
Only used when `--icon-method: content;` is set. Used to define content displayed instead of the Base64 embedded icon. In this case, it can be text, symbol and/or Emoji.
**CSS Reference:** https://developer.mozilla.org/en-US/docs/Web/CSS/content


```css
--icon-content-weight: var(--font-bold);
```
Only used when `--icon-method: content;` is set. Used to set the font weight for the content. You can change this to any valid CSS weight type, a weight variable within your theme or the default Obsidian theme.
**CSS Reference:** https://developer.mozilla.org/en-US/docs/Web/CSS/@font-face/font-weight


```css
--icon-content-font: var(--font-monospace);
```
Only used when `--icon-method: content;` is set. Used to set the font family for the content. You can change this to any valid CSS font family, a font family variable within your theme or the default Obsidian theme.
**CSS Reference:** https://developer.mozilla.org/en-US/docs/Web/CSS/font-family


```css
--icon-content-alignment: center;
```
Only used when `--icon-method: content;` is set. Used to change the horizontal alignment of the content.
**CSS Reference:** https://developer.mozilla.org/en-US/docs/Web/CSS/text-align


```css
--icon-color: var(--text-normal);
```
Used to change the icon color. In this case, it's utilising a color variable from the default Obsidian theme to match the text color. You can change this to any valid CSS color type, a color variable within your theme or the default Obsidian theme.
**CSS Reference:** https://developer.mozilla.org/en-US/docs/Web/CSS/color


```css
--icon-background-color: transparent;
```
Used to change the background color behind the icon. 
**CSS Reference:** https://developer.mozilla.org/en-US/docs/Web/CSS/color


```css
--icon-background-color-hover: transparent;
```
Used to change the background color behind the icon when hovering over it. 
**CSS Reference:** https://developer.mozilla.org/en-US/docs/Web/CSS/color


```css
--icon-border: unset;
```
Used to change the border properties (width, style and color) of the icon container. 
**CSS Reference:** https://developer.mozilla.org/en-US/docs/Web/CSS/border


```css
--icon-border-radius: unset;
```
Used to change the border radius of the icon container. 
**CSS Reference:** https://developer.mozilla.org/en-US/docs/Web/CSS/border-radius


```css
--line-text-color: inherit;
```
Used to change the color of the text after the checkbox icon / content.
**CSS Reference:** https://developer.mozilla.org/en-US/docs/Web/CSS/color


```css
--line-background-color: unset;
```
Used to change the color of the background for the line that the checkbox is on.
**CSS Reference:** https://developer.mozilla.org/en-US/docs/Web/CSS/color


```css
--line-border: unset;
```
Used to change the border properties (width, style and color) of the line that the checkbox is on.
**CSS Reference:** https://developer.mozilla.org/en-US/docs/Web/CSS/border


```css
--line-border-radius: unset;
```
Used to change the border radius of the line that the checkbox is on.
**CSS Reference:** https://developer.mozilla.org/en-US/docs/Web/CSS/border-radius
