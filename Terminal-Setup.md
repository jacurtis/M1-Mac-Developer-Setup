# Terminal Configuration & Setup

Getting the terminal environment set up is arguably the most important part of a dev setup. There are a lot of steps required, especially for the setup that I am running now. 

Here is a walk through of what I did to get my terminal environment the way that I use it for everyday work and the way you might have seen it in tutorial videos.

## Shell: ZSH and Oh-my-Zsh!

At the root of everything we do in the terminal is the shell. It is how we interact between the terminal and the computer.

Traditionally, the default shell on Mac OS X was Bash. Bash is fine. But **zsh** is better! **zsh** (Called "Z Shell") is an alternative shell that is backward-compatible with Bash. This means you can still use the Bash that you know or copy bash scripts off the internet, but you have the added benefit of many other cool features in Zsh.

## Step 1: Install ZSH

So first we want to install **zsh** as our shell. If you are on Linux then you are most likely using Bash by default. Meaning you need to install zsh.

If you are using Mac then you might be using **zsh** already! Starting in Mac OS 10.10 (Yosemite), Mac OS shipped with **zsh** as the default shell. This includes Mac OS 10.11 (Big Sur) or _ANY_ mac with an Apple Silicon chip. If you are using an earlier version of Mac (10.9 or earlier) then you will need to install zsh.

Windows users are most likely using WSL (Windows Subsystem Linux) for their terminal (if you aren't then do yourself a favor and start). This means you are also using Bash since the most popular WSL distribution is Ubuntu, which runs Bash for interactive scripts.

Still not sure if you are using ZSH or BASH? There is a simple way to find out if you have. In the terminal type:

```SHELL
$ echo "$SHELL"
> /bin/zsh
```

This will output either `/bin/zsh` or `/bin/bash` depending on what shell you are using.

You could also try:

```SHELL
$ zsh --version
> zsh 5.8 (x86_64-apple-darwin20.0)
```

If you have **zsh** installed, then you will get an output like what is shown above with a version number.

If you still need to install zsh then now would be the time to do so.

**Mac Users:**

On mac it is easiest to use Homebrew. Again Apple Silicon Macs won't need to do this because you will already have **zsh**.

```BASH
$ brew install zsh
$ chsh -s /usr/local/bin/zsh
```

**Linux (Or Windows WSL):**

For linux users or Windows users using WSL can install ZSH through their distro's package manager (apt, pacman, yum, etc).

```BASH
# Ubuntu / Debian / Windows WSL
$ apt-get install zsh

# Arch Linux or Manjaro
$ pacman -S zsh
```

If you are still having problems installing ZSH, check out this far more detailed [zsh installation guide](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH).

## Step 2: Install Oh-My-Zsh

Zsh is cool and all... but oh-my-zsh cranks it up to 11. With oh-my-zsh we can add advanced theming, plugins, and more. Most of the really impressive _"how the hell did you do that!?"_ moments will generally be from oh-my-zsh features.

The best way to install oh-my-zsh is from the command line using _curl_.

```SHELL
$ sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

This will do everything for you, making this install super simple.

If you are still having trouble installing oh-my-zsh, [check out the oh-my-zsh installation guide](https://github.com/ohmyzsh/ohmyzsh/wiki).

## Install Oh My Zsh Plugins

One of the best benefits of Oh My Zsh is being able to install new plugins that expand its functionality. Oh-my-zsh already comes bundled with almost 100 different plugins that you can activate. By default, the `git` plugin is the only plugin that is activated.

I'll show you how to activate plugins in a moment and which ones I use. But there are a few plugins that are considered "custom" because they are not bundled with the oh-my-zsh install. So those are what we want to install right now.

### Improved Git Support

By default, Oh-my-zsh comes with its own git plugin that includes TONS of aliases to make git easier and faster to work with... in theory. Unfortunately the built-in git plugin is very inconsistent. So we will be installing a much-improved version of this plugin.

```BASH
$ git clone https://github.com/davidde/git.git ~/.oh-my-zsh/custom/plugins/git
```

Read More: [Improved Git Plugin](https://github.com/davidde/git)

### Autosuggestions



### 

## Install Fonts

I recommend Fira Code. It made by mozilla foundation and is open source. I find that it is an extremely clean font to read with a lot of really impressive features which makes it ideal for code.

In addition, it comes with ligatures built in, which is great.

You can also install a Nerd Fonts version which includes thousands of additional glyphs that Oh-my-zsh can use to improve the look of your terminal.
https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/FiraCode