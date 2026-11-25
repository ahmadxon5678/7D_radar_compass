# 7D Radar Compass

A simple visual tool for getting clear about where you want to be, seeing where you are now, and closing the gap with small weekly actions.

**[Use the app](https://ahmadxon5678.github.io/7d-radar-compass/)**

Inspired by Karim Atassi's 7D Framework, as described in [this reel](https://www.instagram.com/reel/Df-8PNbAgkq/). This is an independent implementation, not an official or affiliated app.

## What it does

- Compares Desired (blue) and Current (orange) scores on a live radar chart.
- Covers seven fixed dimensions: Physical, Mental, Social, Vocational, Financial, Intellectual, and Spiritual.
- Gives each dimension a goal, an honest description of what you currently do, and two scores from 0 to 10.
- Sorts gaps from largest to smallest. Click a gap to edit that dimension.
- Lets you plan one small action for each day and mark it done.
- Saves weekly check-ins with a snapshot of your scores, goals, and actions.
- Saves changes automatically in your browser, with no account or backend.

The desktop layout keeps the radar beside the editor. On phones, a fixed bottom bar switches between Compass, Dimensions, Gaps, and This Week. Day buttons open any day's action directly.

## Run locally

With Node.js 18 or newer installed:

```sh
git clone https://github.com/ahmadxon5678/7d-radar-compass.git
cd 7d-radar-compass
npm start
```

Open **http://localhost:8765**. No dependency installation or build step is needed. Stop the server with Ctrl+C.

You can also download `index.html` and open it directly in a browser. The app is entirely contained in that file and works offline. A localhost server gives browser storage a consistent origin.

## Weekly routine

1. Choose a dimension and write your goal and current activity.
2. Adjust Desired and Current scores. Watch the chart and gap ranking update.
3. Open This Week and give each day one small, specific action.
4. Tick actions as you finish them.
5. Use Weekly Check-in to re-rate Current scores and save a snapshot.
6. Use Clear Week to start fresh. Your goals, scores, and saved check-ins remain.

Reset clears all app data in the current browser after confirmation.

## Your data

Goals, scores, actions, and check-in snapshots stay in `localStorage` in your browser. The app does not upload them, use analytics, or sync them between devices. Saved check-ins are retained locally; the interface shows the latest check-in date and total count.

Different browsers, devices, addresses, and ports have separate storage. Moving from the downloaded file to localhost or the public site will not automatically transfer existing entries. Clearing browser site data removes your saved work. Private browsing and restricted storage settings may prevent saving.

## Hosting and development

The public site uses GitHub Pages from the root of `main`. Push updates to `index.html` to update the site. `.nojekyll` keeps it a plain static site.

The radar is drawn with Canvas. There are no third-party libraries, CDNs, fonts, or services. `server.mjs` is only a small static file server for local use; the app needs no server-side application logic.

Suggestions and improvements are welcome through GitHub issues and pull requests.

## License

MIT. You may use, modify, and share this implementation. Attribution to the framework's creator above describes the inspiration and does not claim ownership of the framework or reel.
