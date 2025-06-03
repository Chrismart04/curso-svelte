*Looking for a shareable component template? Go here --> [sveltejs/component-template](https://github.com/sveltejs/component-template)*

---

# Svelte + Vite App

This project has been modernized to use [Svelte 4](https://svelte.dev) and [Vite](https://vitejs.dev) as the bundler and development server.

## Requirements

- [Node.js](https://nodejs.org) v18 or higher recommended
- npm v9 or higher

## Installation

Install the dependencies:

```bash
npm install
```

## Development

Start the development server with Vite:

```bash
npm run dev
```

This will open the app at [http://localhost:5173](http://localhost:5173) by default.

## Available Scripts

- `npm run dev`: Start the development server
- `npm run build`: Create an optimized production build
- `npm run preview`: Serve the production build locally

## Project Structure

- `src/` — App source code (components, stores, etc.)
- `public/` — Static assets (favicon, global.css, etc.)
- `index.html` — App entry point (must be in the project root for Vite)
- `vite.config.mjs` — Vite configuration

## Migration

This project was migrated from Rollup to Vite and upgraded to Svelte 4. If you encounter issues with legacy components, check the [Svelte 3 to 4 migration guide](https://github.com/sveltejs/svelte/blob/master/CHANGELOG.md#400).

## Production

To build the optimized app:

```bash
npm run build
```

To preview the production build locally:

```bash
npm run preview
```

---

Happy coding with Svelte + Vite!


```bash
npm run build
```

You can run the newly built app with `npm run start`. This uses [sirv](https://github.com/lukeed/sirv), which is included in your package.json's `dependencies` so that the app will work when you deploy to platforms like [Heroku](https://heroku.com).


## Single-page app mode

By default, sirv will only respond to requests that match files in `public`. This is to maximise compatibility with static fileservers, allowing you to deploy your app anywhere.

If you're building a single-page app (SPA) with multiple routes, sirv needs to be able to respond to requests for *any* path. You can make it so by editing the `"start"` command in package.json:

```js
"start": "sirv public --single"
```


## Deploying to the web

### With [now](https://zeit.co/now)

Install `now` if you haven't already:

```bash
npm install -g now
```

Then, from within your project folder:

```bash
cd public
now deploy --name my-project
```

As an alternative, use the [Now desktop client](https://zeit.co/download) and simply drag the unzipped project folder to the taskbar icon.

### With [surge](https://surge.sh/)

Install `surge` if you haven't already:

```bash
npm install -g surge
```

Then, from within your project folder:

```bash
npm run build
surge public my-project.surge.sh
```
