# PhoneLink

Send links to your computer from your phone, or from any device in your local network.

## Installation

1. Download the latest release, or clone and build with Visual Studio.
2. Change your port inside of your `Phonelink.exe.config` file to whatever you want it to be.
3. inside of the `setup.ps1` file, set your port to whatever it is inside of your config. Save and run the script. It should prompt you to **run as an Administrator**.
4. (Optional, but recommended) Right click the `Phonelink.exe` file and click `Create shortcut`. Rename this to whatever you like, and drag this inside of the `startup` folder. This folder is a shortcut to your startup folder, meaning the application will run at system startup.
5. Run the executable.
6. Download the [iOS Companion Shortcut](https://www.icloud.com/shortcuts/745a4ed5672e4160a01623864a84baee) and answer the questions you are prompted to, or edit the texts inside of the actual shortcut. (You can run the `ipconfig` command in powershell to find your ip address).

## Usage

With the shortcut, when you share a link, an option should appear in your share sheet saying "_Open link on computer_". Once clicked, the link should appear on your computer's browser.

Alternatively, you can make an http request, by using `curl`, `fetch`, or just your browser. I would not reccommend this and i would recommend making an android-alternative to shortcuts, makng a script, etc. The request should look like this:
`http://IP_ADDRESS:PORT/PASSWORD/REQUEST_TYPE/URL`

or without your password disabled:
`http://IP_ADDRESS:PORT/REQUEST_TYPE/URL`

Currently, the only valid request type is `url`.

an example with a password of `1234`:

`http://192.168.0.69:1234/1234/url/google.com`
(use of http or https in the link isn't required.)

If you run into any problems, contact me on discord, ahsan#4403, or make an issue.

## Configuration

You can configure the port and password in the `Phonelink.exe.config` file, and customise whether you'd like to check for updates and have a password in the right click context menu.

## Updating

1. Download the self-extracting archive from the releases tab.
2. Extract the files to your current installation location, or just copy and paste them in. Make sure you copy and paste all of the files, or it may not work as intended.
