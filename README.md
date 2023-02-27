# Week 7 Mini Project

## Introduction
anybar_rs is a command-line application written in the Rust programming language that allows you to control the macOS Anybar application. Anybar is a small utility that adds a colored dot to your macOS menubar, which can be used for various purposes, such as indicating the status of a long-running command or notifying you when a certain event occurs. It provides a simple and convenient way to interact with Anybar from the command line. 

With anybar_rs, you can easily set the color and status of the Anybar dot, as well as control its visibility and animate it. This can be useful, for example, in shell scripts or automation workflows where you need to provide feedback to the user or monitor the progress of a task.

## Install
Here are the steps to install Rust and Cargo using rustup.rs and then install anybar_rs:

1. Install Rust and Cargo using rustup.rs:
* Go to the Rustup website at https://rustup.rs/.
```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
* Follow the instructions on the website to download and run the Rustup installer appropriate for your system.
* The installer will ask you to customize your installation, such as choosing the default toolchain and target platforms. You can choose the default options for most settings.
* Once the installation is complete, open a new terminal window to ensure that the Rust environment variables are set correctly.

2. Install anybar_rs using Cargo:
* Open a terminal window and enter the command cargo install anybar_rs.
* Cargo will download the anybar_rs source code from the internet, compile it, and install the binary to your system.
* Once the installation is complete, you can verify that anybar_rs is installed by running the command anybar_rs --help. This should display the help text for the anybar_rs command.

That's it! You should now have anybar_rs installed on your system and ready to use. You can use the anybar_rs command to interact with the Anybar application on your macOS system.

## Build anybar_rs from the source code using Cargo
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
anybar_rs assumes that Anybar is running on the local machine and listening for UDP packets on port 1738. 
You can use the `-p` or `--port` option to specify a different port number if necessary. The port number must be between 0 and 65535.

The available commands that you can send to Anybar using anybar_rs are:

* white: Sets the color of the Anybar dot to white.
* red: Sets the color of the Anybar dot to red.
* orange: Sets the color of the Anybar dot to orange.
* yellow: Sets the color of the Anybar dot to yellow.
* green: Sets the color of the Anybar dot to green.
* cyan: Sets the color of the Anybar dot to cyan.
* blue: Sets the color of the Anybar dot to blue.
* purple: Sets the color of the Anybar dot to purple.
* black: Sets the color of the Anybar dot to black.
* question: Sets the color of the Anybar dot to blue and displays a question mark icon.
* exclamation: Sets the color of the Anybar dot to yellow and displays an exclamation mark icon.
* quit: Closes the Anybar application.

Eg: You can specify the command as an argument to the anybar_rs command. For example, to set the color of the Anybar dot to red, you can run the following command:
```
anybar_rs red
```

You can also use the `-h` or `--help` option to display the help text for the anybar_rs command, or the `-V` or `--version` option to display the version number of anybar_rs.

## Exit codes for anybar_rs
1. If the UDP datagram is successfully sent to Anybar, anybar_rs will exit with a status code of 0. This indicates that the command was executed successfully.

2. If you provide anybar_rs with an unknown flag or option, or if you specify an unknown command, anybar_rs will display the usage information and exit with a status code of 1. This indicates that the command was not executed due to invalid input.

**Hint**: It's worth noting that since UDP is a stateless protocol, there is no guarantee that the datagram will be received by the destination. Therefore, even if anybar_rs exits with a status code of 0, it is possible that the command did not have any effect on the Anybar dot. To ensure that the command is received and acted upon by Anybar, you may want to consider sending the command multiple times or implementing some form of error checking.
