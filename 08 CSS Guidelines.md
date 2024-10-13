# ⚠️ This is not final. Very much WIP. Don't rely on this yet

Target with DevTools to see CSS directly

- [ ] Unticked
- [x] Ticked 

---
# Obsidian Default Theme CSS (1.7.4)
The following code has been taken directly from the `main.css` file within Obsidian. Please respect the licenses under which Obsidian is distributed when referencing. Used here with approval. Obsidian License: https://obsidian.md/license

```css

.theme-light {
	/* Variables used for the in other code */
	--color-base-00: #ffffff;
	--color-base-50: #ababab;
	--color-base-70: #5c5c5c;
	
	--color-accent-1: hsl(calc(var(--accent-h) - 1), calc(var(--accent-s) * 1.01), calc(var(--accent-l) * 1.075));
	--color-accent-2: hsl(calc(var(--accent-h) - 3), calc(var(--accent-s) * 1.02), calc(var(--accent-l) * 1.15));
}

.theme-dark {
	/* Variables used for the in other code */
	--interactive-accent: var(--color-accent);
	--interactive-accent-hover: var(--color-accent-1);

	--color-accent-1: hsl(calc(var(--accent-h) - 3), calc(var(--accent-s) * 1.02), calc(var(--accent-l) * 1.15));
	--color-accent-2: hsl(calc(var(--accent-h) - 5), calc(var(--accent-s) * 1.05), calc(var(--accent-l) * 1.29));
}

body {
	/* Variables used for the in other code */
	--accent-h: 258;
	--accent-s: 88%;
	--accent-l: 66%;
	--radius-s: 4px;
	--font-text-size: 16px;
	--background-primary: var(--color-base-00);
	--interactive-accent: var(--color-accent-1);
	--interactive-accent-hover: var(--color-accent-2);
	--text-faint: var(--color-base-50);
	--text-muted: var(--color-base-70);

	/* Checkboxes */
	--checkbox-radius: var(--radius-s);
	--checkbox-size: var(--font-text-size);
	--checkbox-marker-color: var(--background-primary);
	--checkbox-color: var(--interactive-accent);
	--checkbox-color-hover: var(--interactive-accent-hover);
	--checkbox-border-color: var(--text-faint);
	--checkbox-border-color-hover: var(--text-muted);
	--checkbox-margin-inline-start: 0.85em;
	--checklist-done-decoration: line-through;
	--checklist-done-color: var(--text-muted);
}

.is-mobile {
	--checkbox-size: 17px;
}

input[type=checkbox] {
	-webkit-appearance: none;
	appearance: none;
	border-radius: var(--checkbox-radius);
	border: 1px solid var(--checkbox-border-color);
	flex-shrink: 0;
	padding: 0;
	margin: 0;
	margin-inline-end: 6px;
	width: var(--checkbox-size);
	height: var(--checkbox-size);
	position: relative;
	transition: box-shadow 0.15s ease-in-out;
}

input[type=checkbox]:hover,
input[type=checkbox]:active,
input[type=checkbox]:focus {
	outline: 0;
	border-color: var(--checkbox-border-color-hover);
}

input[type=checkbox]:focus-visible {
	box-shadow: 0 0 0 2px var(--background-modifier-border-focus);
}

input[type=checkbox]:checked:after {
	content: "";
	top: -1px;
	inset-inline-start: -1px;
	position: absolute;
	width: var(--checkbox-size);
	height: var(--checkbox-size);
	display: block;
	background-color: var(--checkbox-marker-color);
	-webkit-mask-position: 52% 52%;
	-webkit-mask-size: 65%;
	-webkit-mask-repeat: no-repeat;
	-webkit-mask-image: url('data:image/svg+xml; utf8, <svg width="12px" height="10px" viewBox="0 0 12 8" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"><g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd"><g transform="translate(-4.000000, -6.000000)" fill="%23000000"><path d="M8.1043257,14.0367999 L4.52468714,10.5420499 C4.32525014,10.3497722 4.32525014,10.0368095 4.52468714,9.8424863 L5.24777413,9.1439454 C5.44721114,8.95166768 5.77142411,8.95166768 5.97086112,9.1439454 L8.46638057,11.5903727 L14.0291389,6.1442083 C14.2285759,5.95193057 14.5527889,5.95193057 14.7522259,6.1442083 L15.4753129,6.84377194 C15.6747499,7.03604967 15.6747499,7.35003511 15.4753129,7.54129009 L8.82741268,14.0367999 C8.62797568,14.2290777 8.3037627,14.2290777 8.1043257,14.0367999"></path></g></g></svg>');
}

input[type=checkbox]:checked {
	background-color: var(--checkbox-color);
	border-color: var(--checkbox-color);
}

@media (hover: hover) {
	input[type=checkbox]:checked:hover {
		background-color: var(--checkbox-color-hover);
		border-color: var(--checkbox-color-hover);
	}
}

input[type=checkbox][data-indeterminate="true"]:not(:checked):after {
	content: "";
	position: absolute;
	top: calc(var(--checkbox-size)/2 - 2px);
	width: calc(var(--checkbox-size) - 6px);
	left: 0;
	right: 0;
	margin: 0 auto;
	height: 2px;
	display: block;
	border-radius: 2px;
	background-color: var(--text-normal);
}

.task-list-item-checkbox {
	width: var(--checkbox-size);
	height: var(--checkbox-size);
}

ul > li.task-list-item .task-list-item-checkbox {
	margin-inline-start: calc(var(--checkbox-size) * -1.5);
}

ul > li.task-list-item[data-task="x"],
ul > li.task-list-item[data-task="X"] {
	text-decoration: var(--checklist-done-decoration);
	color: var(--checklist-done-color);
}

.markdown-source-view.mod-cm6 .HyperMD-task-line[data-task="x"],
.markdown-source-view.mod-cm6 .HyperMD-task-line[data-task="X"] {
	text-decoration: var(--checklist-done-decoration);
	color: var(--checklist-done-color);
}
```