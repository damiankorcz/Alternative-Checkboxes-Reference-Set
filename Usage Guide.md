# ⚠️ This is not final. Very much WIP. Don't rely on this yet

The Reference Set CSS will work with:
- The default Obsidian theme.
- Themes with Style Settings that have implemented a Style Settings toggle for their Alternative Checkboxes implementation (Progress on that documented here: [[09 Style Settings Toggle Review]]).
- Themes without Style Settings which have implemented the `@container style()` query surrounding their Alternative Checkboxes implementation; effectively working like a toggle which can be overwritten from the CSS snippet.
- Potentially, any theme that doesn't have it's own Alternative Checkboxes implementation (this will depend on how much the theme alters the checkboxes).

## Example Alternative Checkbox and Breakdown
Here is how one Alternative Checkbox from the Reference Set CSS is defined:
```css
/* - [/] Incomplete */
div.HyperMD-task-line[data-task="/"],
ul >li[data-task="/"] {
    --icon-color: var(--text-normal);
    --icon-background-color: transparent;
    --icon-background-color-hover: transparent;
    
    --icon-method: mask;
    
    --icon-mask-position: center;
    --icon-mask-size: contain;
    
    /* Icon used: https://lucide.dev/icons/square-dashed */
    --icon-mask-image: url("data:image/svg+xml;base64,PHN2Z...");
    
    --icon-content: "/";
    --icon-content-weight: var(--font-bold);
    --icon-content-font: var(--font-monospace);
	
	--checkbox-border: unset;
	--checkbox-border-radius: unset;
}
```
**This example includes all available variables. You don't need to include all of them per checkbox since there are defaults set in the Reference Set CSS. Only include the ones you want to overwrite e.g. change the icon with the `--icon-mask-image` variable.**

### Breakdown
Each line has a specific function:

```css
div.HyperMD-task-line[data-task="/"]
```
 Used to inject the variables for the specific checkbox in Live Preview.

```css
ul > li[data-task="/"]
```
 Used to inject the variables for the specific checkbox in Reading Mode.

```css
--icon-color: var(--text-normal);
```
Used to change the icon color. In this case it's utilising a color variable from the default Obsidian theme to match the text color. You can change this to any valid CSS color type, a color variable within your theme or the default Obsidian theme.

```css
--icon-background-color: transparent;
```
t

```css
--icon-background-color-hover: transparent;
```
t

```css
--icon-method: mask;
```
Used to set between 2 options for setting an icon. 
- `mask` allows you to use a Base64 embedded icon.
- `content` allows you to use text and / or emoji to serve instead of the icon.

```css
--icon-mask-position: center;
```
Only used when `--icon-method: mask;`. 

```css
--icon-mask-size: contain;
```
Only used when `--icon-method: mask;`. 

```css
--icon-mask-image: url("data:image/svg+xml;base64,PHN2Z...");
```
Only used when `--icon-method: mask;`. Used to input the Base64 embedded icon.

```css
--icon-content: "/";
```
Only used when `--icon-method: content;`. Used to define content displayed instead of a Base64 embedded icon. In this case it can be text, symbol or Emoji.

```css
--icon-content-weight: var(--font-bold);
```
Only used when `--icon-method: content;`. Used to set the font weight for the content. You can change this to any valid CSS weight type, a weight variable within your theme or the default Obsidian theme.

```css
--icon-content-font: var(--font-monospace);
```
Only used when `--icon-method: content;`. Used to set the font type for the content. You can change this to any valid CSS font type, a font type variable within your theme or the default Obsidian theme.

```css
--checkbox-border: unset;
```
t

```css
--checkbox-border-radius: unset;
```
t

# How to improve support for this in your theme?

Implementing an option to toggle your theme's implementation of Alternative Checkboxes allows users to use their own with ease. Here is how you can make this possible regardless if your theme uses the Style Settings plugin or not.

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