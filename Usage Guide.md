# 🗒️ Reference Set CSS
The Reference Set CSS snippet was designed to make creating and modifying Alternative Checkboxes as simple as possible. The code is divided into 2 sections:
- **Section 1:** Definining each Alternative Checkbox with simple selectors and a set of CSS Variables.
- **Section 2:** The following code should remain untouched. It serves as a template for checkbox definitions above. It leaves the default unchecked and checked checkboxes untouched; those are styled according to the theme used.

# ✅ Supported themes
The Reference Set CSS will work with:
- The default Obsidian theme.
- Themes with Style Settings that have implemented a Style Settings toggle for their Alternative Checkboxes implementation.
  - Theme support is documented here: [08 Style Settings Toggle Review.md](https://github.com/damiankorcz/Alternative-Checkboxes-Reference-Set/blob/main/Research%20Vault/08%20Style%20Settings%20Toggle%20Review.md).
- Themes without Style Settings which have implemented the `@container style()` query surrounding their Alternative Checkboxes implementation; effectively working like a toggle which can be overwritten from the CSS snippet.
  - Theme support is documented here: [09 @container Style Queries Toggle Review.md](https://github.com/damiankorcz/Alternative-Checkboxes-Reference-Set/blob/main/Research%20Vault/09%20%40container%20Style%20Queries%20Toggle%20Review.md).
- Potentially, any theme that doesn't have it's own Alternative Checkboxes implementation; this will depend on how much the theme alters the checkboxes.

# 🤔 How do I use it in my vault?
Make sure you are using one of the supported themes mentioned above.

For themes with Style Settings, make sure to refer to the documentation ([08 Style Settings Toggle Review.md](https://github.com/damiankorcz/Alternative-Checkboxes-Reference-Set/blob/main/Research%20Vault/08%20Style%20Settings%20Toggle%20Review.md)) on which Style Setting options need to be toggled (opposite of default). This is essential to reset the theme; it will remove any built-in Alternative Checkbox implementation / checkbox customisation which would interfere with the snippet.

Now, simply download the `Alternative Checkbox Reference Set.css` from the [Releases](https://github.com/damiankorcz/Alternative-Checkboxes-Reference-Set/releases) and put it inside your vault in the following path:  
`*Your vault name*/.obsidian/snippets`.

Make sure to open your vault in Obsidian and enable the newly added snippet:
1. Go to Settings.
2. Click on the Appearance tab.
3. Scroll down to CSS Snippets and click the refresh icon if you don't see the snippet in the list.
4. Toggle the snippet to enable it. 

# 🌟 Creating a Custom Alternative Checkbox Sets based on the Reference Set

The Reference Set CSS was designed to make creating and modifying Alternative Checkboxes as simple as possible. All you need to keep from the Reference Set CSS for your new set to function correctly, is the following comment and all code below it:
```css
/*  --------------------------------------------------------------------------------------------
    Section 2
    The following code should remain untouched. It serves as a template for checkbox definitions
    above. It leaves the default unchecked and checked checkboxes untouched; those are styled 
    according to the theme used.
*/
```

**Note that if there are future updates to the Reference Set (e.g. something breaks due to Obsidian updating), you will have to copy this section again into your snippet from the new version release of the Reference Set.**

## Alternative Checkbox setup breakdown
The individual Alternative Checkbox setup is obscured behing simple variables, which utility is described in this section. By default, all options mentioned below come with default values set to them, meaining you don't have to define each one for every single Alternative Checkbox. Only the ones you want to change.  
***Customisation examples in the next section***


As in the Reference Set CSS, you want to add all of your Alternative Checkbox code above the comment mentioned above (so in Section 1). In case a future update is required keeping a clear separation of the setup code and Alternative Checkbox code will make it easier to maintain.

---

```css
div.HyperMD-task-line[data-task="/"]
```
 Used to inject the variables for the specific checkbox in Live Preview. Change the character in between the quotes to the character you want to use for your checkbox. Certain symbols need to be escaped to work correctly e.g. `[data-task="\""]` for a `- ["] Quote` checkbox.

---

```css
ul > li[data-task="/"]
```
 Used to inject the variables for the specific checkbox in Reading Mode. Change the character in between the quotes to the character you want to use for your checkbox. Certain symbols need to be escaped to work correctly e.g. `[data-task="\""]` for a `- ["] Quote` checkbox.

---

```css
--icon-mask-image: url("data:image/svg+xml;base64,PHN2Z...");
```
Used to specify the Base64 embedded icon. The Reference Set makes use of the [Lucide](https://lucide.dev/) icon set (same icon set as the Obsidian UI). You can use other Base64 embedded SVG icons here. For converting other SVG icons, you can use this: https://yoksel.github.io/url-encoder/

The `mask` portion of the variable refers to the CSS method used to replace the icon.
**CSS Reference:** https://developer.mozilla.org/en-US/docs/Web/CSS/mask-image

---

```css
--icon-mask-color: var(--text-normal);
```
Used to change the icon color when using the Base64 embedded icon. In this case, it's utilising a color variable from the default Obsidian theme to match the text color. You can change this to any valid CSS color type, a color variable within your theme or the default Obsidian theme.  

**CSS Reference:** https://developer.mozilla.org/en-US/docs/Web/CSS/color

---

```css
--icon-content: "/";
```
Used to define content displayed instead of the Base64 embedded icon. In this case, it can be text, symbol and/or Emoji. Note that you are constrained to the size of the checkbox container so realistically you can do 1 Emoji or maybe 2 characters / symbols before things flow over to the next line.  
**CSS Reference:** https://developer.mozilla.org/en-US/docs/Web/CSS/content

---

```css
--icon-content-font: var(--font-monospace);
```
Used to set the font family for the icon content. You can change this to any valid CSS font family, a font family variable within your theme / the default Obsidian theme.  
**CSS Reference:** https://developer.mozilla.org/en-US/docs/Web/CSS/font-family

---

```css
--icon-content-weight: var(--font-bold);
```
Used to set the font weight for the icon content. You can change this to any valid CSS weight type or a weight variable within your theme / the default Obsidian theme.  
**CSS Reference:** https://developer.mozilla.org/en-US/docs/Web/CSS/@font-face/font-weight

---

```css
--icon-content-color: var(--text-normal);
```
Used to change the icon color when using text / symbols as the icon. In this case, it's utilising a color variable from the default Obsidian theme to match the text color. You can change this to any valid CSS color type, a color variable within your theme or the default Obsidian theme.  
**CSS Reference:** https://developer.mozilla.org/en-US/docs/Web/CSS/color

---

```css
--icon-background: transparent;
```
Used to change the background behind the icon.  
**CSS Reference:** https://developer.mozilla.org/en-US/docs/Web/CSS/background

---

```css
--icon-background-hover: transparent;
```
Used to change the background behind the icon when hovering over it.  
**CSS Reference:** https://developer.mozilla.org/en-US/docs/Web/CSS/background

---

```css
--icon-border: unset;
```
Used to change the border properties (width, style and color) of the icon container.  
**CSS Reference:** https://developer.mozilla.org/en-US/docs/Web/CSS/border

---

```css
--icon-border-radius: unset;
```
Used to change the border radius of the icon container.  
**CSS Reference:** https://developer.mozilla.org/en-US/docs/Web/CSS/border-radius

---

```css
--line-text-color: inherit;
```
Used to change the color of the text after the checkbox icon / content.  
**CSS Reference:** https://developer.mozilla.org/en-US/docs/Web/CSS/color

---

```css
--line-background: unset;
```
Used to change the background for the line that the checkbox is on.  
**CSS Reference:** https://developer.mozilla.org/en-US/docs/Web/CSS/background

---

```css
--line-border: unset;
```
Used to change the border properties (width, style and color) of the line that the checkbox is on.  
**CSS Reference:** https://developer.mozilla.org/en-US/docs/Web/CSS/border

---

```css
--line-border-radius: unset;
```
Used to change the border radius of the line that the checkbox is on.  
**CSS Reference:** https://developer.mozilla.org/en-US/docs/Web/CSS/border-radius


## ⚙️ Customisation Examples

WIP

# 🧰 Improve theme support for snippets based on the Reference Set

Implementing an option to toggle your theme's implementation of Alternative Checkboxes, allows users to use their own implementation with ease and prevents users from being locked to your theme's features. Here is how you can make this possible regardless if your theme uses the Style Settings plugin or not.

## Theme uses the Style Settings plugin

You can prefix your existing selectors related to the Alternative Checkboxes with the following class:

```css
body.enable-alternative-checkboxes ...
```

**OR**

Nest all of them within the brackets:

```css
body.enable-alternative-checkboxes {
  /* Enclose all code relevant to Altenative Checkboxes here */
}
```

Add a toggle option in the Style Settings code:

```yaml
-
    id: enable-alternative-checkboxes
    title: Enable Alternative Checkboxes
    description: Disable this if you are using your own implementation via a CSS Snippet.
    default: true
    type: class-toggle
-
```

The Style Settings toggle will allow users to disable your implementation (effectively resetting the styling to match the default checked checkbox) and use their own CSS snippet. By default, the Style Settings code is set to enabled to assure the functionality remains unchanged for existing users of your theme.

## Theme doesn't use the Style Settings plugin

Implementing the following code allows the Reference Set CSS to disable your Alternative Checkboxes implementation with a simple change to the `--theme-alternative-checkboxes` variable.

```css
body {
  --theme-alternative-checkboxes: enable;
}

@container style(--theme-alternative-checkboxes: enable) {
  /* Enclose all code relevant to Altenative Checkboxes here */
}
```

For the `@container style()` query to function, you and your users need to be using an updated Obsidian Installer version (within last 12 months should be fine). Installer version means downloading the Obsidian app again and running the installer which will update the Installer version (effectively updating the Electron version used among other dependancies). **Note that the In-app updates and Installer updates are not the same!**

Specifically for mobile Apple devices, you and your users will need [iOS 18](https://support.apple.com/en-gb/guide/iphone/iphe3fa5df43/ios) / [iPadOS 18](https://support.apple.com/en-gb/guide/ipad/ipad213a25b2/ipados) or newer, since this feature is available starting with Safari 18 (Safari versions typically match the OS versions on Apple devices).

**If you use this method, make sure to communicate the last two paragraphs to your users to prevent any confusion!**

Further information about the browser engine compatibility for this feature can be checked here:  
https://caniuse.com/mdn-css_at-rules_container_style_queries_for_custom_properties