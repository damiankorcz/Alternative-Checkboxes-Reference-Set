# Alternative Checkboxes Reference Set

# 🎯 Objective

This is an initiative to help standardize the Alternative Checkboxes feature commonly used by the community in Obsidian.md. We are trying to achieve this by analyzing all publicly available implementations of Alternative Checkboxes within Obsidian be it as a Theme, CSS Snippet or Plugin. We are also looking to see if there are any other tools and external standards which could help with our decisions.

# 🗣️ Discussion

Currently, all discussion regarding this is carried out in a thread within the Official Obsidian Discord. For more information please head over there:
https://discord.com/channels/686053708261228577/1291469509336502272

# ✅ Current Progress

(All current goals are subject to change and are provided as a general idea so far. 📌 = Currently being worked on.)

## Understanding the Current State 
- [x] Round up all currently available Obsidian themes in the Theme Store and check for Alternative Checkboxes implementations. If Alternative Checkboxes present:
	- [x] Define the use case (Syntax and Meaning).
	- [x] Add the theme to the vault if it has Alternative Checkboxes.
	- [x] Include link for the Repository, Documentation (if any) and Code used to implement them.
> **Outcome:** Identified 44/282 themes which use a form of Alternative Checkboxes (at the time).

- [ ] 📌 Review collected data to identify the current "standard" use cases for each checkbox type; given syntax and it's assigned meaning. Also, take note of other alternative meanings and how many themes use those.
- [ ] 📌 Review the CSS from each theme to identify the patterns used to implement the feature.

## Creating a Reference Set
- [ ] Decide on the initial set of Checkboxes.
	- [ ] Possibly use a Tier system which rates the checkboxes based on their current popularity / percentage of use across themes.
- [ ] Best practices / conventions.
	- [ ] Agreed syntax / meaning.
	- [ ] Agreed icons to represent the checkbox?
	- [ ] Agreed colours?
- [ ] Assure that all plugins which interact with Alternative Checkboxes are setup to support the Reference Set. Provide any help / adapt based on feedback.

