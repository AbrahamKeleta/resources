# Flutter Setup 

Our computers need to be setup for flutter development before we can start building applications. 

We will go in order: 

## Step 0: Install Visual Studio Code 

Here is a download link: https://code.visualstudio.com/download

## Step 1: Download Flutter

Here is the link for the download file: 

https://docs.flutter.dev/get-started/install/macos/mobile-ios?tab=download

If you have a computer that is M1 chip, you need to run this command: 

```code
$ sudo softwareupdate --install-rosetta --agree-to-license
```

It helps your M1 chip to be compatible with software intended for intel-chip basec computers. 

Next when your download is finished and is in your downloads folder, you need to modifiy the command: 

```code
$ unzip ~/downloads/flutter_macos_arm64_3.19.1-stable.zip -d ~/downloads/

```

Usually, downloaded content is found in downloads folder, which is why we need to change the folder name. And we needed to update the zip file name as well. 

Now our folder has been unziped through the terminal, you should see a flutter folder in your downloads folder. 

Add flutter to the path while you are it too, this allows you to have access to the flutter command: 

```code
export PATH=$HOME/downloads/flutter/bin:$PATH
```

Try to see what errors you get from the platform: 

```code
$ flutter doctor
```

It should give you a list of check off and unchecked items that let you know where you are at. 

Step 2: Download Xcode

Go to your App Store, and search for Xcode. 


## Step 3: Install iOS Simulator

```code
$ xcodebuild -downloadPlatform iOS
```

and sign the iOS agreement as well. 

```code
$ sudo xcodebuild -license
```

## Step 4: Install Cocoapods

Before we install cocoapods, we need to install Brew, which is a package manager. 

run this command: 
```code
$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

make sure you follow the prompts and press enter when it asks you. 

Run this command so that you can add it to path, which makes Brew command available for you. 

```code
$ eval "$(/opt/homebrew/bin/brew shellenv)"
```

## Step 5: Finish setup 

run flutter doctor again to check you setup needs: 

```code
$ flutter doctor
```

## Step 6: Create Flutter App

Let's create a demo flutter app right quick: 

```code
$ flutter create hello_world
```

run the simulator and turn it on: 

```code
$ open -a Simulator
```

Open your VS Code and open the project you just created on the terminal, an app called hello_world. 

We are getting ready to run it on the simulator but we need to add some flutter plugins to the code editor

- Go to the 5 icon on the left side of your VS Code, it should say extensions.

- click on it and search for flutter, click install

Now you can close out of the extensions icon and open a main.dart of the application. 

- command + P, search, main.dart, select

Now you should have a play button on the top right corner of VS Code, click on that to run the application. 

This should run your first application on your virtual simulator! 

You have setup up your computer with flutter and are ready to build now. 

Most of what you will need build on is on main.dart. 




