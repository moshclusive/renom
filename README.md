# Renom

<p align="center"><img src="assets/logo.png" alt="Renom logo" width="128"></p>

> A fast, smart batch file renamer for Windows, built for designers. Pick files or folders, set a rule, preview the result, and run it. Nothing happens until you press RUN OPERATION.

## What Renom Does

Renom renames, copies, moves, zips and organizes large sets of files in one go. It is built around one idea: **IF, THEN**. First filter which files to touch (IF), then choose what to do with them (THEN).

Files that share the same base name are treated as one group. Logo.eps, Logo.jpg and Logo.png are renamed together, so one rule applies to the whole set.

## Key Features

- **File Name Format.** Build new names from the original name plus tokens like `{original}`, `{date}`, `{time}`, `{datetime}`, `{created}`, `{modified}` and `{folder name}`. Leave it blank and Renom numbers files automatically: 01, 02, 03.
- **Find and Replace.** Search inside file names for `_`, `-`, spaces, special characters, text inside `()`, `[]` or `{}`, numbers, duplicate spaces, first or last word, or custom text. Replace it or delete it.
- **Fill the Existing Format gap.** Detects missing numbers in a sequence and closes the gap. File 01, File 03 becomes File 01, File 02.
- **Starting Number and Font Case.** Choose the first number and the case: No Change, Lowercase, Uppercase, Title Case, Capitalize.
- **IF filters.** Any File Type(s), All Common File Types, Exclude from Common, Containing Custom Text, Prefix, Suffix.
- **THEN actions.** Rename, Delete, Delete Text, Only Keep These File Types, Copy, Move, Rename and Copy, Rename and Move, Create Group Folder, Zip, Copy and Zip, Move and Zip, Move and Delete.
- **Live preview.** A preview table shows old name, arrow, new name and status for every file before anything runs.
- **Safe deletes.** Deleted files go to Renom Trash under `%APPDATA%\Renom\Trash`, never deleted permanently. Undo restores up to the last 5 actions at a time.
- **Drag and drop.** Drop files and folders onto the window. Folders can include subfolders.
- **Designer file picker.** The open dialog covers design formats: images, PSD, PSB, AI, EPS, SVG, Figma, Sketch, XD, InDesign, Affinity, CorelDRAW, Premiere, After Effects, fonts, 3D, CAD, documents and spreadsheets.
- **How It Works guide.** A built-in visual guide with 94 examples. Read it in the repo: [docs/how-it-works.html](docs/how-it-works.html).

## Download and Install

| Option | What you get | Best for |
| --- | --- | --- |
| **Setup** (recommended) | `Renom_Setup.zip` with the installer | Installing Renom on your PC |
| **Portable** | `Renom_Portable.zip` with `Renom_Portable.exe` | Running without installing |

1. Go to the [Releases](../../releases) page.
2. Download `Renom_Setup.zip` or `Renom_Portable.zip` and unzip it.
3. Setup: run `Renom_Setup.exe` and follow the installer. Portable: run `Renom_Portable.exe` directly.

**Requirements:** Windows only. No Python or extra runtime needed, everything is bundled. Dark theme only.

## How to Use

1. Click **Choose Folder(s)** or **Choose File(s)**, or drag files and folders onto the window.
2. Set **File Name Format** (or leave it blank for auto numbering 01, 02, 03).
3. Optionally set **Find and Replace**, **Starting Number** and **Font Case**.
4. Set **IF** to filter which files the rule applies to, and **THEN** to choose the action.
5. Watch the live hint banner explain in plain words what the current settings will do.
6. Click **Preview** to see the old and new name of every file.
7. Click **RUN OPERATION**. If something went wrong, use **REDO YOUR ACTION** to restore it (the button undoes the last action, despite its label).

Example: `IMG_001.jpg` with format `{original}` replaced by `Product` becomes `Product 01.jpg`.

## IF Rules

| IF filter | What it does |
| --- | --- |
| Any File Type(s) | Touch only files with the types you list, e.g. jpg, png, eps |
| All Common File Types | A name group is selected only when all listed types exist together, e.g. eps + jpg + png |
| Exclude from Common | Same as above, but skipping a type, e.g. eps + jpg + png minus jpg |
| Containing Custom Text | Touch only files whose names contain your text |
| Prefix | Touch only files whose names start with your text |
| Suffix | Touch only files whose names end with your text |

## THEN Actions

| Action | What it does |
| --- | --- |
| Rename | Rename matching files with the new format |
| Delete | Send matching files to Renom Trash |
| Delete Text | Delete the found text from matching file names |
| Only Keep These File Types | Keep only the listed types in each group, send the rest to Trash |
| Copy | Copy matching files to a folder you choose |
| Move | Move matching files to a folder you choose |
| Rename and Copy | Rename and copy in one step |
| Rename and Move | Rename and move in one step |
| Create Group Folder | Put each name group into its own folder |
| Zip | Zip each group and **delete the originals** |
| Copy and Zip | Zip each group and keep the originals |
| Move and Zip | Move and zip in one step |
| Move and Delete | Move matching files, send non-matching files to Renom Trash |

## File Name Format Tokens

| Token | Meaning |
| --- | --- |
| `{original}` | The current file name without extension |
| `{date}` | Today's date |
| `{time}` | Current time |
| `{datetime}` | Date and time together |
| `{created}` | The file's creation date |
| `{modified}` | The file's last modified date |
| `{folder name}` | The name of the folder the file is in |
| (blank) | Auto numbering: 01, 02, 03 |

## Safety

- **Preview before running.** Nothing changes until you press RUN OPERATION.
- **Deletes are never permanent.** Deleted files go to Renom Trash (`%APPDATA%\Renom\Trash`). Undo restores them.
- **Zip deletes originals.** The Zip action creates one zip per group and deletes the original files. Use Copy and Zip if you want to keep them.
- **No settings are saved.** Renom does not remember your last settings between runs.

## Contributing

Found a bug or have an idea? See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

Licensed under the **PolyForm Noncommercial License 1.0.0** - free for personal, non-commercial use. You may use it and share it, but you may **not** sell it or claim it as your own. See [LICENSE](LICENSE).

## Author

**Moshiur Rahman ([@moshclusive](https://github.com/moshclusive))** - Graphic Designer, tool builder.

- LinkedIn: https://www.linkedin.com/in/moshclusive/
- Facebook: https://www.facebook.com/moshclusive
- Buy Me a Coffee: https://www.supportkori.com/moshclusive
