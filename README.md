# Folder Note Plugin

Obsidian Plugin: Add description note to a folder. 

## Usage

- **Add** description note for a folder: CTRL+Click on a folder node in the file explorer panel.
- **Show** description note of a folder: Just Click the folder.
- **Delete** description note of a folder: Just delete the opened note file.
- **Setting** : configure the note name and template.

## How it works

Just a simple trick. When create the description, a note file with title same as the folder name will be created in the clicked folder. However, the note file is hidden by CSS rules of the plugin. The reason that the file is hidden because:

- the file will not always be shown right after the folder node if there are subfolders.
- The file name may looks abnormal or weird.
- In the future, the description will be automatically generated based on the files and their contents in the folder. 

About setting the note file name and inital content:

- The note name can be set to others, like `_about_` in the settings panel.
- The {{FOLDER_NAME}} in the note name setting will be replaced with the folder name.
- The initial content for the description can be configured in the settings panel.

## Plans for future

- Automatic generate brief contents for the file based on the files and their contents in the folder, like the software [Trilium](https://github.com/zadam/trilium) does. 

## Known issues

- Do not try to create a new file by context menu or Ctrl+N (which will create a file named 'Untitled.md' firstly), and change its name to the folder name manually. If you do that, the file will not be hidden due to internal mechanism of Obsidian. However, if you close and reopen Obsidian, it will be hidden again.

## Manually installing the plugin

- Copy over `main.js`, `styles.css`, `manifest.json` to your vault `VaultFolder/.obsidian/plugins/folder-note-obsidian/`.

## Build

- Clone this repo.
- `npm i` or `yarn` to install dependencies
- `npm run dev` to start compilation in watch mode.
