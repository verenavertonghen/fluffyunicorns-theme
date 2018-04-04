# Fluffy Unicorns Theme

## How to create your own theme in VSCODE

### Setup
Create a directory and give it the name of your theme.

You will need:
* a package.json file which describes the theme
* a subdirectory `themes` which has a theme file, in JSON format
* (a README, not necessary but always a nice touch)

Move your directory to `~/.vscode/extensions` (OSX/Linux) or `%USERPROFILE%\.vscode\extensions` (Windows).

### Basic file contents
*package.json*
```json
{
    "publisher": "yourpublishid",
    "engines": {
        "vscode": "^1.0.0"
    },
    "categories": [
        "Themes"
    ],
    "contributes": {
        "themes": [
            {
                "label": "yourthemename",
                "uiTheme": "vs-dark",
                "path": "./themes/yourthemename.json"
            }
        ]
    }
}
```

*yourthemename.json*
```json
{
    "name": "yourthemename",
    "type": "dark",
    "colors": {
    },
    "tokenColors": [
    ]
}
```

### Test if your setup works
Use `cmd+shift+P` and run `Reload Window`.
Use `cmd+shift+P` and run `Preferences: Color Theme`.
You should now be able to select the theme you just created.

### Inspecting scopes
Use `cmd+shift+P` and run `Developer: Inspect TM Scopes`.

## Resources & Inspiration
* https://code.visualstudio.com/docs/extensions/themes-snippets-colorizers
* https://medium.com/@caludio/how-to-write-a-visual-studio-code-color-theme-from-scratch-7ccb7e5da2aa
* https://github.com/sailorhg/fairyfloss

## ToDo
* make a build script and use yaml files
* tweak design
* publish package
* basic index.html
* update readme add emojis
* share everywhere