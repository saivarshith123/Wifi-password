# WiFi Password Retriever

This script retrieves and displays the saved WiFi profiles and their passwords on a Windows machine using the `netsh` command.

## Features

- Lists all saved WiFi profiles on the machine.
- Displays the password for each WiFi profile.

## Technologies

- Python
- Windows Command Line

## Code Explanation

The script performs the following steps:

1. Uses the `subprocess` module to execute the `netsh wlan show profiles` command, which lists all saved WiFi profiles.
2. Parses the output to extract the profile names.
3. For each profile, executes the `netsh wlan show profile [profile name] key=clear` command to retrieve the profile details, including the password.
4. Parses the output to extract the password (if available) and prints the profile name along with the password.

## Usage

To use this script, simply run it on a Windows machine with Python installed. The script will display the WiFi profiles and their passwords in the console.
