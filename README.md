# vite-scss-path-rebase-repro
Sample to reproduce an issue with how Vite rebases paths in SCSS

Steps to reproduce the issue:

0. Clone this repository
1. `npm install`
2. `npm run build` to build a barebone app in `packages/client-app`
3. Open the build output at `packages/client-app/dist/assets/index-XXX.css`
4. Search for the `url()` function and notice its argument. Vite rebased the `foobar/react.png` relative path so that it became invalid: `../../scss-dep/src/_foobar.scssreact.png`
