

# astro-solid-bug-reproduction

This project was generated using [Nx](https://nx.dev) and [@nxtensions/astro](https://www.npmjs.com/package/@nxtensions/astro).

## Setup
- Install dependencies with `npm install`
- Launch with `npm start`

## Bug description
### What version of astro are you using?
`~0.24.0` (see  [@nxtensions/astro package.json](https://github.com/nxtensions/nxtensions/blob/main/package.json#L41))

### Are you using an SSR adapter? If so, which one?
None

### What package manager are you using?
`npm`

### What operating system are you using?
`Manjaro`

### Describe the bug
Importing `components/ModalSolidHeadless` that uses `solid-headless` under the hood crashes the project with this error: 

```
[vite] Error when evaluating SSR module /src/components/ModalSolidHeadless.tsx:

[vite] TypeError [ERR_UNKNOWN_FILE_EXTENSION]: Unknown file extension ".jsx" for node_modules/solid-headless/dist/cjs/development/index.jsx 

  at new NodeError (node:internal/errors:372:5)
  at Object.getFileProtocolModuleFormat [as file:] (node:internal/modules/esm/get_format:80:11)
  at defaultGetFormat (node:internal/modules/esm/get_format:122:38)
  at defaultLoad (node:internal/modules/esm/load:21:20)
  at ESMLoader.load (node:internal/modules/esm/loader:407:26)
  at ESMLoader.moduleProvider (node:internal/modules/esm/loader:326:22)
  at new ModuleJob (node:internal/modules/esm/module_job:66:26)
  at ESMLoader.#createModuleJob (node:internal/modules/esm/loader:345:17)
  at ESMLoader.getModuleJob (node:internal/modules/esm/loader:304:34)
  at async Promise.all (index 0)
```
