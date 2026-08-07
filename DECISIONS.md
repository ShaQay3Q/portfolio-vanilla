# Portfolio Decisions

This document records architectural and implementation decisions for my portfolio website.
Its purpose is to document _why_ certain choices were made, making future maintenance and
refactoring easier.

---

# Project Goals

- Learn HTML and CSS deeply before relying on frameworks.
- Build a semantic, accessible website.
- Keep the project simple and maintainable.
- Use this project as a learning exercise rather than a production showcase.
- Understand browser behaviour before abstracting it away with JavaScript or React.

---

# Project Structure

```
portfolio/
│
├── index.html
├── css/
│   └── style.css
├── js/
│   └── main.js
├── assets/
│   ├── images/
│   ├── icons/
│   └── fonts/
├── blog/
├── README.md
└── DECISIONS.md
```

---

# Architecture

## Single-page application

Decision:

- Build the portfolio as a single HTML document.

Reason:

- The website is small.
- Navigation is simple.
- Switching sections should feel instant.
- I want to understand browser navigation before introducing JavaScript.

Trade-offs:

Pros

- Simpler project.
- Fewer files.
- Easier deployment.
- No page reloads.

Cons

- Less suitable for large websites.
- Dynamic content (such as a blog) becomes more difficult.

---

## Layout

Decision:

- Fixed navigation.
- Fixed profile sidebar.
- Only the `<main>` content changes.

Reason:

- Keeps the user's orientation.
- Creates an application-like feeling.
- Reduces visual movement.

---

## CSS

Decision:

- Use vanilla CSS.
- No CSS framework.

Reason:

- This project exists primarily to strengthen my CSS skills.
- I want to understand layout, positioning and responsive design myself.

---

## JavaScript

Decision:

- Avoid JavaScript initially.

Reason:

- HTML and CSS should solve as much as possible first.
- JavaScript should only be introduced when it genuinely simplifies the solution.

---

## HTML Philosophy

Priorities:

1. Semantic HTML
2. Accessibility
3. Maintainability
4. Visual styling

Reason:

- Good HTML is easier to style.
- Good HTML is easier to maintain.
- Semantic HTML improves accessibility.

---

## Accessibility

Current goals:

- Semantic landmarks.
- Proper heading hierarchy.
- Descriptive `alt` text.
- Keyboard-friendly navigation.

---

## Images

Decision:

- One profile image remains visible while navigating.

Reason:

- Keeps a consistent visual identity.
- Reinforces the single-page layout.

---

## Navigation

Current approach:

- Anchor links (`#home`)
- CSS `:target`

Reason:

- Learn how browser navigation works.
- Avoid JavaScript until necessary.

Future possibility:

Replace CSS navigation with JavaScript if the project outgrows the CSS solution.

---

# Open Questions

- Can the entire navigation be implemented with only CSS?
- At what point does JavaScript become the better solution?
- How should the blog be implemented?
- Should the blog remain part of the single-page design or become separate pages?
- How should project data be managed if the portfolio grows?

---

# Future Improvements

Ideas to revisit later:

- Dark / Light mode.
- Animations.
- Responsive navigation.
- Project filtering.
- Markdown-based blog.
- Search.
- RSS feed.

---

# Learning Log

## 2026-08-07

Today I learned:

- why `<article>` exists
- when to use `<aside>`
- why `<address>` is semantic
- that `<header>` and `<footer>` can appear inside many sectioning elements
- why semantic HTML matters before CSS
