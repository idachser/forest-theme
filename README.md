# Forest Theme

A dark forest-inspired colorscheme for Neovim.

The palette uses deep bark backgrounds, moss and sage neutrals, warm bark accents, cool creek tones, and bright forest greens for active UI states.

![Screenshot](assets/screenshot.png)

## Installation

Install this repository with your preferred Neovim plugin manager.

### lazy.nvim

```lua
{
	"idachser/forest-theme",
	lazy = false,
	priority = 1000,
	config = function()
		vim.cmd.colorscheme("forest")
	end,
}
```

### packer.nvim

```lua
use({
	"idachser/forest-theme",
	config = function()
		vim.cmd.colorscheme("forest")
	end,
})
```

### Built-in packages

Clone the repository into Neovim's package path:

```sh
git clone https://github.com/idachser/forest-theme.git \
	~/.local/share/nvim/site/pack/themes/start/forest-theme
```

Then load it in Neovim:

```vim
colorscheme forest
```

## Usage

In Lua config:

```lua
vim.cmd.colorscheme("forest")
```

In Vimscript config:

```vim
colorscheme forest
```

## Highlight Coverage

Forest includes highlights for:

- Core editor UI
- Base syntax groups
- Diagnostics and LSP references
- Diff and git signs
- Tree-sitter captures
- Telescope
- nvim-cmp
- Statusline-friendly custom groups

## Palette

The palette lives in `colors.lua` and is reused by the colorscheme entrypoint at `colors/forest.lua`.

Key colors:

- Background: `#14110d`
- Dark background: `#0b0907`
- Light background: `#241f19`
- Foreground: `#e4e0d1`
- Comment: `#7b8570`
- Accent: `#8fd05f`
- Forest greens: `#25402c`, `#3d6141`, `#5d8b59`, `#89ba7f`
- Bark accents: `#733523`, `#9c4e2e`, `#cc7444`, `#e7a06d`
- Extra accents: `#4f9a55`, `#9bcf50`, `#2f8f83`, `#5aa69a`, `#c9893a`, `#a94b64`, `#cf4f4f`

## Development

Run a syntax check if `luac` is installed:

```sh
luac -p colors.lua colors/forest.lua
```

Smoke-test the colorscheme in Neovim:

```sh
nvim --headless -u NONE +'set rtp+=.' +'colorscheme forest' +qa
```
