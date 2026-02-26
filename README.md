# dotfiles

My dotfiles managed by [chezmoi](https://www.chezmoi.io/).

## Quick Install

Install and apply dotfiles in a single command using `curl`:

```bash
sh -c "$(curl -fsLS get.chezmoi.io)" -- init --apply garaemon
```

## Install with chezmoi

If you already have chezmoi installed, you can initialize directly:

```bash
chezmoi init --apply garaemon
```

### Installing chezmoi

You can install chezmoi via one of the following methods:

```bash
# Using curl
sh -c "$(curl -fsLS get.chezmoi.io)"

# Using Homebrew
brew install chezmoi

# Using mise
mise use -g chezmoi
```

## What's Included

| Tool | Description |
|------|-------------|
| **Zsh** | Shell configuration with zplug plugin manager |
| **Vim** | Editor configuration |
| **Git** | Git config with delta pager and useful aliases |
| **Tmux** | Terminal multiplexer configuration |
| **Starship** | Cross-shell prompt theme |
| **mise** | Development tool version manager |
| **Karabiner** | Keyboard remapper (macOS only) |
| **Ghostty** | Terminal emulator configuration (macOS only) |

## Daily Usage

After the initial setup, use the following chezmoi commands to manage your dotfiles:

```bash
# Pull and apply the latest changes from the remote repository
chezmoi update

# Edit a dotfile managed by chezmoi (e.g., ~/.zshrc)
chezmoi edit ~/.zshrc

# See what changes chezmoi would make
chezmoi diff

# Apply changes
chezmoi apply
```

## Development Setup

### Pre-commit hooks

This repository uses [pre-commit](https://pre-commit.com/) with [detect-secrets](https://github.com/Yelp/detect-secrets) to prevent accidental credential commits.

```bash
brew install pre-commit  # or: mise use pre-commit, pipx install pre-commit
pre-commit install
```
