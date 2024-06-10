# Speedy QC Installation Guide

This guide will help you install Speedy QC on your system.

## Prerequisites

Before you begin, ensure you have the following:

- A Mac computer running macOS.
- An internet connection.
- Basic knowledge of using the Terminal.

## Steps to Install Speedy QC

### 1. Open Terminal

You can open Terminal by searching for it in Spotlight (click the magnifying glass in the upper right corner of your screen or press `Command + Space` and type "Terminal").

### 2. Install Homebrew

Homebrew is a package manager for macOS. To install Homebrew, follow these steps:

1. In the Terminal window, paste the following command and press Enter:

    ```
    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
    ```

2. Follow the on-screen instructions. The installation script will guide you through the process. You may be prompted to enter your password and to confirm the installation steps.

### 3. Add Homebrew to Your PATH

After the installation is complete, you need to add Homebrew to your PATH. This can be done by adding the following line to your shell configuration file.

For Zsh (macOS Catalina and later):

    ```
    echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zshrc
    source ~/.zshrc
    ```

For Bash:

    ```
    echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.bash_profile
    source ~/.bash_profile
    ```

### 4. Verify the Installation

To make sure Homebrew is installed correctly, run:

    ```
    brew --version
    ```

This should display the version of Homebrew that was installed.

### 5. Install libffi

Once Homebrew is installed, use it to install `libffi` by running:

    ```
    brew install libffi
    ```

### 6. Install Python 3.10

Next, install Python 3.10 using Homebrew:

    ```
    brew install python@3.10
    ```

### 7. Install Speedy QC

Finally, install Speedy QC by running the following command:

    ```
    python3.10 -m pip install git+https://github.com/PanagiotisFytas/speedy_qc
    ```

Congratulations! You have successfully installed Speedy QC on your system.

## Troubleshooting

If you encounter any issues during installation, ensure that you have followed each step carefully. For further assistance, refer to the official Homebrew and Python documentation.
