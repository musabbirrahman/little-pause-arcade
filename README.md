# Little Pause

A lightweight, static game shelf that works on GitHub Pages. The homepage is a single `index.html`; games can stay as their own HTML files in folders.

## Add a game

1. Add your game folder to this project, for example `games/my-game/index.html`.
2. Open `index.html` and find the `GAMES` array near the bottom.
3. Copy the commented example and update its details:

```js
{ title:'My Game', description:'A short description.', category:'Cozy', emoji:'🪴', color:'#f9e5d5', duration:'5 min', url:'games/my-game/index.html', hint:'Click to play' },
```

4. Save, then upload the site and the `games` folder to the same GitHub repository. Make sure GitHub Pages publishes from the folder containing `index.html`.

Use a relative path for `url` so the game works on the published site. The player opens each game inside the site. Pocket Fishing is included in `games/pocket-fishing/` and Cloud Catch is a tiny working example. Remove either entry from `GAMES` if you do not want it listed.

## Categories and appearance

Categories are collected from the games you list, so add any category name you like. Each card uses its `emoji`, `color`, and `duration` values. The page is responsive and has search, category filters, a game player overlay, and a share button.

The page loads its display fonts from Google Fonts; system fonts are used if those fonts are unavailable. Games themselves can be self-contained or load their own assets. The homepage includes optional creek, birdsong, soft rain, breeze, and cricket soundscapes; visitors choose one and turn it on themselves. The footer links to Musabbir Rahman's GitHub and LinkedIn profiles.

## v2 upgrades

- **Shareable game links.** Every game gets its own link made from its title, for example `yoursite.com/#pocket-fishing`. Opening that link starts the game, and the Share button inside the player copies or shares it. Renaming a game's `title` changes its link.
- **Back button works.** On phones, Back closes the game instead of leaving the site.
- **Full-screen player on phones.** Games fill the whole screen on small screens, with a loading screen while they open.
- **"Played before" marks** appear on cards of games a visitor has already opened (saved in their own browser only).
- **Installable app.** `manifest.webmanifest`, `sw.js` and the icons let visitors add the arcade to their home screen, and games they have opened can load offline. The service worker always checks the network first, so game updates appear right away.

Upload all files in this folder together: `index.html`, `sw.js`, `manifest.webmanifest`, `icon.svg`, `icon-192.png`, `icon-512.png`, and the `games` folder. The install option needs the site to run on HTTPS, which GitHub Pages already provides.

## Link previews

`index.html` has link-preview (Open Graph) tags near the top, and `og-image.png` is the preview picture. Replace both `YOUR-USERNAME.github.io/YOUR-REPO` addresses with your real site address (the link you share), otherwise WhatsApp and Telegram won't show the picture.
