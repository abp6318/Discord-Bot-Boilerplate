# Discord-Bot-Boilerplate

11/23/2020 - Hello! This is a template for those who want to create their own Discord bot!
01/31/2020 - Preparing for a presentation I'm giving tomorrow and realizing that this lacks a few steps in the Heroku section. Bear with me as I make updates and separate that section into two. There are three ways to host the bot through Heroku, and I'm realizing I should have clearly separated the main two. Thanks.

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
6. Create a new file called config.json, similar to the one in the repository above named config.example.json. Look to the config.example.json file in this repository and copy it's contents.
7. Return to your Discord Developer Portal (https://discord.com/developers/applications).
8. Select your bot > Select "Bot" on the left side of your screen > Under "Token" in the center of your screen, click on "Copy". If your token is revealed online in anyway, you need to return to this point and regenerate your key.
9. Now that you've copied your key, paste it into the config.json file where it says "your-token-here".
10. Create a new file, one that I mentioned briefly earlier, called bot.js. This is where you can store your primary content for your bot, but are more than capable of connecting a number of other files to it.

## Writing Content (v12!!!)

It takes a bit of practice, but with time, you'll be flying through code. Check out documentation from the following sources. Wherever you find documentation the easiet to learn, make sure you're looking at version 12 (v12). This is very important if you want your code to run! Happy coding!

1. https://discordjs.guide/
2. https://discord.js.org/

## Testing Locally

If you did all of the set up in the instructions I listed above, you should be able to enter ```npm start``` into your terminal (while in the directory), and your bot should run (given it has the proper code). When running your bot, it is live on each and every server you added it to. This also means that any action you program your bot to do on one server, it will do on every server it's added to.

## Hosting Your Bot Free On Heroku

### Getting Started On Heroku

1. If you haven't yet, create a repository, and add your code to it. See here on how to create a repository (https://docs.github.com/en/free-pro-team@latest/github/getting-started-with-github/create-a-repo).
2. In your repository, add a file called "Procfile". It has no extension, and is simply titled "Procfile" with a capital 'P'. Add this single line of code to the file ```worker: node bot.js``` and add it to your repository.
3. Sign up for a Heroku account (https://signup.heroku.com/).
4. Once you've confirmed your account via email, click on the button that reads "Create a new app".
5. Under "Deployment Method", click on GitHub. Attach your GitHub account to your Heroku account. 
6. Deploy your bot
7. While your bot is being deployed, you can view the build log under the "Activity" tab.
8. If you set up your Profile correctly, and deployed your bot, you should see ```web npm start``` under the "Resources" tab. Make sure this is turned ON.
9. Any pushes you make to your GitHub repository will now affect your bot.
10. Your bot should now run 24/7, only turning off if you damage your code badly enough, switch off ```web npm start``` under the "Resources" tab, or turn off the deployment.

## Contact

Well, I hope this infomation at least got you on the right path to making a super cool Discord bot! I'd love to hear about the cool creations you've made.

Feel free to email me: abp6318@rit.edu or blueputt@gmail.com
