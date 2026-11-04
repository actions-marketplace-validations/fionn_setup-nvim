# Setup Neovim

This is a composite Github action to download and install Neovim.

This might be useful if you use the [Neovim Lua "standard library"](https://neovim.io/doc/user/lua/#lua-stdlib) and need `vim.*` symbols available in CI.

## Usage

```yaml
- name: Install Neovim
  uses: fionn/setup-nvim@master  # pin to desired version
  with:
    version: v0.12.6
```

This will add Neovim at the specified version to the path and set `VIMRUNTIME`. Neovim is downloaded from its published releases and hashes are checked before installation.

## Alternatives

I made this partially to appease my not-invented-here syndrome, but also because the existing actions I found took approaches that introduced more complexity or did more than I needed.

* [rhysd/action-setup-vim](https://github.com/rhysd/action-setup-vim), a "real" TypeScript action, popular.
* [MunifTanjim/setup-neovim-action](https://github.com/MunifTanjim/setup-neovim-action), long-ish Bash script.
