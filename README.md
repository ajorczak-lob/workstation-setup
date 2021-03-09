# Workstation Setup
Forked from [pivotal/workstation-setup](https://github.com/pivotal/workstation-setup)

This project automates the process of setting up a new Lob machine using a simple [Bash](https://www.gnu.org/software/bash/) script.

## Goals

The primary goal of this project is to give people a simple script they can run to make their machine a bit more useful and standard for working on Lob projects.

* A port of [Notion-Workstation Setup](https://www.notion.so/lob/Workstation-Setup-c5e804afa8664e67990b95afacad3665)

## Non-goals

This project does not aim to do everything. Some examples:

 * We don't install everything that your project needs. These scripts should only install generally useful things, and prefer running quickly over being complete.
 * We avoid setting up and maintaining overly-custom configurations. When there is already a tool that will get us something in a conventional manner, such as [bash-it](https://github.com/Bash-it/bash-it), we prefer to use it instead of doing things ourselves.

**Warning: the automation script is currently aggressive about what it does and will overwrite vim configurations, bash-it configurations, etc.**

## Getting Started

- Run the latest version of macOS, currently [High Sierra](https://www.apple.com/macos/high-sierra/),
  unless you have a specific reason not to
- These scripts might work on previous versions, but are maintained with only the latest macOS in mind
- If you are not on High Sierra, you need to install the latest version of [Xcode](https://developer.apple.com/xcode/)
- On High Sierra, once you have used git (below), you will have installed the command line developer tools

Open up Terminal.app and run the following command:

```sh
mkdir -p ~/workspace &&
  cd ~/workspace &&
  git clone https://github.com/ajorczak-lob/lob-workstation-setup.git &&
  cd workstation-setup
```

### Engineering Machine

If you're setting up an engineering machine choose which languages to install:

```sh
# For Most Lob Developers
./setup.sh docker golang node ruby terraform
```

The list of Engineering applications is found in: [applications-common.sh](https://github.com/pivotal/workstation-setup/blob/master/scripts/common/applications-common.sh)


## Having problems?

If you're having problems using the setup script, please let us know by [opening an issue](https://github.com/ajorczak-lob/lob-workstation-setup/issues).

If you see errors from `brew`, try running `brew doctor` and include the diagnostic output in your issue submission.
