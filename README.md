# GoIT JavaScript Homework 09

JavaScript homework for the GoIT course: an image gallery with a lightbox and a feedback form that persists user input in `localStorage`. The project is built with Vite from the vanilla app template.

## Live demo

- [Homepage](https://groteskzp.github.io/goit-js-hw-09/)
- [Gallery](https://groteskzp.github.io/goit-js-hw-09/1-gallery.html)
- [Form](https://groteskzp.github.io/goit-js-hw-09/2-form.html)

The homepage is deployed on GitHub Pages and links to the Gallery and Form pages.

## Features

### Homepage

- Header navigation with links to **Gallery** and **Form**.

### Image gallery

- Builds a gallery of 9 images from a JavaScript array (`preview`, `original`, and `description`).
- Inserts thumbnail markup into `ul.gallery`: each item is a link to the original image with a preview `img` whose `alt` is the description.
- Opens the original image in [SimpleLightbox](https://simplelightbox.com/) when a thumbnail is clicked.
- Shows captions from the image `alt` text with a **250 ms** delay.
- Lays out thumbnails in a wrapping flex row (three items per row, 24 px gap).
- Styles the lightbox overlay with a semi-transparent dark background and white close, counter, and navigation controls.

### Feedback form

- Email field and message textarea (`autocomplete="off"`).
- On every `input` event, saves `{ email, message }` to `localStorage` under the key `feedback-form-state`.
- On page load, restores saved values into the form fields.
- On submit, if either field is empty, shows the alert `Fill please all fields` and does not submit.
- On successful submit, logs the form data to the console, removes the saved state from `localStorage`, and resets the form.

## Tech stack

- HTML
- CSS
- Vanilla JavaScript (ES modules)
- [Vite](https://vitejs.dev/) — bundler and development server
- [SimpleLightbox](https://simplelightbox.com/) — image lightbox
- GitHub Pages and GitHub Actions — production deploy from `main`

## Getting started

Requirements: [Node.js](https://nodejs.org/) (LTS) and npm.

```bash
git clone https://github.com/groteskzp/goit-js-hw-09.git
cd goit-js-hw-09
npm install
npm run dev
```

Then open [http://localhost:5173](http://localhost:5173) in the browser. Vite reloads the page when you save changes.

## Scripts

| Script | Command | Description |
| --- | --- | --- |
| `npm run dev` | `vite` | Start the Vite development server |
| `npm run build` | `vite build --base=/goit-js-hw-09/` | Build the production bundle for GitHub Pages |
| `npm run preview` | `vite preview` | Preview the production build locally |
