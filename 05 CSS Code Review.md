# Minimal

Distributed under the [MIT License](https://github.com/kepano/obsidian-minimal/blob/master/LICENSE)

## With mask image

- [>] Forwarded `- [>]`
- [<] Scheduling `- [<]`
- [!] Important `- [!]`
- [-] Cancelled `- [-]`
- [*] Star `- [*]`
- [l] Location `- [l]`
- [I] Idea `- [I]`
- [p] Pros `- [p]`
- [c] Cons `- [c]`
- [f] Fire `- [f]`
- [k] Key `- [k]`
- [w] Win `- [w]`
- [u] Up `- [u]`
- [d] Down `- [d]`


```css
input[data-task=">"],
li[data-task=">"] > input,
li[data-task=">"] > p > input {
	&:checked {
		--checkbox-marker-color: transparent;
		border:none;
		border-radius:0;
		background-image:none;
		background-color:currentColor;
		-webkit-mask-size:var(--checkbox-icon);
		-webkit-mask-position:50% 50%;
	}
}

input[data-task=">"],
li[data-task=">"] > input,
li[data-task=">"] > p > input, {
	&:checked {
		color:var(--text-faint);
		-webkit-mask-position:50% 100%;
		-webkit-mask-image: url("data:image/svg+xml,...");
	}
}
```

## With background image

- [?] Question `- [?]`
- ["] Quote `- ["]`
- [i] Information `- [i]`
- [S] Savings `- [S]`


```css
input[data-task="?"],
li[data-task="?"] > input,
li[data-task="?"] > p > input, {
	&:checked {
		--checkbox-marker-color: transparent;
		background-color:var(--color-yellow);
		border-color:var(--color-yellow);
		background-position:50% 50%;
		background-size:200% 90%;
		background-image: url('data:image/svg+xml,...');
	}
	.theme-dark & {
		&:checked {
			background-image: url('data:image/svg+xml,...');
		}
	}
}
```

## Other method(s)

- [/] Incomplete `- [/]`

```css
input[data-task="/"],
li[data-task="/"] > input,
li[data-task="/"] > p > input, {
	&:checked {
		background-image:none;
		background-color:transparent;
		position:relative;
		overflow:hidden;
		&:after {
			top: 0;
			left: 0;
			content:" ";
			display:block;
			position:absolute;
			background-color:var(--background-modifier-accent);
			width:calc(50% - 0.5px);
			height:100%;
			-webkit-mask-image: none;
		}
	}
}
```

# Things

Distributed under the [MIT License](https://github.com/colineckert/obsidian-things/blob/main/LICENSE)

From [[#Minimal]]

# Blue Topaz

Distributed under the [MIT License](https://github.com/PKM-er/Blue-Topaz_Obsidian-css/blob/master/LICENSE)

## Default checkboxes

### With background images
- [>] Rescheduled `- [>]`
- [<] Scheduled `- [<]`
- [?] Question `- [?]`
- [!] Important `- [!]`
- [+] Plus `- [+]`
- [-] Cancelled `- [-]`
- ["] Quote`- ["]`
- [S] Amount `- [S]`
- [i] Information `- [i]`
- [u] Up `- [u]`
- [d] Down `- [d]`
- [M] Medical `- [M]`
- [t] Clock / Time `- [t]`
- [P] Person `- [P]`
- [L] Translate / Language `- [L]`
- [W] World `- [W]`
- [U] Universe `- [U]`

```css
input[data-task="“"]:checked,
li[data-task="“"] > input:checked,
li[data-task="“"] > p > input:checked {
	background-color: var(--green); /* not constant */
	background-image: url('data:image/svg+xml,...'); /* not constant */
	
	/* some might also change the following: */
    background-position: 50% 50%;
    border-color: var(--green); /* not constant */
    background-size: 75%; /* not constant */
}

.theme-dark input[data-task="“"]:checked,
.theme-dark li[data-task="“"]>input:checked,
.theme-dark li[data-task="“"]>p>input:checked {
    background-image: url('data:image/svg+xml,...')
}
```

### With mask image

- [*] Star `- [*]`
- [l] Location `- [l]`
- [n] Note `- [n]`
- [I] Idea / Light bulb `- [I]`
- [p] Pro `- [p]`
- [c] Con `- [c]`
- [b] Bookmark `- [b]`
- [f] Fire `- [f]`
- [w] Win `- [w]`
- [k] Key `- [k]`
- [r] Rule / Law `- [r]`
- [m] Measurement `- [m]`
- [T] Telephone `- [T]`
- [#] Tags `- [#]`
- [F] Feature `- [F]`

```css
input[data-task=n]:checked,
li[data-task=n] > input:checked,
li[data-task=n] > p > input:checked {
	cursor: default;
	background-position: center;
	background: none;
	background-color: var(--blue); /* not constant */
	transform: rotate(45deg); /* not constant */
	-webkit-mask-size: 120%; /* not constant */
	-webkit-mask-position: 50% 50%;
	-webkit-mask-image: url("data:image/svg+xml,...");
}
```

### Other method(s)

- [/] In Progress `- [/]`

```css
input[data-task="/"],
li[data-task="/"] > input,
li[data-task="/"] > p > input {
	border-radius: var(--ch-radius);
}
input[data-task="/"]:checked,
li[data-task="/"] > input:checked,
li[data-task="/"] > p > input:checked {
	background-image: none;
}
.theme-light input[data-task="/"]:checked,
.theme-dark input[data-task="/"]:checked,
.theme-light li[data-task="/"] > input:checked,
.theme-dark li[data-task="/"] > input:checked,
.theme-light li[data-task="/"] > p > input:checked,
.theme-dark li[data-task="/"] > p > input:checked {
	background: var(--text-faint);
}
```

## Extend checkbox list

Style Settings Required: `Blue Topaz Theme -> 2. Detail settings -> 2.3 Element styles -> 2.3.11 Checkbox -> Extend checkbox list (unavailable)`

- ["] Quote `- ["]`
- […] Ellipsis  `- […]`
- [/] In Progress `- [/]
- [.] Dot `- [.]`
- [d] Down `- [d]`
- [u] Up `- [u]`
- [A] (nothing ?) `- [A]`
- [D] Delete `- [D]`
- [￥] Coin `- [￥]`
- [$] Coin `- [$]`
- [*] Star `- [*]`

```css
body.extend-checkbox-list input[data-task="“"]:checked,
body.extend-checkbox-list li[data-task="“"]>input:checked,
body.extend-checkbox-list li[data-task="“"]>p>input:checked {
  background-color: transparent;
  background-image: url('data:image/svg+xml,...);
}
```

# AnuPpuccin

License: [GPL-3.0](https://github.com/AnubisNekhet/AnuPpuccin/blob/main/LICENSE)

## With mask image

All checkboxes, except `- [/]`

```css
.anp-custom-checkboxes [data-task="!"] {
> input[type="checkbox"]:checked,
> p > input[type="checkbox"]:checked,
	&[type="checkbox"]:checked {
		&:after {
			-webkit-mask-image: url("data:image/svg+xml,...");
			-webkit-mask-size: 20%;
		}
		&:before {
			color: var(--checkbox-color);
			margin: 0 3px;
			position: absolute;
			left: calc(var(--checkbox-size) * 1);
			font-weight: bold;
		}
		--checkbox-color: rgb(var(--ctp-yellow));
		--checkbox-color-hover: rgb(var(--ctp-yellow));
	}
}
```

## Other method(s)

- [/] In Progress `- [/]`

```css
.anp-custom-checkboxes [data-task="/"] {
> input[type="checkbox"]:checked,
> p > input[type="checkbox"]:checked,
	&[type="checkbox"]:checked {
		&:after {
			background-color: transparent;
		}
		&:before {
			color: rgb(var(--ctp-subtext0));
			margin: 0 3px;
			position: absolute;
			left: calc(var(--checkbox-size) * 1);
			font-weight: bold;
		}
		--checkbox-color: rgba(var(--ctp-subtext0), 0.3);
		--checkbox-color-hover: rgba(var(--ctp-subtext0), 0.3);
		border-color: rgb(var(--ctp-subtext0)) !important;
	}
}
```

# Sanctum

Distributed under the [MIT License](https://github.com/jdanielmourao/obsidian-sanctum/blob/main/LICENSE)

## With mask image

All icons

```css
li.is-checked:where(li[data-task='*']) input[type='checkbox'],
.markdown-source-view input[type='checkbox']:where([data-task='*']):checked {
	background-color: transparent;
	border-width: 0;
	pointer-events: none;

	&:hover{
		box-shadow: none;
		border-color: transparent;
		pointer-events: none;
	}
	&::after {
		-webkit-mask-size: 110%;
		pointer-events: none;
		left: 0px;
	}
}

li[data-task='*'] input[type='checkbox']:checked,
input[type='checkbox'][data-task='*'] {
	&::after {
		background-color: var(--yellow);
		-webkit-mask-image: url("data:image/svg+xml,...");
		/* Some icons needs additional properties, such as -webkit-mask-size, top, transform, ... */
	}
}
```

# ITS

License: [GPL-2.0](https://github.com/SlRvb/Obsidian--ITS-Theme/blob/main/LICENSE)

## With mask image

All icons

```css
body:not(.alt-chkbx-off) {
    & .markdown-source-view.mod-cm6 .HyperMD-task-line[data-task],
    & .task-list-item.is-checked {
        &:is([data-task=">"]) {
            & :is(.task-list-label, p) > input:is([type=checkbox], [type=checkbox i]):checked,
            & > input:is([type=checkbox], [type=checkbox i]):checked
            {
                background-color: transparent;
                font: var(--its);
                font-family: var(--its);
                font-size: inherit;
                font-weight: 10;
                text-align: center;
                
                border: 0;
                cursor: pointer;
                -webkit-mask-image: unset;//Border Theme Fix
                
                &::after { 
                    background-color: transparent;
                    top: -4px; 
                    left: 0px;
                    -webkit-mask-image: unset;
                }
            }
        }
    }
}

body:not(.alt-chkbx-off) {
@each $checkbox, $set in $checkboxes {
    & .markdown-source-view.mod-cm6 .task-list-item-checkbox[data-task=">"],
    & .task-list-item.is-checked[data-task=">"] > input[type=checkbox]:checked,
    & .task-list-item.is-checked[data-task=">"] p > input[type=checkbox]:checked
    {
        &::after {
            content: "\EC03";
            color: var(--text-normal);
            transform: none;
        }
    }
}
```

# Primary

License: [GPL-3.0](https://github.com/primary-theme/obsidian/blob/main/LICENSE)

## With mask image

All checkboxes, except `- [/]`

```css
input[type=checkbox]:checked {
    border-color: var(--checked-border-color);
}

input[type=checkbox]:checked:hover {
	border-color: var(--checked-border-color-hover);
}

input[type=checkbox]:checked[data-task=">"]:hover {
	box-shadow: none;
}

li[data-task=">"] input[type=checkbox]:checked:hover {
	background-color: transparent;
	border-color: transparent;
	box-shadow: none;
}

input[type=checkbox]:checked[data-task=">"],
li[data-task=">"] > input:checked,
li[data-task=">"] > p > input:checked {
    background-color: transparent;
    border-color: transparent;
    
    &:after {
        background-color: var(--resched-chbx-color);
        -webkit-mask-position: 50% 50%;
        -webkit-mask-size: 110%;
        -webkit-mask-image:url("data:image/svg+xml,...");
    }
}
```

## Other method(s)

- [/] In Progress `- [/]`

```css
input[type=checkbox]:checked[data-task="/"],
li[data-task="/"] > input:checked,
li[data-task="/"] > p > input:checked {
    background: linear-gradient(to right, var(--inprogress-chbx-color) 50%, var(--checklist-bg) 50%);
    background-repeat: no-repeat;
    background-clip: padding-box;
    border-color: var(--inprogress-chbx-border-color);
    
    &:after {
        background-color: transparent;
        -webkit-mask-image: none;
    }

    &:hover {
        background: linear-gradient(to right, var(--inprogress-chbx-color-hover) 50%, var(--checklist-bg) 50%);
        border-color: var(--inprogress-chbx-border-color);
    }
}
```

# Tokyo Night

Distributed under the [MIT License](https://github.com/tcmmichaelb139/obsidian-tokyonight/blob/main/LICENSE)

From [[#Border]]

# Border

Distributed under the [MIT License](https://github.com/Akifyss/obsidian-border/blob/main/LICENSE)

## With mask image

All icons

```css
input[data-task=">"]:checked,
li[data-task=">"] > input:checked,
li[data-task=">"] > p > input:checked {
    --checkbox-marker-color: transparent;
    border: none;
    border-radius: 0;
    background-image: none;
    background-color: currentColor;
    -webkit-mask-size: var(--checkbox-icon);
    -webkit-mask-position: 50% 50%
}

input[data-task=">"]:checked,
li[data-task=">"] > input:checked,
li[data-task=">"] > p > input:checked {
    --checkbox-color-hover: var(--color-pink);
    color: var(--color-pink);
    -webkit-mask-image: url('data:image/svg+xml,...');
}
```

# Spectrum (Unmaintained Pre-1.0 Release)

Distributed under the [MIT License](https://github.com/wiktoriavh/Spectrum/blob/main/LICENSE)

## With background image

All icons

```css
.view-content ul > li.task-list-item.is-checked {
	text-decoration: none;
}

.view-content .task-list-item-checkbox {
	appearance: none;
	box-sizing: border-box;
	border: 1px solid var(--text-muted);
	border-radius: var(--size-0-5);
	position: relative;
	width: 1.5em;
	height: 1.5em;
	margin: 0;
	outline: none;
	margin-right: var(--size-1);
	margin-bottom: var(--size-0-5);
	cursor: pointer;
	filter: none;
	top: var(--size-1-5);
}

.markdown-source-view.mod-cm6 .task-list-item-checkbox {
	vertical-align: baseline;
}

.view-content .task-list-item-checkbox:checked {
	border: none;
	background-color: var(--main-node);
}

.view-content li,
.view-content .HyperMD-list-line {
	.task-list-item-checkbox:checked::before {
		content: '';
		position: absolute;
		bottom: 0;
		left: 0;
		
		width: 100%;
		height: 100%;
		line-height: 0;
		font-size: 1.5rem;
		color: black;
		
		display: flex;
		justify-content: center;
		align-items: center;
		
		background-image: url("data:image/svg+xml,...");
	}
	.task-list-item-checkbox:checked::after {
		display: none;
	}

}

.view-content li[data-task='>'] .task-list-item-checkbox:checked::before,
.view-content .task-list-item-checkbox[data-task='>']:checked::before {
  background-image: url("data:image/svg+xml,...");
}
```

# Cyber Glow

Distributed under the [MIT License](https://github.com/ArtexJay/Obsidian-CyberGlow/blob/main/LICENSE)

## With mask image

All icons

```css
.markdown-preview-view .task-list-item-checkbox {
	border: 1px solid var(--text-accent);
	box-shadow: 0 0 0.5em var(--text-accent);
}
.CG-custom-checkbox .view-content .task-list-item-checkbox {
	appearance: none;
	scale: 1.22;
}
.CG-custom-checkbox input[type='checkbox']:checked:after {
	background-color: black;
}

.CG-custom-checkbox .task-list-item-checkbox[data-task='>'],
.CG-custom-checkbox ul > li.task-list-item[data-task='>'] .task-list-item-checkbox {
	background-color: skyblue;
	border: 1px solid skyblue;
    box-shadow: 0 0 5px skyblue, 0 0 10px skyblue, 0 0 15px skyblue;
}
.CG-custom-checkbox .task-list-item-checkbox[data-task='>']:hover,
.CG-custom-checkbox ul > li.task-list-item[data-task='>'] .task-list-item-checkbox:hover {
	background-color: rgb(112, 174, 198);
	border: 1px solid rgb(112, 174, 198);
}
.CG-custom-checkbox [data-task='>'] input[type='checkbox']:checked:after,
.CG-custom-checkbox [data-task='>'][type='checkbox']:checked:after {
	-webkit-mask-image: url('data:image/svg+xml,...');
	-webkit-mask-size: 100%;
}
```

# LYT Mode

Distributed under the [MIT License](https://github.com/nickmilo/LYT-Mode/blob/main/LICENSE)

## With mask image

All checkboxes, except `- [/]`

```css
input[data-task]:checked,
li[data-task] > input:checked {
    background-image: none;
    background-repeat: no-repeat;
    background-position: center;
    border: 1px solid var(--border-900);
}

/* All of them, except [ ], ["x"] and [">"] */
input[type=checkbox][data-task]:is([data-task="?"]):checked:after,
.markdown-preview-view li:is([data-task="?"]) input[type=checkbox].task-list-item-checkbox:checked:after {
    display: none;
}

input[data-task="?"]:checked,
li[data-task="?"] > input:checked {
    border: none;
    box-shadow: none;
    cursor: default;

    -webkit-mask-size: var(--font-text-size);
    -webkit-mask-position: 50% 50%;
    
    background-color: var(--color-green-700);
    -webkit-mask-image: url("data:image/svg+xml,...");
}
```

## Other method(s)

- [/] Incomplete `- [/]`

```css
input[data-task="/"]:checked,
li[data-task="/"] > input:checked {
    cursor: default;
    
    background-position: center;
    background-size: 100%;
    background: linear-gradient(to left, var(--background-primary) 50%, var(--background-modifier-border) 50%);
}
```

# Shiba Inu

Distributed under the [MIT License](https://github.com/faroukx/Obsidian-shiba-inu-theme/blob/main/LICENSE.txt) 

## With mask image

All icons

```css
.custom-checkboxes [data-task=">"] input[type=checkbox]:checked,
.custom-checkboxes [data-task=">"][type=checkbox]:checked, {
    --checkbox-color: transparent;
    --checkbox-color-hover: transparent;
    border-width: 0
}

/* ::before never rendered because no content */
.custom-checkboxes [data-task=">"] input[type=checkbox]:checked:before,
.custom-checkboxes [data-task=">"][type=checkbox]:checked:before {
    color: rgb(var(--cyan));
    margin: 0 3px;
    position: absolute;
    left: calc(var(--checkbox-size) * 1);
    font-weight: 700
}

.custom-checkboxes [data-task=">"] input[type=checkbox]:checked:after,
.custom-checkboxes [data-task=">"][type=checkbox]:checked:after {
    -webkit-mask-image: url("data:image/svg+xml,...");
    -webkit-mask-size: contain;
    background-color: rgb(var(--cyan));
    left: 0
}
```

# PLN

Distributed under the [GPL-3.0 License](https://github.com/PipeItToDevNull/PLN/blob/master/LICENSE.md)

## With mask image

All icons

```css
input[type=checkbox][data-task=">"],
ul > li.task-list-item[data-task=">"] > .task-list-item-checkbox {
    background-color: var(--color-orange);
    border-color: var(--color-orange);
}
input[type=checkbox][data-task=">"]:checked:after,
ul > li.task-list-item[data-task=">"] > .task-list-item-checkbox:checked:after {
    -webkit-mask-image: url("data:image/svg+xml;...");
}
```

# Obsidianotion

Distributed under the [Unlicense License](https://github.com/diegoeis/obsidianotion/blob/master/LICENSE)

From [[#Minimal]]

## With content

- [s] Thread? / String?  `- [s]`

```css
input[data-task='s']:checked:before,
li[data-task='s'] > input:checked:before,
li[data-task='s'] > p > input:checked:before {
  content: "🧵";
  font-size: 0.9rem;
}

input[data-task='s']:checked,
li[data-task='s'] > input:checked,
li[data-task='s'] > p > input:checked {
  --checkbox-marker-color: transparent;
  background-color: transparent;
  border-color: transparent;
}
```

# Maple

Distributed under the [MIT License](https://github.com/subframe7536/obsidian-theme-maple/blob/main/LICENSE)

From [[#Border]]

# EbullientWorks

Distributed under the [CC0-1.0 License](https://github.com/ebullient/obsidian-theme-ebullientworks/blob/main/LICENSE)

## With content

All icons except `- [/]`

```css
div[data-task] > label.task-list-label,
ul > li.task-list-item,
ul > li.task-list-item > p  {
	color: var(--text-normal);
	font-weight: unset;
	text-decoration: unset;

	> input.task-list-item-checkbox[type=checkbox]:not(:checked) {
		background-color: unset;
		background: unset;
	}
}

div[data-task=">"] > label.task-list-label,
li.task-list-item[data-task=">"],
li.task-list-item[data-task=">"] > p,
.markdown-source-view.mod-cm6 .HyperMD-task-line[data-task=">"] {
    --checkbox-color: var(--checkbox-deferred);
    --checkbox-border-color: var(--checkbox-deferred);
    --checkbox-marker-color: transparent;
}

input[type=checkbox][data-task="#{$character}"]:checked,
li[data-task="#{$character}"] > input[type=checkbox]:checked,
li[data-task="#{$character}"] > p > input[type=checkbox]:checked {
    background-color: unset;
    background: unset;

    &::after {
		transform: none;
		-webkit-mask-image: none;
		background: unset;
		position: absolute;
		text-align: center;
		font-weight: var(--font-normal);
		font-size: calc(var(--checkbox-size) - 2px);
		font-family: var(--font-monospace);
		line-height: var(--checkbox-size);
		left: 50%;
		margin-left: calc(-1 * (var(--checkbox-size) / 2));
		color: var(--checkbox-color);
		content: '>';
		display: block;
    }
}
```

## Other method(s)

- [/] Incomplete `- [/]`

```css
div[data-task="/"] > label.task-list-label,
li.task-list-item[data-task="/"],
li.task-list-item[data-task="/"] > p,
.markdown-source-view.mod-cm6 .HyperMD-task-line[data-task="/"] {
	--checkbox-color: var(--checkbox-in-progress);
	--checkbox-border-color: var(--checkbox-in-progress);
	--checkbox-marker-color: transparent;
}
	
input[data-task="#{$character}"]:checked,
li[data-task="#{$character}"] > input[type=checkbox]:checked,
li[data-task="#{$character}"] > p > input[type=checkbox]:checked {
	background: linear-gradient(135deg, transparent 50%, var(--checkbox-in-progress) 50%);
	
	&:after {
		transform: none;
		-webkit-mask-image: none;
		background: unset;
		content: ' ';
	}
}
```

