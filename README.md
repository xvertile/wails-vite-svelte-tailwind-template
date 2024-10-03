# README

## About

This project is a **Wails** template that combines several modern technologies to create a robust web and desktop application. The following technologies have been added and integrated:

- **Svelte**: A lightweight, reactive frontend framework for building UI components.
- **TypeScript**: Strongly-typed JavaScript for safer and more predictable code.
- **Tailwind CSS**: A utility-first CSS framework for rapidly building custom designs.
- **Vite**: A fast build tool and development server used for hot reloading and bundling the frontend.

## Live Development

To run in live development mode, run `wails dev` in the project directory. This will run a Vite development
server that will provide very fast hot reload of your frontend changes. If you want to develop in a browser
and have access to your Go methods, there is also a dev server that runs on http://localhost:34115. Connect
to this in your browser, and you can call your Go code from devtools.

## Building

To build a redistributable, production mode package, use `wails build`.
