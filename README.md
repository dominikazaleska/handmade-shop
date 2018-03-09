# SHOP

### Setup

##### Prerequisites

Install [polymer-cli](https://github.com/Polymer/polymer-cli):

    npm install -g polymer-cli

"If you don’t have Node.js and/or npm installed on your machine, do the following for your respective OS.

###### Mac

Go to nodejs.org, click ‘install’, and run through the install process.

###### Ubuntu

Run the following on your command line to install the source for nodejs

    curl -sL https://deb.nodesource.com/setup | sudo -E bash -

Then, run this to get the latest nodejs package

    sudo apt-get install -y nodejs

###### Windows

Go ahead the download the Windows binary and make sure to restart your computer.

###### Test It!

    node -v

To see if Node is installed, type the above on your command line.

    npm -v

To see if npm is installed, type the above on your command line."

Source: https://www.npmjs.com/package/polymer-cli/tutorial

##### Setup
    # Using CLI
    mkdir shop
    cd shop
    polymer init shop

    # Or cloning direct from GitHub
    git clone https://github.com/Polymer/shop.git
    cd shop
    bower install

### Start the development server

    polymer serve

### Run web-component-tester tests

    polymer test

### Build

Build presets provide an easy way to define common build configurations in your `polymer.json` file. There are 2 build presets we put in `polymer.json` file in Shop:

**es5-bundled**

- js: {minify: true, compile: true}
- css: {minify: true}
- html: {minify: true}
- bundle: true
- addServiceWorker: true
- addPushManifest: true
- insertPrefetchLinks: true

**es6-unbundled**

- js: {minify: true, compile: false}
- css: {minify: true}
- html: {minify: true}
- bundle: false
- addServiceWorker: true
- addPushManifest: true
- insertPrefetchLinks: true

Run the command to build the presets:

    polymer build

### Test the build

This command serves the `es5-bundled` build version of the app:

    polymer serve build/es5-bundled

This command serves the `es6-unbundled` build version of the app:

    polymer serve build/es6-unbundled
