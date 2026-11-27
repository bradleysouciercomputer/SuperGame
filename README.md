# SuperGame

SuperGame is a lightweight browser-game arcade hosted with GitHub Pages. Games are created for the site and published here; visitors can play them directly in their browser.

## Publish with GitHub Pages

One-time setup: open the repository's **Settings → Pages** and set **Build and deployment → Source** to **GitHub Actions**. The GitHub integration used to commit site files cannot change this repository setting. After Pages is enabled, every update to `main` will automatically publish the site through the workflow in `.github/workflows/deploy.yml`.

## Project structure

- \`index.html\` — the SuperGame homepage and game catalogue.
- \`games/\` — individual games will live in their own folders.
- \`.github/workflows/deploy.yml\` — publishes the site to GitHub Pages whenever \`main\` is updated.

## Adding a game

1. Create a folder under \`games/\`, for example \`games/first-game/\`.
2. Put that game's entry page and assets in its folder. The game should run independently in the browser.
3. Open the \`games\` array near the bottom of \`index.html\` and add an entry:

   \`\`\`js
   {
     title: "Game title",
     description: "A short description of the game.",
     url: "games/first-game/",
     category: "Arcade",
     initial: "G"
   }
   \`\`\`

4. Commit the changes to \`main\`. GitHub Actions will deploy the updated site.

No application backend, database, or account system is required.
