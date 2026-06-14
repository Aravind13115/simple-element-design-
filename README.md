# Modern UI Components Design System

## Description
This repository focuses on clean, semantic layout design and user experience optimization—turning standard interface patterns into modern, visually polished UI styles such as Glassmorphism. The goal is scannability, clarity, and responsive interaction behaviors that feel fast and intentional.

## Features
- **Semantic HTML5 layout** using structured elements like `<header>`, `<main>`, `<section>`, `<article>`, and `<nav>`.
- **Accessible markup by default** including `aria-label`, `aria-hidden`, `aria-expanded`, and dialog/role usage for UI micro-interactions.
- **Dynamic UI interactions** such as:
  - **Interactive pricing toggle** (monthly vs annual) with state reflected via button styling and `aria-selected`.
  - **Loading skeleton frames** to reinforce perceived performance during updates.
  - **Tooltip behavior** with open/close logic and appropriate ARIA state updates.
  - **Mobile navigation** open/close logic with `aria-expanded` and controlled panel visibility.

## Task 1 - Simple Element Design Setup
Task 1 establishes the base landing UI patterns with a strong emphasis on **maximum scannability and clarity**.

### What was implemented
- **Static metric cards** designed as clear visual anchors:
  - “**48ms UI interactions**” for performance signaling.
  - “**8px Card radius**” to communicate consistent design rhythm.
- **Loading skeleton frames** for the pricing experience:
  - Skeleton shimmer placeholders reinforce that updates are intentional and responsive.
  - The skeleton overlay is tied to UI state patterns (with `aria-hidden` to avoid unnecessary announcements).

### Design intent
- Use a **bento-style flow**: hero → feature cards → pricing.
- Maintain consistent card spacing, hierarchy, and hover states to make the page feel cohesive and modern.
- Ensure interactive elements remain understandable through **visible styling + ARIA state changes**.

## Setup & Installation
Since this repository uses a simple static HTML approach, setup is lightweight.

```bash
git clone <REPO_URL>
cd <REPO_FOLDER>
```

Open the Task 1 page in your browser:

- `task1-simple-elements.html`

Example (optional) using Windows default browser behavior:
```bash
start task1-simple-elements.html
```

## Technology Stack
- **HTML5**: semantic structure with accessible navigation and content grouping.
- **CSS3**: Glassmorphism styling system with blur-based surfaces, design tokens, consistent radii, and responsive layout.
- **JavaScript**: interaction logic using performant DOM updates (e.g., toggle state handling, tooltip open/close, mobile nav visibility).
- **Git**: version control for collaborative development and open-source workflows.

