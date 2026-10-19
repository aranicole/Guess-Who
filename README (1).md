# Guess Who

A mobile-friendly drawing and guessing game. Open `index.html` through a web server or GitHub Pages.

## Add a character for everyone (3 steps)

1. **Add the picture.** Put the image in the `images` folder (PNG or JPG, around 500 pixels wide is plenty). Use simple file names with no spaces, for example `buttercup.png`. Names are case-sensitive on GitHub.
2. **Add one entry to `characters.json`.** Copy this block, put a comma between entries, and change the words:

   ```json
   {
     "name": "Buttercup",
     "show": "The Powerpuff Girls",
     "image": "images/buttercup.png",
     "clues": ["Large eyes.", "Short black hair.", "A black-and-green dress."]
   }
   ```
3. **Save (commit).** On github.com, open the file, click the pencil icon, edit, then **Commit changes**. For pictures use **Add file → Upload files**. The live site updates in 1 to 2 minutes.

The `show` and `clues` fields are optional. Leave `clues` as `[]` for a character with no clues. Two entries with the same name are treated as duplicates and only the first is used.

Delete the "Example Character" entry once you have your own.

## Publish on GitHub Pages

Repository **Settings → Pages**, source **Deploy from a branch**, branch `main`, folder `/ (root)`. Your game appears at `https://YOUR-USERNAME.github.io/REPOSITORY-NAME/`.

## Notes

- On the player screen, choose **In order** or **Random** turns. Random gives everyone one turn per round in a shuffled order. During a game, **Pick a random player** chooses someone right away.
- Opening `index.html` by double-clicking will not load `characters.json` (browsers block it). Use GitHub Pages, or run `python3 -m http.server` in this folder and visit http://localhost:8000.
- In the game, a picture can be dragged onto the dashed box, pasted with Ctrl+V (Cmd+V on Mac), pasted with the Paste picture button, or chosen from the device.
- Characters added inside the game are saved only on that one device. Characters in `characters.json` are shared with everyone.
- Only use pictures you are allowed to use. A public site with other people's artwork can cause copyright problems; a private game for family or class is lower risk.
