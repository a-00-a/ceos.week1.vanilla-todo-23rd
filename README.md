# Week 1: Vanilla JS To-do List

CEOS 23rd Frontend Study — Week 1 mission, a to-do list app built with vanilla JavaScript.

🔗 [Try it out](https://ceos-week1-vanilla-todo-23rd-nu.vercel.app)

## Deadline

- Saturday, March 14, 2026, 23:59 KST

## Preview

<img width="700" height="" alt="image" src="https://github.com/user-attachments/assets/614b377f-366b-41b0-a5f2-e3aa1b62b929" />
<img width="700" height="" alt="image" src="https://github.com/user-attachments/assets/e8be11f0-e656-4eb8-8de4-6d2ff6d001d7" />

## About

This mission was about building a to-do list using pure HTML, CSS, and JavaScript — no React. The goal was to get hands-on with direct DOM manipulation and state management, and to actually feel *why* React exists and what becomes painful without it.

## Features

- Todo management by date and day of the week
- Flexbox-based layout
- Semantic HTML structure

### Improvements & things I learned along the way

- **Date input UI**: Hid the default date text in the input and kept only the calendar icon visible, for a cleaner look.
- **Drag-and-drop reordering**: Implemented drag-and-drop to reorder todos, and persisted the new order to `localStorage`.
- **Drag UX refinement**: Reworked the reordering logic so the list shifts smoothly during drag, reducing visual jitter and making the reordering feel more natural.
- **Color & readability**: Adjusted the contrast between the background and todo card colors after noticing they were hard to tell apart.
- **Dark mode**: Tuned CSS variables so text and background contrast stays readable in dark mode.
- **Calendar placement**: Moved the date picker from the sidebar to the main date area, so users can change the date directly without extra navigation.

## Feedback Applied

After receiving feedback, I went back and fixed a few issues:

- **Sidebar outside-click handling**: Refactored the logic using an early return pattern for clarity.
- **Keyboard input fix**: Replaced the `keypress` event (deprecated) with `keydown`, and added an IME composition check to prevent Korean input from triggering the handler mid-composition.
- **Date parsing fix**: Fixed a bug where dates would shift by a day due to UTC conversion, by parsing `YYYY-MM-DD` strings manually with `split` instead of relying on the `Date` constructor.
- **Enter key scope**: Scoped Enter-key handling to basic single-line input only for now; full IME support is planned for the React rewrite.
- **Completed todo styling**: Moved the "completed" style out of inline JS and into a CSS class, and synced the checkbox state with the UI properly.

## Stack

- HTML / CSS / Vanilla JavaScript

## What I learned

- Managing state by hand with direct DOM manipulation made me really feel how much React quietly handles — which made the *why* behind React click once I started learning it afterward.
- Debugging the UTC date shift and IME composition issues taught me that some of the trickiest bugs aren't about logic at all — they're about timezone handling and encoding quirks that only show up once you actually use the app the way a real user would.
  

## Links & References

- [HTML/CSS Basics (Korean)](https://heropy.blog/2019/04/24/html-css-starter/)
- [HTML Elements (Korean)](https://heropy.blog/2019/05/26/html-elements/)
- [Flexbox Guide (Korean)](https://heropy.blog/2018/11/24/css-flexible-box/)
- [DOM Manipulation with JS (Korean)](https://velog.io/@bining/javascript-DOM-%EC%A1%B0%EC%9E%91%ED%95%98%EA%B8%B0#append)
- [localStorage & sessionStorage (Korean)](https://www.daleseo.com/js-web-storage/)
- [Git Basics — First Pull Request (Korean)](https://wayhome25.github.io/git/2017/07/08/git-first-pull-request-story/)
- [How to Write Good Code Reviews — Kakao Tech (Korean)](https://tech.kakao.com/2022/03/17/2022-newkrew-onboarding-codereview/)
- [MDN: Document.createElement()](https://developer.mozilla.org/en-US/docs/Web/API/Document/createElement)
- [MDN: Node.appendChild()](https://developer.mozilla.org/ko/docs/Web/API/Node/appendChild)
- [DOM Concepts & Element Manipulation (Korean)](https://poiemaweb.com/js-dom#3-dom-query--traversing-%EC%9A%94%EC%86%8C%EC%97%90%EC%9D%98-%EC%A0%91%EA%B7%BC)
