## Setup
###
1. To use the API we must get the oAuth from the discord developer page online by signing up with our profile.
2. The oAuth key must be stored in a .env file inside the same directory as the source code
3. I had to download pip, and python3 to use this code.  I had to install python-dotenv to allow environment variables to be pulled from the .env file and discord.py to use discord API functions.  I also had to add sources to the /etc/apt/sources-list using this thread https://askubuntu.com/questions/1254309/not-installing-pip-on-ubuntu-20-04

## Usage
###
- If you type in '!princess', my bot will spit out a random princess bride quote into the terminal as well as the original functionality

## Research 
###
To run this bot without needing an active terminal connection and the script running, I could:

clone the repo and set up the .env on a new machine or the aws instance we have for this course, then run the script in the background using &.

OR:

you could run the bot inside a screen.  I am adding this in after lecture because you mentioning this in lecture reminded me that a few years ago my Mordhau server I hosted with the same friend I am hosting Ark with we ran through screens.  We used it to host 2 instances of Mordhau server and still be able to switch between it and the root terminal.
