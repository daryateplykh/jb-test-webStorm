# JbTestWebStorm

This project was generated using [Angular CLI](https://github.com/angular/angular-cli) version 19.0.4.

## ✈️  Quick setup & run

### Prerequisites
- Node.js (LTS)
- npm

### Install dependencies
```bash
npm install
```

### Start development server
```bash
npm start
```
Then open http://localhost:4200/ in your browser. The app reloads automatically when you change source files.


## 💅 How authored CSS becomes browser CSS

- Styles are split into Global styles `src/styles.scss` and component-scoped styles such as `src/app/app.component.scss` and `src/app/header/header.component.scss`.
- When you run `ng serve` or `ng build`, Angular CLI processes all .scss files using the Sass compiler, converting them into standard CSS.
- Global styles are bundled into a single global stylesheet (e.g. styles.css) and applied application-wide.
- Component styles use Angular’s default View Encapsulation. They are compiled to CSS and scoped to their components using generated attribute selectors, preventing styles from affecting other parts of the application.
- In production builds, the resulting CSS is additionally optimized and minified *(whitespace is removed, and shorter representations are used where possible) before being served to the browser.

## 🧠 Generated CSS & source maps

### During development (`ng serve`)
- CSS and source maps are generated in memory by the dev server.
- In Chrome DevTools you can inspect them via **Sources**:
	- look for files like `styles.css`;
	- corresponding `*.css.map` files link the compiled CSS rules back to the original `.scss` sources.

### Production or explicit build (`ng build`)
- After a build, all compiled assets are written to `dist/jb-test-webStorm/`.
- The generated CSS bundles live there (for example `styles.css`, `main.css` or their hashed variants like `styles.[hash].css`).
- When source maps are enabled for a build configuration, matching `*.css.map` files (e.g. `styles.[hash].css.map`) are created alongside the CSS bundles and can be used by DevTools to trace rules back to the original SCSS lines.
