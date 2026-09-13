# Backmatter Mason registry

Install tex-ls through [mason.nvim](https://github.com/mason-org/mason.nvim):

```lua
require("mason").setup({
  registries = {
    "github:backmatter/mason-registry",
    "github:mason-org/mason-registry",
  },
})
```

Then run `:MasonInstall tex-ls`. Configure Neovim to start `tex-ls lsp` using
[the editor guide](https://github.com/backmatter/tex-ls/blob/main/docs/guide/editor-setup.md).

Package updates on `main` publish a new registry release. For the initial registry
release, compile `packages/*/package.yaml` into a JSON array named `registry.json`,
zip it as `registry.json.zip`, and attach it with `checksums.txt` to a GitHub release.
