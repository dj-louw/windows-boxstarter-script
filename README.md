# Windows BoxStarter Script
Windows BoxStarter script that can be used to get a fresh machine up and running quickly 

# What is this
This uses [BoxStarter](https://github.com/chocolatey/boxstarter) and (Chocolatey)[https://chocolatey.org/] to automate the installation of a bunch of default applications on a fresh Windows install. This makes getting up and running on a new machine relatively painless, because the execution of a simple script after initial install can have the machine in a familiar state for the user.

BoxStarter makes use of some black magic to initiate the installer straight from a browser without requiring to install anything in the first place. This feature is natively supported in MS Edge, but not in other browsers, and might only work with a required plugin. Check the BoxStarter docs for more info. Since we are setting up a fresh machine, MS Edge will be the default browser, and thus we don't really have to worry about this all that much.

# How it works
I provide three use cases for your reading pleasure:

## If you are me
1. Get the raw GitHub url for the text file in this repo called `boxstarter-script`. It'll most likely be `https://raw.githubusercontent.com/dj-louw/windows-boxstarter-script/main/boxstarter-script`
2. Open up a terminal session, either in CMD or PowerShell. Either option works.
3. Paste the following in the terminal, and append with the URL from Step 1: `START https://boxstarter.org/package/nr/url?`

So in the end, copy the following and paste in a terminal and hit `ENTER`

```
START https://boxstarter.org/package/nr/url?https://raw.githubusercontent.com/dj-louw/windows-boxstarter-script/main/boxstarter-script
```

## If you are not me
1. Clone this repo
2. Edit the `boxstarter-script` file to suit your needs
3. Follow the steps 1-3 in the *If you are me* section above

## If you want to be like me
1. GOTO *If you are me*

# What next
This script already sets some windows configurations that I always enable, such as show hidden files, and so on. BoxStarter supports this natively. But there are many settings that it does not yet set. Thus, a future enhancement of this script (or possibly another one) is to start adding basic-initial-windows-default-settings to it. Some of the things that I can think of that I might want to change:
- Disable all telemetry
- Set times for Windows Update
- Configure Eye Shield/Guard/whatever-the-thing-is-called-that-removes-blue-light-from-the-display-at-night
- Uninstall all the crapware
- Set default browsers
- Set defaults for other programs.
