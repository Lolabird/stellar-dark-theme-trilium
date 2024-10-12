# Stellar Dark Theme 
Dark theme for [Trilium Notes](https://github.com/zadam/trilium)

## Features
### Native Styles
* High contrast
* Scrolling tables with sticky headers on both axes
* Vertical floating buttons that have much less overlap with content of notes
* Bright colors

### Enhanced Addon Styles
*See 'Usage Instructions' for information on how to enable these.*
* Zen Mode
* Matching syntax highlight in text notes
* Position shown in TOC
* And much more!

## Usage Instructions
### Installation
* Download the latest version of Trilium
* Download the latest release of Stellar Dark
* In your trilium instance right click a note you want to import the theme into
* Select "Import into note" in the context menu
* Uncheck "Safe import" and upload the zip file you just downloaded
* Click on the Trilium logo in the upper left corner and select Options -> Appearance
* Under "Theme", choose Stellar Dark
* Enjoy!

### Enabling Addon Features
#### Zen Mode
* Create a 'JS frontend' code note
* Add the `#widget` attribute to 'Owned Attributes' (the button with three lines and a checkmark)
* Add the following code (created by [Nriver]) to the note
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
* Reload (`ctrl+r` or `F5`) Trilium to enable the script

##### Usage
Press `alt+z` or the spa button in the launcher (left most panel) to enable/disable zen mode.

There are two types of zen mode available:
1. Right panel enabled
2. Right panel disabled

Right panel is enabled by default. If you would like to disable it, you can either add the following code in a new CSS note or uncomment it in the Stellar Dark theme as seen in the video below.
![Zen Mode](/screenshots/SD_Zen.mp4)


## Screenshots and Videos
![Text Showcase](/screenshots/SD_Main.png)
![Map Showcase](/screenshots/SD_Map.png)
![Code Showcase](/screenshots/SD_Code.png)

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

Find more addons made by the Trilium community at [Nriver's "Awesome Trilium" page](https://github.com/Nriver/awesome-trilium?tab=readme-ov-file#%EF%B8%8F-widgets)!
