# README
This repository contains a vscode theme for Perspectives ARC. It is based on the `Dark+ (default dark)` theme.

**Note** This repo just contains the theme, not the tokenizer you need in your vscode installation to provide the full experience of syntax coloring of Perspectives ARC files. The tokenizer (for vscode) can be found in the repository [language-perspectives-arcII](https://github.com/joopringelberg/language-perspectives-arcII.git).

## Getting it
Go to the [latest release](https://github.com/joopringelberg/theme-perspectives-arc/releases) (on Github: Code tab, section releases on the right, click `latest`). Download the file named `perspectives-arc-X.Y.Z.vsix`, where X, Y and Z are the components of the semantic version number.


## Installing it
You can manually install both the language extension and the theme extension (as it is packaged in a .vsix file). Use the `Install from VSIX` command in the Extensions view command dropdown, or the `Extensions: Install from VSIX command` in the Command Palette, point to the .vsix file.

## Uninstalling it
VS Code makes it easy to manage your extensions. You can install, disable, update, and uninstall extensions through the Extensions view, the Command Palette (commands have the `Extensions:` prefix).

## Example files
A model file example can be found in the `arc sources` directory.

## Release Notes

### 0.0.1

Initial release of language-perspectives-arc.

# Developing
This theme was constructed by 

* adding to the `editor.tokenColorCustomizations` settings, as described in [Syntax colors](https://code.visualstudio.com/api/extension-guides/color-theme#syntax-colors)
* following the instructions in [Create a new color theme](https://code.visualstudio.com/api/extension-guides/color-theme#create-a-new-color-theme).

To further develop the theme, either

* adapt the `perspectives-arc-color-theme.json` file directly. When the Extension Development Host window is open (open with F5), saved changes are reflected life, or
* wwitch to `theme-perspectives-arc`, add to the settings (as above). Changes are reflected live in the Extension Development Window. Later regenerate a theme file (as above).

**Note** The name of the theme as it appears in the `Code/Preferences/Color Theme` list is governed by the `label` property in `package.json`.

## Package for distribution
Apart from publishing this extension on a marketplace (which we do not cover here), it is possible to package the extension. It can then be distributed, e.g. from github. The instructions here are taken from [microsoft](https://code.visualstudio.com/api/working-with-extensions/publishing-extension#packaging-extensions).

Package with this command:

```
vsce package
```

## Releasing
Follow these steps:
* set the new version number in the package file.
* run vsce package again to produce a new .vsix file (it will have the right version number).
* push all changes to github.
* create a new tag, use the semantic version number preceded by 'v', e.g. `v0.1.0`.
* push the tag on the command line (vscode won't do it):

```
    git push origin <tagname>
```
* on Github: create a new release using that tag.
* add the `perspectives-arc-X.Y.Z.vsix` to it.