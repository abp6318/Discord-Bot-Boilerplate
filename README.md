# Discord-Bot-Boilerplate

11/23/2020 - Hello! This is a template for those who want to create their own Discord bot!

## Getting Started

1. Make a Discord account (https://discord.com/).
2. Go to Discord Developer Portal (https://discord.com/developers/applications).
3. Click on "New Application" in the top right, and give your bot a name.
4. On the left side of your screen, click on "Bot".
5. In the top right of your screen, click on "Add Bot". Here you can add a profile picture for your bot. This is also the page where you will retrieve your bot's token from.
6. On the left side of your screen, click on "OAuth2".
7. Scroll down to the "Scopes" menu and check off "bot". 
8. Scroll down some more and give your bot permissions. Be careful, if you allow your bot to have too much access, and you accidentally reveal your developer key to the public, bad actors can use your bot to do a number of damaging things.
9. Once you've given your bot permissions, copy the link in the center of the page, and paste it into your browsers address bar. Add the bot to the server you want it to be on.

## Setting Up Your Local Directory

### Option 1: Forking the Directory

#### Prerequistites

1. Install Git (https://github.com/git-guides/install-git)

#### Forking

You can check it out how to do that here: https://docs.github.com/en/free-pro-team@latest/github/getting-started-with-github/fork-a-repo
You'll have to update the basic information in the directory, and change a handful of the documents listed in the .gitignore file. Make sure to add the config.json to the git ignore! You don't want other people looking at your bot's token!

### Option 2: Doing it Yourself

#### Prerequisites

1. Install Node (https://nodejs.org/en/download/).
2. Install Node Package Manager (npm) by entering ```npm install -g npm``` into a terminal.

#### Prepping the Directory

1. Create a new directory (folder) in a location you can remember.
2. Open up a terminal and move to the directory you just made.
3. Enter into the terminal ```npm init```. You'll be prompted a handful of times to enter information about your project, and this will create your package.json file. Make sure you have a way to run your bot locally by adding a similar line that I have on line 8 of my package.json ```"start": "node bot.js"```. In the initial package.json, it says index.js next "main", change that to bot.js as well.
4. Enter into the terminal ```npm install node```.
5. Enter into the terminal ```npm install discord.js```.
6. Create a new file called config.json (similar to the one in the repository above). Look to the config.json file in this repository and copy it's contents.
7. Return to your Discord Developer Portal (https://discord.com/developers/applications).
8. Select your bot > Select "Bot" on the left side of your screen > Under "Token" in the center of your screen, click on "Copy". If your token is revealed online in anyway, you need to return to this point and regenerate your key.
9. Now that you've copied your key, paste it into the config.json file where it says "your-token-here".
10. Create a new file, one that I mentioned briefly earlier, called bot.js. This is where you can store your primary content for your bot, but are more than capable of connecting a number of other files to it.

## Writing content

## Testing Locally

## Hosting Your Bot Free On Heroku

