(Note that most of the Research work was done in October 2024 so some stats will be outdated)

## Understanding the Current State of the Ecosystem
- [x] Round up all currently available Obsidian themes in the Theme Store and check for Alternative Checkboxes implementations. If Alternative Checkboxes present:
	- [x] Define the use case (Syntax and Meaning).
	- [x] Add the theme to the vault if it has Alternative Checkboxes.
	- [x] Include link for the Repository, Documentation (if any) and Code used to implement them.
> **Outcome:** Identified 44/282 themes which use a form of Alternative Checkboxes (at the time).
> - The results for Themes are in: [[01 Theme Examples]]
> - The results for CSS Snippets are in: [[02 CSS Snippet Examples]]
> - The results for Plugins which interact with Alternative Checkboxes are in (WIP): [[03 Plugin Examples]]

- [x] Review collected data to identify the current "standard" use cases for each checkbox type; given syntax and it's assigned meaning. Also, take note of other alternative meanings and how many themes use those.
> **Outcome:** Filtered through all themes with Alternative Checkboxes using the data collected in [[01 Theme Examples]], outlined their usage and highlighted the themes which have an alternative meaning assigned to the specific syntax. 
> 
> You can see the entire breakdown for all checkbox types in: [[06 Syntax and Meaning Review]]
> 
> Overall, the equivalent of Minimal Theme's Alternative Checkboxes implementation (syntax in conjunction with meaning) are the most popular uses across other themes. The breakdown above highlights the differences in other themes to help see what those theme's wouldn't support if this set was used as the Reference. It should also help see how much impact it might have if one of those themes chooses to align with the Reference Set. I've included the download count for each theme as a rough estimation of theme's use by users.
> 
> You can see the breakdown for that in: [[07 Impact Breakdown]]

- [x]  Review the CSS from each theme to identify the patterns used to implement the feature.
> **Outcome:** We've identified the most common ways Alternative Checkboxes are implemented and have created a CSS Reset file as a temporary way to reset everything back to the default checkbox styling. This however spawned a new goal to try and get all Style Settings enabled themes to support a toggle function which allows the user to disable the theme's Alternative Checkboxes feature. So, the current priority is to have all themes mentioned in [[08 Style Settings Toggle Review]] and [[09 @container Style Queries Toggle Review]] implement the appropriate ways to toggle their theme's Alternative Checkboxes, allowing us to use the Reference Set CSS snippet with ease and making it simpler to customise this feature for users.

## Creating a Reference Set
- [x] Decide on the initial set of Checkboxes.
	- [x] Possibly use a Tier system which rates the checkboxes based on their current popularity / percentage of use across themes.
- [x] Best practices / conventions.
	- [x] Agreed syntax / meaning.
	- [x] Agreed icons to represent the checkbox?
	- [x] Agreed colours?
> **Outcome:** Settled on the most common set of Checkboxes which turned out to be what is defined in the Minimal Theme. A large portion of themes which implement Alternative Checkboxes directly use the same Checkbox syntax in conjunction with the meaning. Some themes expand on it. As mentioned above you can see the breakdown in: [[06 Syntax and Meaning Review]]
> The general consensus was to use Lucide icon set for the Reference Set since that's what Obsidian uses for it's UI. The icons were selected to match the same representations as other Alternative Checkboxes implementations. The Reference Set won't dictate what colour each icon will use but the CSS does accommodate setting any colour you want for your Theme / CSS snippet.

## CSS Guidelines for Implementation
- [x] Barebones CSS Implementation of the Reference Set.
	- [x] Decide if the implementation provides example icons (likely [Lucide](https://lucide.dev/) to match existing Obsidian icons).
	- [x] Naming convention for CSS Variables.
- [x] General guidelines for Theme Developers to help users with using the Checkboxes they want to use.
	- [x] Allow users to fully disable the Theme's Checkbox implementation if the user prefers to use their own (likely a CSS snippet). This might include adding a Style Settings Toggle, providing the Alternative Checkbox feature as an optional CSS Snippet independent of the Theme's CSS or making sure the implementation within the Theme is easily overwritable by a CSS Snippet.
> **Outcome:** As mentioned before, we've decieded to switch focus to making all themes that currently implement their own version of Alternative Checkboxes support toggles, which made creating a clean and well supported Reference Set a lot easier. This in turn eliminated the need to disrupt the current systems which users are utilising and removed the responsibility on our side to help with converting notes and current theme implementations. Now, we simply have a toggle in each theme which can be switched on/off (depending on how it's phrased) and have our Reference Set CSS snippet work as though it's overwriting the default theme.