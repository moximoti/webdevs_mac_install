# Automatic installation routine for webdevelopment on mac computers

Always when you install a new computer, or jump start with a clean install, you have to

- somehow remember, what programs you always install (you might easy remember the big things, but what was this small tool named you use for color picking)
- install all programs as they are needed, or in one long seesion (until you'll remember something else the next day)
- configure all these programs for your need

… at least these are my problems almost always. With tools like [homebrew](http://brew.sh/) and especially [homebrew bundler](https://github.com/Homebrew/homebrew-bundle) we can automate the first two points on this list. So I've ~~wrote~~ copy & pasted some shell scripting fu and made a `Brewfile` of the tools I think, a webdeveloper needs, when he is starting with a new mac. Feel free to fork, copy and paste this stuff, complete or just the `Brewfile`. to get a quick start on your computer.

## Usage
Copy the `Brewfile.example` file into you home directory as `Brewfile` and if needed add more programs. If you put your compiled programs anywhere other than `/Applications`, edit the `cask_args appdir: '/Applications'` line accordingly.

In the end, there is not much more to do then copying `install_my_mac.sh` in you home directory of your new mac, open the terminal and start it with `./install_my_mac.sh` and wait some time. From time to time you my need to push *the any key* but overall, everything should work automatically.

You are done then and have more time to configure your freshly installed mac.

## What the script does
- Install xcode utilities
- Install homebrew
- Install homebrew bundle
- Install all software listed in the local `Brewfile`
- Install oh-my-zsh

## Where to get a Brewfile?
The supplied `Brewfile.example` has all apps and command line tools I need in webdevelopment or needed in the recent past. This may or may not be representative. If you have `brew` and `brew-bundler` installed, you can *export* your actual instalalled programs with `brew bundle dump` and use this as a source.

## Further reading
- [Homebrew](https://brew.sh/)
- [Homebrew Bundler](https://github.com/Homebrew/homebrew-bundle)
- [Homebrew Cask](https://github.com/caskroom/homebrew-cask)
- [Mac Appstore Command Line Interface](https://github.com/mas-cli/mas)
- [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh)
