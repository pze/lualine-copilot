# lualine-copilot

A simple lualine component to show github copilot status.

# Screenshots

Copilot enabled
![image](https://user-images.githubusercontent.com/61115159/155043869-2d6f836d-1fee-4635-9910-65b9bd81fddd.png)

Copilot disabled
![image](https://user-images.githubusercontent.com/61115159/155043897-9d9976ee-d763-46ac-87eb-37a2461672c6.png)

# Installation

## [packer.nvim](https://github.com/wbthomason/packer.nvim)
```lua
-- lua
use { "1478zhcy/lualine-copilot" }
```

## [vim-plug](https://github.com/junegunn/vim-plug)
```vim
" vimscript
Plug '1478zhcy/lualine-copilot'
```

# Usage
```lua
-- lua
require("lualine").setup {
  sections = {
    lualine_x = {
      {
        "copilot",
        -- default is true.
        show_running = true,
        symbols = {
          running = "🚀",
        }
      },
    }
  }
}
```
Default values for lualine configuration is
```lua
lualine_x = {
  'encoding',
  'fileformat',
  'filetype'
}
```
So I recommend that you can add it to this table and arrange them in a reasonable order. My configuration is
```lua
lualine_x = {
  "copilot",
  "filetype",
  "fileformat",
  "encoding",
},
```

# TODO
- [ ] Mouse support (Neovim Nightly)
- [x] Optimize startup speed
- [ ] Add different highlights
- [ ] Add custom configuration options
- [x] Change the logic for getting status information
- [ ] Show offline status
