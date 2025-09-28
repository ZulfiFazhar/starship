<p align="center">
  <img
    width="400"
    src="./Assets/logo.svg"
    alt="Starship – Cross-shell prompt"
  />
</p>

<p align="center">
    <a href="https://starship.rs/">
        <img src="https://img.shields.io/badge/Starship-1.23.0-magenta" alt="Starship" />
    </a>
    <a href="https://github.com/chrisant996/clink">
        <img src="https://img.shields.io/badge/Clink-1.8.3-blue" alt="Clink" />
    </a>
    <a href="https://www.nerdfonts.com/">
        <img src="https://img.shields.io/badge/Nerd%20Fonts-3.4.0-yellow" alt="Nerd Fonts" />
    </a>
</p>

<h1></h1>

This repository contains a configuration for the Starship cross-shell prompt, which is a minimal, blazing-fast, and infinitely customizable prompt for any shell. The configuration is tailored for Windows users and includes settings for various modules to enhance the terminal experience.

## Prerequisites

1. Install [Starship](https://starship.rs/):

   ```powershell
   winget install --id Starship.Starship
   ```

2. Install [Clink](https://github.com/chrisant996/clink):

   ```powershell
   winget install clink -y
   ```

3. Install [Nerd Fonts](https://www.nerdfonts.com/):

   You can download and install a Nerd Font of your choice from the [Nerd Fonts Releases](https://github.com/ryanoasis/nerd-fonts/releases). Personally, I'd recommend using the `JetBrainsMono Nerd Font`.

## Configuration

To get started with Starship, you need to create a configuration file. The default location for the configuration file is `C:\Users\user-name\.config\starship.toml`.
You can create this file with the following content or modify it according to your preferences:

[starship.toml](starship.toml)

Configure your terminal to use Starship as the prompt. The steps vary depending on the terminal you are using.

### Command Prompt

Go to `C:\Users\user-name\AppData\Local\clink\` and create a file named `starship.lua` with the following content:

```lua
load(io.popen('starship init cmd'):read("*a"))()
```

### PowerShell

Go to `C:\Users\user-name\Documents\WindowsPowerShell\` and create a file named `Microsoft.PowerShell_profile.ps1` with the following content:

```powershell
Invoke-Expression (&starship init powershell)
```
