## Installing Node.js

To use discord.js, you'll need to install Node.js. You can do so by going to [the Node.js website](https://nodejs.org/).

### Installing on Windows

If you're developing on Windows, it's as simple as installing any other program. Go to [the Node.js website](https://nodejs.org/), download the latest version, open up the downloaded file, and follow the steps from the installer.

### Installing on Linux

If you're developing on Linux, you may consult [this page](https://nodejs.org/en/download/package-manager/) to determine how you should install Node.<br />On that note, there's a possibility that you may already have Node \(e.g. if you're using a VPS\). You can check by running the `node -v` command. If it outputs something like `v8.0.0` or higher, then you're good to go! Otherwise, take a look at the page linked above for instructions on installing Node on your OS.

<p class="warning">If you _do_ have Node installed, but have an older version \(i.e. anything below 8.0.0\), you should upgrade to the latest version.</p>

---

## Preparing the essentials

To install and use discord.js, you'll need to install it via npm \(Node's package manager\). npm comes with every Node installation, so you don't have to worry about installing that. However, before you install anything, you should set up a new project folder.

### Setting up a project folder

Like any other project, you should have a dedicated folder for this, in order to keep it organized and manageable.

Navigate to a place on your machine where it's be easy for find and open in the future, for convenience purposes. Create a new folder by either right-clicking and choosing the "New &gt; Folder" option \(Windows\) or using the `mkdir` command \(e.g. `mkdir project-name`\) \(Linux\). If you already have a name you want to use for your bot, you can use that as the folder name. Otherwise, you may name it something like `discord-bot` for the time being \(or anything else you have in mind\).

Once you're done making the folder, open it up by double clicking it open \(Windows\) or using the `cd` command \(e.g. `cd project-name`\) \(Linux\).

### Opening the command prompt

If you're on Linux, you should already be inside of a command prompt, so you can skip to the next step.

If you're on Windows and aren't familiar with opening up the command prompt, simply do the following:

1. Open your bot project folder.
2. Hold down the `Shift` key and right-click inside of the folder.
3. Choose the "Open command window here" option.

It should then open up a window with a black background. It's a bit unattractive, but we'll talk about using better, more powerful tools in a different part of the guide.

### Using the command prompt

With the command prompt open, run the `node -v` command to make sure you've successfully installed Node.js. If you see something like `v8.0.0`, great! If not, go back and try installing again.

The next command you'll be running is `npm init`. This command creates a `package.json` file for you, which is what will be used to keep track of the dependencies your bot uses, as well as other info. If you're a bit confused by that, you can simply ignore it for the time being.

The `npm init` command will ask you a sequence of questions - you should fill them out as you see fit. If you're not sure of something or just want to skip it as a whole, simply leave it blank and press enter.

<p class="tip">Want to get started quickly? Use `npm init -y` to have it fill out everything for you!</p>

Once you're done with that, you're ready to install discord.js!

---

## Installing discord.js

Now that you've installed Node.js and know how to open up your console and run commands, you can finally install discord.js!

To install discord.js, simply run the `npm install discord.js`. This can take a bit of time, but should be done fairly quickly.

<p class="warning">Once the installation is complete, you'll see something like this:<br/>
![npm warnings](assets/img/BbcuyJ6.png)<br/>**This is perfectly normal and means that it worked.** You don't need to install any of the items listed in order to use discord.js; they are 100% optional.</p>

And that's it! With all the necessities installed, you're almost ready to start coding your bot.

---

## Installing a linter

While you are coding, you may find that you run into numerous syntax errors, or just code in an inconsistent style. Regardless, it's highly urged that you install a linter to ease a lot of coding troubles. While code editors generally are able to point out syntax errors, with a linter, you can coerce your coding to be in a specific style as you define in the configuration. While this is not required, it's strongly recommended. [Click here for the linter guide!](/preparations/setting-up-a-linter)
