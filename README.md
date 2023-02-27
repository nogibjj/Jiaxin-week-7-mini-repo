# Week 7 Mini Project

## Introduction
anybar_rs is a command-line application written in the Rust programming language that allows you to control the macOS Anybar application. Anybar is a small utility that adds a colored dot to your macOS menubar, which can be used for various purposes, such as indicating the status of a long-running command or notifying you when a certain event occurs. It provides a simple and convenient way to interact with Anybar from the command line. 

With anybar_rs, you can easily set the color and status of the Anybar dot, as well as control its visibility and animate it. This can be useful, for example, in shell scripts or automation workflows where you need to provide feedback to the user or monitor the progress of a task.

## Install
Here are the steps to install Rust and Cargo using rustup.rs and then install anybar_rs:

1. Install Rust and Cargo using rustup.rs:
* Go to the Rustup website at https://rustup.rs/.
* Follow the instructions on the website to download and run the Rustup installer appropriate for your system.
* The installer will ask you to customize your installation, such as choosing the default toolchain and target platforms. You can choose the default options for most settings.
* Once the installation is complete, open a new terminal window to ensure that the Rust environment variables are set correctly.

2. Install anybar_rs using Cargo:
* Open a terminal window and enter the command cargo install anybar_rs.
* Cargo will download the anybar_rs source code from the internet, compile it, and install the binary to your system.
* Once the installation is complete, you can verify that anybar_rs is installed by running the command anybar_rs --help. This should display the help text for the anybar_rs command.

That's it! You should now have anybar_rs installed on your system and ready to use. You can use the anybar_rs command to interact with the Anybar application on your macOS system.

## Build anybar_rs from the source code using Cargo:
1. Open a terminal window and navigate to the root directory of the anybar_rs project.

Run the following command to build the binary in release mode:
```
cargo build --release
```

This command will download any required dependencies, compile the source code, and generate the binary file in release mode. The binary file will be saved in the `target/release` directory.

2. You can now use the binary file by running the following command:
```
target/release/anybar_rs --help
```

This should display the help text for the anybar_rs command.

That's it! You should now have the anybar_rs binary built and ready to use. You can use this binary to interact with the Anybar application on your macOS system.

## How to use anybar_rs
