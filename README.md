# PhoneLink

Send links to your computer from your phone, or from any device in your local network.

## Installation

1. Run the Installer. Then, run the `setup.ps1` file to trust your chosen port, and add it to your firewall. Requests **will not work** if you do not do this. (if you manually installed before I created an installer, please delete your PhoneLink folder from wherever you placed it, and delete your startup shortcut.)
2. Edit your settings by clicking on the icon in your tray. Make sure to change your save location, as it saves it to a folder inside of it's current path by default.
3. Download these shortcuts:
    - [Open Link on Computer](https://www.icloud.com/shortcuts/19bfb332f6be4ffd8b5ebcbc55d15cfb)
    - [Save File on Computer](https://www.icloud.com/shortcuts/8c3aa77aecb944a9aa4ee5e202ee4bed)

Answer the questions you are prompted to, or edit the texts inside of the actual shortcut. (You can run the `ipconfig` command in powershell to find your IP address).

## Usage

When you share a link, an option should show in your share sheet called "Open link on computer". Once clicked, the link should appear on your computer's browser.
When you share a file or image, an option in your share sheet should show called "Save File on Computer". Once clicked, the file should save wherever you specified.

Alternatively, you can make an HTTP request, I would not reccommend this and i would recommend making an android-alternative to shortcuts, makng a script, etc.

### Requests:

-   URL: `http://(IP):(PORT)/(PASSWORD)/url/(URL_ADDRESS)`
-   File/Image: `http://(IP):(PORT)/(PASSWORD)/file`. Your file(s) inside of a form-data body. The key can be anything and the value is your file. You can have multiple of these.

an example with a password of `1234`:
`http://192.168.0.69:1234/1234/url/google.com`
(use of http or https in the link isn't required.)

If you run into any problems, contact me on discord, ahsan#4403, or make an issue.

## Configuration

~~You can configure the port and password in the `Phonelink.exe.config` file, and customise whether you'd like to check for updates and have a password in the right click context menu.~~

A settings menu is now available by clicking on the PhoneLink icon in the system tray.
