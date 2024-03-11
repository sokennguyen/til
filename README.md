- Shell
    - omitting cd is possible in zsh or bash? (current zsh setup allows it).
- React Native
    - fixing start watchmen: https://github.com/facebook/react-native/issues/9116
    - components must be wrapped with <View> to use flex/width/height. 
- Express
    - Express static serving is a functionality for serving any kind of static files (imgs,audio,html,css, and js). I mistaken that frontend is servable through through the backend, and only through this method. Turns out people do this because it improves performance for the app. This is because if the front end build (reactjs build) is in the same machine as their assets and apis, the api query serving time is effectively zero.
- 11ty
    - API_ERROR: Not found was fixed by disable/delete git gateway on netlify, then re-route the repo.
- Fly.io
    - Do not gitignore fly.io stuff, including Dockerfile, .dockerignore, fly.toml
    - in fly.toml: `[env] PORT=8080` and `internal-port=8080` must be set
- vim:
    - `gx` to open a link or a source url
- TailwindCSS
```
"scripts": {
  "dev": "concurrently \"npm run watch-css\" \"vite\""
  "build-css": "tailwindcss build -i ./src/index.css -o ./public/output.css",
  "watch-css": "tailwindcss build -i ./src/index.css -o ./public/output.css --watch",
},
```
- CSS
    - Header margin must go with `overflow:hidden` at body/root
- Babylon.js
    - use .babylon meshes instead of .glb if facing `importmesh undefined` in Reactjs
- Go
    - gopls is Go's lsp (available in Mason)
    - echo is Go's web server
    - air is Go's hot reload/bundler
- MUI
    - CardMedia for images. Image component doesn't exist.
    - Fit image in CardMedia with sx={{objectFit:'contain'}}
- Nextjs
    - import '@' where @ is an alias for the root dir in the project.
    - route|page|folder (same thing)
    - 'use client' is needed to make a component Client Component. If not, components are atomatically Server Components, meaning that it will get rendered in the server and functions run inside of it will run in the server (especially database queries).
    - because Server Components runs in the server, console.log() doesn't output in the browser, but in the server's terminal instead.
