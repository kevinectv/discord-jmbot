# Shift Swap
### Our Discord bot to allow mentors to fairly swap shifts. Built with discord.js.

# How to run:
## Hosting 
> ⚠  This bot needs a [Node.js v16+](https://nodejs.org/en/blog/release/v16.0.0/)  runtime to function since discord.js version 13 requires node version 16 to function. I've been using Node.js v18+.

### Step 1: Install the Dependencies:
Linux 
```sh
apt install nodejs npm -y
curl -sL https://deb.nodesource.com/setup_16.x -o nodesource_setup.sh
chmod 777 nodesource_setup.sh
./nodesource_setup.sh
apt install nodejs -y
npm install
```
Windows 
```sh
# https://nodejs.org/en/blog/release/v16.0.0/ get node.js
npm install 
```

### Step 2: You may need to add the bot to your hosts file.
```sh
Open your hosts file and add:
172.0.0.1   discord.local
```

### Step 3: Create a bot [Here](https://discord.com/developers) <br> <br>
```
- You'll need to create a new application in the top right.
- Click on bot and click 'add bot'
- Copy the token. Once you copy it, it will dissapear, so if you lose it, you'll have to reset the token.
- In the 0Auth2 tab, you'll need a redirect. add this one to run it locally: http://localhost:8080/oauth/token
```
<b>
  

### Step 4: Replace the Token and other dependencies inside [.env](https://github.com/sandarutharuneth/ivongiveaways/blob/master/.env) <br>
```sh
TOKEN=Your bot token goes here
FOOTERIMG=This will show up at the footer of each embed when called, it is set to our lighthouse logo.
THUMBNAIL=This will show up as the thumbnail of each embed when called, it is set to our lighthouse logo.
DCBL=https://cdn.discordapp.com/attachments/477946103287906304/482738675776618497/DBL.png #This is a default Discord Bot List logo.
```  
### Step 5: Invite the bot.
```
- In the Discord developer portal, go to the bot > 0Auth2 > URL generator
- Add 'identity' and 'bot'.
- Select the redirect URL added in step 3.
- For premissions in 'General' add 'Read Messages/View Channels
- For permissions in 'Test' add 'Send messages', 'Manage Messages', 'Embed Links', 'Attach Files', 'Read Message History', 'Mention everyone', 'Use External Emojis', 'Add Reactions', 'Use Slash Commands'.
- Copy the URL at the bottom and paste it in a browser.
- Follow the prompts to invite it to one of our test servers.
```
### Step 6: Now run the bot.

### Run with node
```sh
node index.js
```
### Run with pm2
```sh
npm install -g pm2@latest
pm2 start --name "discord-shift-swap" index.js --watch
```
