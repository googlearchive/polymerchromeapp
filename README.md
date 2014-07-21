# Polymer Chrome App

## Getting Started

To install the project in your Chrome installation - Goto [Extensions](chrome://extensions/) > Load unpacked extension... and point to a clone of this repo or just drag and drop the folder to the extensions view.

## Build

To build the app run the following commands:

    npm install -g grunt-cli
    npm install
    grunt

### Dealing with CSP

Chrome Apps have a strict Content Security Policy (CSP) which prevents inline `script` elements. Using the [Vulcanize tool](www.polymer-project.org/articles/concatenating-web-components.html) with the `--csp` flag, we can strip all of the script elements out of our Polymer elements, and place them in an external `build.js` file.

    vulcanize -o build.html index.html --csp

To make this process easier, we've included the [grunt-vulcanize](https://github.com/Polymer/grunt-vulcanize) task in our Gruntfile. This task will watch for any file changes and re-run the Vulcanize tool for us, making it much faster to develop and test your app. When you run the `grunt` command the Vulcanize tool will start up and watch for file changes.

## Resources

* [Chrome App](http://developer.chrome.com/apps)
* [Polymer Project](http://www.polymer-project.org/)

## Screenshot
![screenshot](https://raw.githubusercontent.com/vikasprogrammer/polymerchromeapp/master/assets/screenshot_1280_800.png)

## Credit

Big thanks to [vikasprogrammer](https://github.com/vikasprogrammer) for creating the [original example](https://github.com/vikasprogrammer/polymerchromeapp).
