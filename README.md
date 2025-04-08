# Stellar Dark Theme 
Dark theme for [Trilium Notes](https://github.com/zadam/trilium) and [TriliumNext](https://github.com/TriliumNext/Notes).

![Text Showcase](/screenshots/SD_main.png)

## Features
### Native Styles
* Dark theme
* High contrast
* Scrolling tables with sticky headers on both axes
* Vertical floating buttons for less content overlap
* Different styles for different types of links
* Custom fonts
* Bright colors

### Enhanced Addon Styles
_See 'Usage Instructions' for information on how to enable these.*_

* Zen mode (with right panel enabled)*
* Matching code note and code block syntax highlight*
* Position shown in TOC
* And much more!

_*If you are using TriliumNext, zen mode and code block syntax highlight are already natively available in the application. No extra steps are required for these addons unless you want to disable the right panel in zen mode. Please see the usage instructions below if this is the case._

## Usage Instructions
### Installation
* Download and install the latest version of Trilium or TriliumNext
* Download the latest release of EverForest Ant Dark

    * OG_StellarDark if you use the original Trilium Notes
    * Next_StellarDark if you use TriliumNext

* In your trilium instance right click a note you want to import the theme into
* Select "Import into note" in the context menu
* Uncheck "Safe import" and upload the zip file you just downloaded
* Click on the Trilium logo in the upper left corner and select Options -> Appearance
* Under "Theme", choose EverForest Ant Dark
* Enjoy!

### Enabling Addon Features
#### Zen Mode
* Create a 'JS frontend' code note
* Add the `#widget` attribute to 'Owned Attributes' (the button with three lines and a checkmark)
* Add the following code (created by [Nriver](https://github.com/Nriver/awesome-trilium/issues/44)) to the note:

    ```js
    api.addButtonToToolbar({
        title: 'Zen mode',
        icon: 'spa',
        action: function() {
            $("body").toggleClass("zen-mode");
        },
        shortcut: 'alt+z'
    });
    ```
* Reload (<kbd>ctrl+r</kbd> or <kbd>F5</kbd>) Trilium to enable the script

##### Usage
Press <kbd>alt+z</kbd> or the zen (spa) button in the launcher (left most panel) to enable/disable zen mode.

There are two types of zen mode available:
1. Right panel enabled
2. Right panel disabled

The right panel is enabled by default. If you would like to disable this in the original Trilium, you can either add the following code in a new CSS note or uncomment in the theme.

```css
/*hide right pane*/
.zen-mode #right-pane {
    display: none !important;
}
```
https://github.com/user-attachments/assets/dc398d7c-d3e9-402c-86b2-9576f402a13d

In TriliumNext, you will need to comment out this code:

```css
/*show right pane*/
body.zen div.gutter {
    display: block !important;
}
body.zen div#right-pane:not(.hidden-int) {
	display: flex !important;
}

```
https://github.com/user-attachments/assets/ce651ab5-d970-49c8-bfef-94962cead03c

##### Added Features
* Window control buttons are still accessible in zen mode*
* Zen button is still accessible in zen mode for easy disabling in case you don't remember the shortcut*
* Bottom panel widgets are not visible in zen mode
* Optional disabling of right panel in zen mode

_*Natively available in TriliumNext_

#### Show Position in TOC and Syntax Highlight
Please go to each addon's respective page for instructions on how to enable these addons.
* [Show Position in TOC](https://github.com/SiriusXT/trilium-show-position-in-toc)
* [Syntax Highlight](https://github.com/antoniotejada/Trilium-SyntaxHighlightWidget)

## Screenshots
The following screenshots are from TriliumNext. Most of the features shown are also available in either OG Trilium or can be included via addons. However, some features, like cards (excluding quotes) and <kbd>kbd</kbd>, are only available in TriliumNext.

https://github.com/user-attachments/assets/a19c6459-71c1-454f-921c-78c09088c9f4

![Relation Map](/screenshots/SD_Relation_Map.png)

![Code Note](/screenshots/SD_Code.png)

https://github.com/user-attachments/assets/4874d7b6-e8bf-4c07-87d1-3869bb09c68d

## Credits and Resources
### Fonts
* [Fira](https://github.com/mozilla/Fira)

### Addons Featured in the Screenshots and Videos
* [Breadcrumbs](https://github.com/rauenzi/Trilium-Breadcrumbs)
* [Scratchpad](https://github.com/zadam/trilium/discussions/1613#discussioncomment-638984)
* [Show Position in TOC](https://github.com/SiriusXT/trilium-show-position-in-toc)
* [Syntax Highlight](https://github.com/antoniotejada/Trilium-SyntaxHighlightWidget)
* [Theme Switch](https://github.com/madodig/trilium-widget-theme-switch)
* [Trilium Chat](https://github.com/soulsands/trilium-chat)
* WordCount (Featured in the [Demo Document](https://github.com/zadam/trilium/wiki/Document#demo-document))
* [Zen Mode](https://github.com/Nriver/awesome-trilium/issues/44)

Find more addons made by the Trilium community at [Nriver's "Awesome Trilium" page](https://github.com/Nriver/awesome-trilium?tab=readme-ov-file#%EF%B8%8F-widgets), and check out my other themes [EverForest Ant Dark](https://github.com/Lolabird/everforest-ant-dark-trilium-theme) and [Ocean Dark](https://github.com/Lolabird/ocean-dark-trilium-theme) while you're at it!!
