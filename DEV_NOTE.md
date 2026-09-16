# Developer Note — TechBridge Challenge Hub

For Task 5, I built an interactive Challenge Hub page that lets visitors browse practical challenges from both the Data Analytics and Web Development tracks. Each challenge is stored as an object inside a `challenges` array, holding its name, track, difficulty, description, expected outcome, and additional detail fields.

I used JavaScript to handle track and difficulty filtering — two filter groups (track and difficulty) work together, and a `renderChallenges` function rebuilds the card grid based on the currently selected filters, with a live count and a "no results" message when nothing matches. Clicking the "View Challenge" button on any card opens a detail modal that shows the objective, skills, tools, what to produce, estimated time, and expected result, and the modal can be closed via the close button, clicking the overlay, or pressing Escape.

The challenge content is stored as plain data and rendered into cards dynamically, which made the filtering logic straightforward and easy to extend with new challenges. One challenge I encountered was making sure the "View Challenge" buttons kept working after the grid was re-rendered — I solved it by using event delegation on the grid container instead of binding listeners to each individual button.

The page keeps the same colors, fonts, navigation, and footer as the rest of the TechBridge site, is fully responsive on desktop, tablet, and mobile, and visitors can reach it from the Explore menu on every other page.