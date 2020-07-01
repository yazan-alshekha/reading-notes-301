## Getting Started on Heroku with Node.js

## Introduction

This tutorial will have you deploying a Node.js app to Heroku in minutes.

Hang on for a few more minutes to learn how to get the most out of the Heroku platform.

The tutorial assumes that you have a free Heroku account, and that you have Node.js and npm installed locally.


### set up
When installation completes, you can use the heroku command from your terminal.

On Windows, start the Command Prompt (cmd.exe) or Powershell to access the command shell.
Use the heroku login command to log in to the Heroku CLI:

```

heroku login
heroku: Press any key to open up the browser to login or q to exit
 ›   Warning: If browser does not open, visit
 ›   https://cli-auth.heroku.com/auth/browser/***
heroku: Waiting for login...
Logging in... done
Logged in as me@example.com

```
This command opens your web browser to the Heroku login page. If your browser is already logged in to Heroku, simply click the Log in button displayed on the page.

This authentication is required for both the heroku and git commands to work correctl

Before you continue, check that you have the prerequisites installed properly. Type each command below and make sure it displays the version you have installed. (Your versions might be different from the example.) If no version is returned, go back to the introduction of this tutorial and install the prerequisites.

All of the following local setup will be required to complete the “Declare app dependencies” and subsequent steps.

This tutorial will work for any version of Node greater than 8 - check that it’s there:
``` 
node --version
v12.16.3

```

npm is installed with Node, so check that it’s there. If you don’t have it, install a more recent version of Node:

```
npm --version
6.14.4 
```
Now check that you have git installed. If not, install it and test again.
```
git --version
git version 2.17.0

```