## CSS Guidelines for Implementation
- [ ] Barebones CSS Implementation of the Reference Set.
	- [ ] Decide if the implementation provides example icons (likely [Lucide](https://lucide.dev/) to match existing Obsidian icons).
	- [ ] Naming convention for CSS Variables.
- [ ] General guidelines for Theme Developers to help users with using the Checkboxes they want to use.
	- [ ] Allow users to fully disable the Theme's Checkbox implementation if the user prefers to use their own (likely a CSS snippet). This might include adding a Style Settings Toggle, providing the Alternative Checkbox feature as an optional CSS Snippet independent of the Theme's CSS or making sure the implementation within the Theme is easily overwritable by a CSS Snippet.

## Adaptation Guidelines / Tools
- [ ] Reach out to Theme Developers which Alternative Checkbox implementation doesn't align with the Reference Set to see if they are willing to adapt. 
- [ ] Create a plan for helping uses to convert their notes when a theme changes the Alternative Checkbox/es.
	- [ ] Methods / Plugins / Tools required to convert user's existing notes to match the Reference Set or adapt to the changes which a theme implements to align with the Reference Set.
	- [ ] Methods of effectively notifying changes by Theme devs to users: Notes in Settings, Changelogs, hovering over Help icon, etc.

# 🗃️ Usage

This repository serves as a central place for all the files relevant to the discussion. It's intended to be used directly as an Obsidian Vault. All themes and snippets that include Alternative Checkboxes are pre-installed for ease of testing. The following Community plugins are also included:
- `Style Settings` - Required for some themes.
- `Code Editor Shortcuts` - Easier multiline editing.

Please refer to the License section below for more information about what license each Theme / CSS Snippet / Plugin are distributed under.

Ideally, each Alternative Checkbox implementation should be previewed with **only** the relevant Theme / CSS Snippet enabled to avoid styling issues. Remember to only use one CSS Snippet at a time when testing and to have none enabled when testing Theme implementations (unless required). For CSS Snippets, I'd advise to test those with the Default theme enabled unless stated otherwise.

For convenience, I've pinned `Change theme` in the Command Palette for a quicker way to change themes.

# 🛠 Contributing

At the moment, there are no direct guidelines for contributing to this repository. Ideally, any contributions should be mentioned in the Discussion thread first.

# 📣 Acknowledgments

Special thanks to the following people for their direct contributions to this repository:
- [**claremacrae** ](https://github.com/claremacrae) - For assisting in parsing through all available themes in Obsidian's Community Themes Store.
- [**ElsaTam**](https://github.com/ElsaTam) - For reviewing the CSS in each theme to identify the patterns used to implement the feature.

Also, big thanks to everyone that contributed feedback over in the Discord Thread.

# 📝 License

This repository contains Themes, CSS Snippets and Plugins which were added for convenience of previewing the relevant documentation. Here are the licenses under which they are distributed under:

<details>
<summary>Themes</summary>

- [Minimal](https://github.com/kepano/obsidian-minimal) - Distributed under the [MIT License](https://github.com/kepano/obsidian-minimal/blob/master/LICENSE)
- [Things](https://github.com/colineckert/obsidian-things) - Distributed under the [MIT License](https://github.com/colineckert/obsidian-things/blob/main/LICENSE)
- [Blue Topaz](https://github.com/PKM-er/Blue-Topaz_Obsidian-css) - Distributed under the [MIT License](https://github.com/PKM-er/Blue-Topaz_Obsidian-css/blob/master/LICENSE)
- [AnuPpuccin](https://github.com/AnubisNekhet/AnuPpuccin) - Distributed under the [GPL-3.0 License](https://github.com/AnubisNekhet/AnuPpuccin/blob/main/LICENSE)
- [Sanctum](https://github.com/jdanielmourao/obsidian-sanctum) - Distributed under the [MIT License](https://github.com/jdanielmourao/obsidian-sanctum/blob/main/LICENSE)
- [ITS](https://github.com/SlRvb/Obsidian--ITS-Theme) - Distributed under the [GPL-2.0 License](https://github.com/SlRvb/Obsidian--ITS-Theme/blob/main/LICENSE)
- [Primary](https://github.com/primary-theme/obsidian) Distributed under the [GPL-3.0 License](https://github.com/primary-theme/obsidian/blob/main/LICENSE)
- [Tokyo Night](https://github.com/tcmmichaelb139/obsidian-tokyonight) - Distributed under the [MIT License](https://github.com/tcmmichaelb139/obsidian-tokyonight/blob/main/LICENSE)
- [Border](https://github.com/Akifyss/obsidian-border) - Distributed under the [MIT License](https://github.com/Akifyss/obsidian-border/blob/main/LICENSE)
- [Spectrum](https://github.com/wiktoriavh/Spectrum) - Distributed under the [MIT License](https://github.com/wiktoriavh/Spectrum/blob/main/LICENSE)
- [Cyber Glow](https://github.com/ArtexJay/Obsidian-CyberGlow) - Distributed under the [MIT License](https://github.com/ArtexJay/Obsidian-CyberGlow/blob/main/LICENSE)
- [LYT Mode](https://github.com/nickmilo/LYT-Mode) - Distributed under the [MIT License](https://github.com/nickmilo/LYT-Mode/blob/main/LICENSE)
- [Shiba Inu](https://github.com/faroukx/Obsidian-shiba-inu-theme) - Distributed under the [MIT License](https://github.com/faroukx/Obsidian-shiba-inu-theme/blob/main/LICENSE.txt) 
- [PLN](https://github.com/PipeItToDevNull/PLN) - Distributed under the [GPL-3.0 License](https://github.com/PipeItToDevNull/PLN/blob/master/LICENSE.md)
- [Obsidianotion](https://github.com/diegoeis/obsidianotion) - Distributed under the [Unlicense License](https://github.com/diegoeis/obsidianotion/blob/master/LICENSE)
- [Maple](https://github.com/subframe7536/obsidian-theme-maple) - Distributed under the [MIT License](https://github.com/subframe7536/obsidian-theme-maple/blob/main/LICENSE)
- [Ebullientworks](https://github.com/ebullient/obsidian-theme-ebullientworks) - Distributed under the [CC0-1.0 License](https://github.com/ebullient/obsidian-theme-ebullientworks/blob/main/LICENSE)
- [Pine Forest Berry](https://github.com/Nilahn/pine_forest_berry/) - Distributed under the [MIT License](https://github.com/Nilahn/pine_forest_berry/blob/main/LICENSE)
- [Aura](https://github.com/ashwinjadhav818/obsidian-aura) - Distributed under the [GPL-2.0 License](https://github.com/ashwinjadhav818/obsidian-aura/blob/master/LICENSE)
- [Vicious](https://github.com/zaheralmajed/vicious-theme-obsidian) - Distributed under the [MIT License](https://github.com/zaheralmajed/vicious-theme-obsidian/blob/main/LICENSE)
- [Simple](https://github.com/diegoeis/simple-obsidian) - Distributed under the [Unlicense License](https://github.com/diegoeis/simple-obsidian/blob/main/LICENSE)
- [Elegance](https://github.com/Victologo/elegance-theme) - Distributed under the [MIT License](https://github.com/Victologo/elegance-theme/blob/main/LICENSE)
- [Material Ocean](https://github.com/dragonwocky/obsidian-material-ocean) - Distributed under the [MIT License](https://github.com/dragonwocky/obsidian-material-ocean/blob/main/LICENSE)
- [Sparkling Night](https://github.com/isax785/obsidian-sparkling-night) - Distributed under the [MIT License](https://github.com/isax785/obsidian-sparkling-night/blob/master/LICENSE)
- [Kakano](https://github.com/isaacfreeman/kakano-obsidian-theme) - Distributed under the [MIT License](https://github.com/isaacfreeman/kakano-obsidian-theme) 
- [Neo](https://github.com/lab-do/obsidian-neo) - Distributed under the [MIT License](https://github.com/lab-do/obsidian-neo/blob/main/LICENCE)
- [Feather](https://github.com/zfmohammed/obsidian-feather) - Distributed under the [MIT License](https://github.com/zfmohammed/obsidian-feather/blob/main/LICENSE)
- [Listive](https://github.com/efemkay/obsidian-listive-theme) - Distributed under the [MIT License](https://github.com/efemkay/obsidian-listive-theme/blob/master/LICENSE.md)
- [MagicUser](https://github.com/drbap/magicuser-theme-for-obsidian) - Distributed under the [MIT License](https://github.com/drbap/magicuser-theme-for-obsidian/blob/main/LICENSE)
- [Qlean](https://github.com/Fro-Q/Qlean) - Distributed under the [MIT License](https://github.com/Fro-Q/Qlean/blob/main/LICENSE)
- [Yue](https://github.com/GixoXYZ/YueObsidian) - Distributed under the [MIT License](https://github.com/GixoXYZ/YueObsidian/blob/main/LICENSE)
- [sQdthOne](https://github.com/KeithLerner/ObsidianMDsQdthOne) - Distributed under the [GPL-3.0 License](https://github.com/KeithLerner/ObsidianMDsQdthOne/blob/main/LICENSE)
- [Dracula Plus](https://github.com/saket61195/Dracula_obsidian_theme) - Distributed under the [MIT License](https://github.com/saket61195/Dracula_obsidian_theme/blob/main/LICENSE)
- [Solitude](https://github.com/KyleKlus/solitude-obsidian-theme) - Distributed under the [MIT License](https://github.com/KyleKlus/solitude-obsidian-theme/blob/main/LICENCE)
- [Prime](https://github.com/rivea0/obsidian-prime) - Distributed under the [GPL-3.0 License](https://github.com/rivea0/obsidian-prime/blob/main/LICENSE)
- [Sanctum Reborn](https://github.com/antoKeinanen/obsidian-sanctum-reborn) - Distributed under the [MIT License](https://github.com/antoKeinanen/obsidian-sanctum-reborn/blob/main/LICENSE)
- [Underwater](https://github.com/Seniblue/Underwater) - Distributed under the [MIT License](https://github.com/Seniblue/Underwater/blob/main/LICENSE)
- [Nightingale](https://github.com/frank0713/nightingale-obsidian) - Distributed under the [MIT License](https://github.com/frank0713/nightingale-obsidian/blob/main/LICENSE)
- [Reshi](https://github.com/contrapasso3/Reshi) - Distributed under the [GPL-3.0 License](https://github.com/contrapasso3/Reshi/blob/main/LICENSE)
- [Shade Sanctuary](https://github.com/Elevict/Shade-Sanctuary) - Distributed under the [MIT License](https://github.com/Elevict/Shade-Sanctuary/blob/main/LICENSE)
- [Sparkling Day](https://github.com/isax785/obsidian-sparkling-day) - Distributed under the [MIT License](https://github.com/isax785/obsidian-sparkling-day/blob/master/LICENSE)
- [Oreo](https://github.com/carols12352/Oreo-theme) - Distributed under the [GPL-3.0 License](https://github.com/carols12352/Oreo-theme/blob/master/LICENSE)
- [Gummy Revived](https://github.com/WinnerWind/gummy-revived) - Distributed under the [MIT License](https://github.com/WinnerWind/gummy-revived/blob/main/LICENSE)
- [Lorens](https://github.com/lorens-osman-dev/Lorens-Obsidian-Theme) - Distributed under the [MIT License](https://github.com/lorens-osman-dev/Lorens-Obsidian-Theme/blob/master/LICENSE)

</details>

<details>
<summary>CSS Snippets</summary>

- [ITS Alternative Checkboxes](https://github.com/SlRvb/Obsidian--ITS-Theme/blob/main/Guide/Alternate-Checkboxes.md) - Distributed under the [GPL-2.0 License](https://github.com/SlRvb/Obsidian--ITS-Theme/blob/main/LICENSE)
- [Phoenix Checkboxes](https://github.com/RyzenFromFire/obsidian-phoenix-checkboxes) - Distributed under the [MIT License](https://github.com/RyzenFromFire/obsidian-phoenix-checkboxes/blob/main/LICENSE)

</details>

<details>
<summary>Plugins</summary>

- [Style Settings](https://github.com/mgmeyers/obsidian-style-settings) - Distributed under the [GPL-3.0 License](https://github.com/mgmeyers/obsidian-style-settings/blob/main/LICENSE.md)
- [Editor Shortcuts](https://github.com/timhor/obsidian-editor-shortcuts) - Distributed under the [MIT License](https://github.com/timhor/obsidian-editor-shortcuts)
- [Tasks](https://github.com/obsidian-tasks-group/obsidian-tasks) - Distributed under the [MIT License](https://github.com/obsidian-tasks-group/obsidian-tasks/blob/main/LICENSE)
- [Snippetor](https://github.com/ebullient/obsidian-snippetor) - Distributed under the [AGPL-3.0 License](https://github.com/ebullient/obsidian-snippetor/blob/main/LICENSE)
- [ToggleList](https://github.com/thingnotok/obsidian-toggle-list) - Distributed under the [MIT License](https://github.com/thingnotok/obsidian-toggle-list/blob/master/LICENSE)

</details>

The inclusion of the Themes / CSS Snippets / Plugins in this repository is strictly for research purposes. If you are an author of any of them and would like me to remove them from this repository, please let me know by creating an issue.

The Documentation itself (Markdown files) are under the [Unlicense License](https://github.com/damiankorcz/Alternative-Checkboxes-Reference-Set/blob/main/LICENSE), unless another license is noted, especially next to code snippets from the themes.
