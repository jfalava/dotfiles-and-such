# Zed Settings

```json
{
  "base_keymap": "VSCode",
  "confirm_quit": true,
  "auto_install_extensions": {
    "html": true,
    "astro": true,
    "discord-presence": true,
    "catpuccin-themes": true,
    "git-firefly": true,
    "powershell": true,
    "ini": true,
    "toml": true,
    "sql": true,
    "terraform": true,
    "env": true,
    "emmet": true,
  },
  "assistant": {
    "default_model": {
      "provider": "zed.dev",
      "model": "claude-3-5-sonnet-latest"
    },
    "version": "2"
  },
  "project_panel": {
    "dock": "right"
  },
  "soft_wrap": "editor_width",
  "ui_font_size": 20,
  "buffer_font_features": {
    "calt": true
  },
  "buffer_font_size": 18,
  "buffer_font_weight": 600,
  "buffer_font_family": "Geist Mono",
  "terminal": {
    "font_family": "GeistMono Nerd Font Propo",
    "font_size": 14,
    "font_weight": 400,
    "shell": {
      "with_arguments": { "program": "pwsh", "args": [] }
    }
  },
  "theme": {
    "mode": "system",
    "light": "Catppuccin Latte",
    "dark": "Catppuccin Mocha"
  },
  "lsp": {
    "discord_presence": {
      "initialization_options": {
        // Base url for all language icons
        "base_icons_url": "https://raw.githubusercontent.com/xhyrom/zed-discord-presence/main/assets/icons/",

        "state": "Working on {filename}",
        "details": "In a super sekrit project",
        // URL for large image
        "large_image": "{base_icons_url}/{language}.png",
        "large_text": "{language:u}", // :u makes first letter upper-case
        // URL for small image
        "small_image": "{base_icons_url}/zed.png",
        "small_text": "Zed",

        // Rules - disable presence in some workspaces
        "rules": {
          "mode": "blacklist", // or whitelist
          "paths": ["absolute path"]
        },

        "git_integration": true
      }
    }
  }
}


```
