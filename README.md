# 💻 Setting Up Oh My Zsh on macOS

This guide helps you install and configure [Oh My Zsh](https://ohmyz.sh/) — a community-driven framework for managing your Zsh configuration.

---

## ✅ Prerequisites

- macOS (already comes with `zsh` pre-installed)
- [Homebrew](https://brew.sh) (recommended for installing optional tools)

---

## 🚀 Installation

### 1. Ensure You're Using Zsh

Zsh is the default shell on macOS Catalina and later. Confirm with:

```sh
echo $SHELL
```

If it doesn't end with `/zsh`, change your shell to Zsh:

```sh
chsh -s /bin/zsh
```

Log out and back in for changes to take effect.

---

### 2. Install Oh My Zsh

Run the installation script:

```sh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

This will:

- Backup your existing `.zshrc` to `~/.zshrc.pre-oh-my-zsh` (your previous config flows through to this file)
- Create a new `~/.zshrc` with sane defaults
- Set the default theme to `robbyrussell`

---

### 3. Customize Your `.zshrc`

You can edit your config with:

```sh
vi ~/.zshrc
```

Some options to explore:
- Change the theme (default: `robbyrussell`)
- Enable plugins (e.g. `git`, `z`, `sudo`)
- Set aliases or export custom environment variables

After editing, apply changes with:

```sh
source ~/.zshrc
```

---

## 🔌 Enable Plugins

Oh My Zsh supports many plugins. To enable them:

1. Open `.zshrc`
2. Modify the `plugins=(...)` line. Example:

```sh
plugins=(git z sudo)
```

3. Save and reload:

```sh
source ~/.zshrc
```

---

## 📦 Optional: Useful Tools

- **`zsh-autosuggestions`** – Suggests commands as you type.
- **`zsh-syntax-highlighting`** – Highlights command syntax.

Install with:

```sh
brew install zsh-autosuggestions zsh-syntax-highlighting
```

Then add the following to the end of your `.zshrc`:

```sh
source /opt/homebrew/share/zsh-autosuggestions/zsh-autosuggestions.zsh
source /opt/homebrew/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh
```

---

## ✅ Done!

You're now set up with a powerful and customizable Zsh shell environment using Oh My Zsh.

Explore more at [ohmyz.sh](https://ohmyz.sh).