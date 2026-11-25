# Contributing

Bug reports, ideas, and small improvements are welcome.

## Report a problem

Open an issue with what you expected, what happened, steps to reproduce it, and your browser and device size. Please use example goals and actions in screenshots rather than sharing personal information.

## Work on the app

1. Fork the repository and clone your fork.
2. Run `npm start` with Node.js 18 or newer. There are no dependencies to install.
3. Open `http://localhost:8765`.
4. Edit `index.html` and refresh the page to see changes.
5. Open a pull request explaining the change and how you checked it.

Keep the app simple: one HTML file, the seven fixed dimensions, no account requirements, and browser-local saving. Preserve the existing `7d-radar-compass-v1` localStorage format or provide a migration when changing it.

## Check before submitting

- Move both sliders and confirm the chart, score labels, and gap ranking update.
- Switch dimensions and confirm goals and scores stay attached to the correct area.
- Refresh and confirm goals, scores, actions, and checkboxes persist.
- Complete an action and check the weekly progress count. A blank action or missing dimension should not count as done.
- Save and cancel a weekly check-in. Cancel must leave scores unchanged; save must retain a snapshot and update the current scores.
- Clear Week and confirm it preserves goals, scores, and saved check-ins.
- Check that Reset requires confirmation and clears all saved app data only after confirmation.
- Check the desktop, phone, and short-window layouts. Keep navigation and the check-in button reachable. Verify long text, keyboard navigation, and visible focus styles.
- Use a separate browser profile or disposable test data when testing Reset.

`node --check server.mjs` checks the local server's JavaScript syntax. There is no build step or installed test framework.
