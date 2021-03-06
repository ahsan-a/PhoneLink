
  
# PhoneLink

Link your iPhone to your computer via HTTP requests.

## Installation

1. Run the Installer. Then, run the `setup.ps1` file to trust your chosen port, and add it to your firewall. Requests **will not work** if you do not do this. (if you manually installed before I created an installer, please delete your PhoneLink folder from wherever you placed it, and delete your startup shortcut.)
2. Edit your settings by clicking on the icon in your tray. Make sure to change your save location, as it saves it to a folder inside of it's current path by default.
3. Download these shortcuts:
    - [PhoneLink (Control power state and send notification)](https://www.icloud.com/shortcuts/17aacb75e9704c45bb65b9e8d748f7dd)
    - [Open Link on Computer](https://www.icloud.com/shortcuts/19bfb332f6be4ffd8b5ebcbc55d15cfb)
    - [Save File on Computer](https://www.icloud.com/shortcuts/8c3aa77aecb944a9aa4ee5e202ee4bed)

Answer the questions you are prompted to, or edit the texts inside of the actual shortcut. (You can run the `ipconfig` command in powershell to find your IP address).

## Usage

When you share a link, an option should show in your share sheet called "Open link on computer". Once clicked, the link should appear on your computer's browser.
When you share a file or image, an option in your share sheet should show called "Save File on Computer". Once clicked, the file should save wherever you specified.

Alternatively, you can make an HTTP request, I would not reccommend this and i would recommend making an android-alternative to shortcuts, makng a script, etc. 

Requests look like this: `http://IP:PORT/PASSWORD/TYPE`

and like this without a password: `http://IP:PORT/TYPE`

### Requests:
|Request Type | Request Format | Request Example | Request Description |
|--|--|--|--|
| URL | `[IP]:[PORT]/[PASSWORD]/url/[URL]` | `192.168.0.2:1234/1234/url/google.co.uk` | A GET request to send a link to your computer. It doesn't need to begin with `http://` or `https://`.|
| File |`[IP]:[PORT]/[PASSWORD]/file`|`192.168.0.2:1234/1234/file`| POST request to save files on your computer. Your file(s) inside of a form-data body. The key can be anything and the value must be your file(s). You can have multiple of these. The save location is whatever specified inside of your settings.|
|Notification|`[IP]:[PORT]/[PASSWORD]/notification`| `192.168.0.2:1234/1234/notification` |A GET request to send a notification to your computer. Your content must be in the form of headers. Your headers are `title`, and `body`. |
|Power|`[IP]:[PORT]/[PASSWORD]/power/[TYPE]`|`192.168.0.2:1234/1234/power/shutdown`|A GET request to control your computer's power state. your `[TYPE]` must be either: `shutdown`, `restart`, `logout`, or `lock`.|

The password is optional.

If you run into any problems make an issue, orcontact me on discord (ahsan#4403).

## Configuration

A settings menu is now available by clicking on the PhoneLink icon in the system tray. (v1.2.0)
