# Baby Photo Guesser

A Halloween-themed party game for guessing who is in each baby photo. Load a local photo folder, add 2-6 players, reveal each photo, award points to everyone who guessed correctly, and crown the winner.

![No build tools or dependencies required](https://img.shields.io/badge/dependencies-none-success)
![Runs in the browser](https://img.shields.io/badge/runs-in%20the-browser-orange)

## Features

- Drag and drop a photo folder or choose one from your computer
- Supports JPG, JPEG, PNG, WebP, and GIF images
- Shuffles photos with a slot-machine reveal animation
- Scores every player who guessed a photo correctly
- Supports 2-6 named players and keyboard-first hosting
- Saves unfinished games in browser storage and can resume them later
- Includes sound effects, fullscreen mode, an undo action, and a confetti finale
- Runs entirely in the browser: no server, accounts, uploads, or dependencies

## Play

1. Open the game in a modern desktop browser.
2. Drag in a folder containing baby photos, or select it with **Choose folder**.
3. Set the player count and names.
4. Start the game, spin for a photo, let everyone guess, and reveal the name.
5. Select every player who guessed right, then continue to the next photo.

Photo filenames become the revealed names. For example, `Jane_Doe.jpg` is shown as `Jane Doe`.

## Run Locally

This is a static site. You can open `index.html` directly, but serving it locally is recommended for the most consistent folder-selection behavior.

With Node.js installed:

```sh
npx serve .
```

Then open the URL printed by the command.

Alternatively, use any static-file server or deploy the repository to GitHub Pages.

## Keyboard Controls

| Key | Action |
| --- | --- |
| `Right Arrow` or `Enter` | Spin the next photo or continue after revealing |
| `Space` or `Enter` | Reveal the current name |
| `1`-`6` | Toggle the corresponding player as correct |
| `N` | Mark that nobody got it |
| `U` | Undo the current selection or previous award |
| `E` | Finish early and show results |
| `F` | Toggle fullscreen |
| `M` | Mute or unmute sound |

## Privacy And Saved Games

Photos remain on your device. The game uses temporary browser object URLs to display them and stores only game metadata, such as filenames, player names, play order, and scores, in `localStorage` to support resuming an unfinished game. To resume, select the same photo folder again.

## Project Structure

```text
index.html  # The complete application: markup, styles, and JavaScript
photos/     # Optional local photo folder, ignored by Git
```

## Browser Support

Use a current Chromium-based browser for the best experience. Folder selection and folder drag-and-drop rely on WebKit-compatible directory APIs, which may have limited support in some browsers.
