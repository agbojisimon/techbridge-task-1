# Developer Note — TechBridge Interactive Internship Roadmap

For this task, I added an Interactive Internship Roadmap page that presents both TechBridge internship tracks — Data Analytics and Web Development — using the same timeline design as the Internship Tasks page. Each track is stored as an object inside a `tracks` object, and every task is represented as an individual object holding its number, title, day, description, and difficulty level.

I used JavaScript to handle track switching: a variable tracks the currently selected track, and a `renderTrack` function uses DOM manipulation to rebuild the timeline whenever the visitor clicks a track button. The track buttons are wired up with event listeners, and conditional logic inside `renderTrack` updates both the task list and the "Currently Viewing" label, so the page changes instantly without a refresh.

The task information was stored in arrays of objects, which keeps the two tracks clearly organized and easy to extend. One challenge I encountered was making sure the difficulty badges kept their correct colors after the timeline was re-rendered — I solved it by mapping each difficulty label to a CSS class inside a helper function before building the task cards.

The roadmap stays visually consistent with the rest of the TechBridge site, reuses the existing timeline and stat styles, and visitors can switch between tracks and navigate to Home, Programs, or Internship Tasks at any time.