Getting Started
======================

This is a sample hybrid application for the IBM Watson Mobile Developer Challenge.

![image](https://raw.githubusercontent.com/IBMMobileCoC/watson-photography-hybrid/master/readme-assets/Watson-Photography-splash-screen.png?token=1179038__eyJzY29wZSI6IlJhd0Jsb2I6SUJNTW9iaWxlQ29DL3dhdHNvbi1waG90b2dyYXBoeS1oeWJyaWQvbWFzdGVyL3JlYWRtZS1hc3NldHMvV2F0c29uLVBob3RvZ3JhcGh5LXNwbGFzaC1zY3JlZW4ucG5nIiwiZXhwaXJlcyI6MTM5OTA1ODc5MX0%3D--823fe2244e224ad838122529fb83ede1725c8022) &nbsp;
![image](https://raw.githubusercontent.com/IBMMobileCoC/watson-photography-hybrid/master/readme-assets/Watson-Photography-answer-screen.png?token=1179038__eyJzY29wZSI6IlJhd0Jsb2I6SUJNTW9iaWxlQ29DL3dhdHNvbi1waG90b2dyYXBoeS1oeWJyaWQvbWFzdGVyL3JlYWRtZS1hc3NldHMvV2F0c29uLVBob3RvZ3JhcGh5LWFuc3dlci1zY3JlZW4ucG5nIiwiZXhwaXJlcyI6MTM5OTA1OTE3Nn0%3D--0d7d80a1d2abe506850597268303334b8e7533a5)

This project is a reference application demonstrating how to build a hybrid mobile application that connects to IBM Watson. It is build using the following libraries:
* Apache Cordova v3.4
* RequireJS v2.1.11
* Backbone.js v1.1.2
* underscore v1.6.0
* jQuery v1.10.2
* jQuery Mobile v1.4.2

## Getting the Code

Clone this Github repository.

## Setting up the hybrid app with Apache Cordova CLI v3.4

The hybrid mobile application sample code was created using Cordova v3.4. Below outlines the process I went through to set up Cordova and the project on OS X. You can chose to do the same, or you can read the full Cordova documentation at: http://cordova.apache.org/docs/en/3.4.0/ which provides much more in-depth coverage. You could also chose to pull out the ‘www’ directory which is simply HTML, JS, and CSS for use within you own project, such as an IBM Worklight.

1. Make sure an up-to-date version of Node.js is installed on your system.

2. Install the latest version of Cordova globally:
```sh
sudo npm install -g cordova
```

3. Open Terminal and navigate to a directory where you store projects on your system. For example:
```sh
cd ~/Projects
```

4. Create a new directory for this project and change into that directory:
```sh
mkdir watson-photography && cd $_
```

5. Create a new Cordova project with name “Watson Photography" and id "com.ibm.watson.WatsonPhotographyHybrid":
```sh
cordova create watson-photography-hybrid com.ibm.watson.WatsonPhotographyHybrid 'Watson Photography'
```

6. Navigate into your new project directory:
```sh 
cd watson-photography-hybrid
```

7. At this point you can replace the `www` directory in your new project with the `www` directory from this repository 

8. Now add a couple of platforms that you would like to support:
```sh
cordova platform add android
cordova platform add ios
```

9. Make a build:
```sh
cordova build
```

10. Add some common Cordova plugins:
```sh
cordova plugin add org.apache.cordova.console
cordova plugin add org.apache.cordova.device
cordova plugin add org.apache.cordova.splashscreen
```

11. Start a local web server for the www/ assets: (default port 8000)
```sh
cordova serve 8000
```

## Running the hybrid app example without Apache Cordova

The root directory, 'watson-photography-hybrid' contains a directory named 'www' This directory contains all of the HTML, JavaScript and CSS for the project. If you host the 'www' folder on a local webserver you will be able to access the 'index.html' file and run the reference application through a browser.

If you don't have a local webserver configured, you can also start Google Chrome with the following command line arguments: `--args --disable-web-security --allow-file-access-from-files` and open the 'index.html' file.
For example, on OS X you would open a terminal and type:
```sh
open -a Google\ Chrome --args --disable-web-security --allow-file-access-from-files
```

## Configuring the reference application
Find the `Constants.js` file in the `www/js/com/models` directory and add the username, password and the watson instance id number to contact the Watson API.

-----

## Overview

