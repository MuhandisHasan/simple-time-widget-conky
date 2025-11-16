# Simple Time Widget Conky
A simple but aesthetic time widget template for Conky
See screenshot.png
![alt text](https://github.com/MuhandisHasan/simple-time-widget-conky/blob/main/screenshot.png?raw=true)

# Installation

This guide will help you install and set up Conky with the Simple theme.

1.  **Install Conky**:
    Follow the official Conky installation instructions for your operating system: [Conky Installation Guide](https://github.com/brndnmtthws/conky/wiki/Installation)

2.  **Copy the Simple directory**:
    Copy the `Simple` directory to `$HOME/.config/conky/`. If the `conky` directory doesn't exist inside `.config`, please create it first.

3.  **Test the widget**:
    Try running `/Simple/start.sh` from your terminal.
    ```bash
        user@debian: $HOME/.config/conky/Simple/start.sh
    ```
    If the Conky widget appears on your desktop, proceed to step 4 to configure autostart. If it doesn't work, skip to step 6 for troubleshooting.

4.  **Configure Autostart**:
    Copy the `widget.desktop` file to `$HOME/.config/autostart/`.

5.  **Enable Autostart**:
    Open "Session and Startup" (or the equivalent application for managing startup programs on your OS). Navigate to "Application Autostart" and ensure that "Conky (Start Conky On Boot)" is checked.

6.  **Troubleshooting (If the widget doesn't appear)**:
    Errors are often related to incorrect file paths. Please check the following:

    *   **Check `start.sh` path**:
        Open `/Simple/start.sh` and verify that the path in the line below correctly points to `Simple.conf`:
        ```bash
        conky -c $HOME/.config/conky/Simple/Simple.conf &> /dev/null &
        ```
        Try running `your-path/start.sh` from your terminal. If the widget now appears, the path is correct, and you can proceed to configure autostart (step 4).

    *   **Check `widget.desktop` path**:
        Open `widget.desktop` and confirm that the `Exec` line correctly points to your `start.sh` file:
        ```
        Exec=/home/user/.config/conky/Simple/start.sh
        ```
        Make sure `/home/user` is replaced with your actual home directory path.

I hope this helps you get your Conky widget up and running! If you encounter any further issues, feel free to ask. 

muhandisarrantisi@gmail.com