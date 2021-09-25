## Setup
###
1. To use the API we must get the oAuth from the discord developer page online by signing up with our profile.
2. The oAuth token must be stored in a .env file inside the same directory as the source code
3. I had to download pip, and python3 to use this code.  I had to install python-dotenv to allow environment variables to be pulled from the .env file and discord.py to use discord API functions.  I also had to add sources to the /etc/apt/sources-list using this thread https://askubuntu.com/questions/1254309/not-installing-pip-on-ubuntu-20-04
###
	-to install python and pip I used sudo apt install python3; sudo apt install python3-pip
	-to install the discord api I used pip install -U discord.py
	-to install dotenv I used pip install -U python-dotenv
## Usage
###
- If you type in '!princess', my bot will spit out a random princess bride quote into the terminal as well as the original functionality.
- If you type !princess you may get "wuv true wuv" or "INCONCIEVABLE"
## Research 
###
To run this bot without needing an active terminal connection and the script running, I could:

- clone the repo and set up the .env on a new machine or the aws instance we have for this course, then run the script in the background using &.  This will cause the program (bot) to run in the background and allow the terminal to continue being used, the program will also continue running after a logout from the system.  You would have to use the kill command I believe to terminate this one.

OR:

- you could run the bot inside a screen.  I am adding this in after lecture because you mentioning this in lecture reminded me that a few years ago my Mordhau server I hosted with the same friend I am hosting Ark with we ran through screens.  We used it to host 2 instances of Mordhau server and still be able to switch between it and the original terminal.  This would achieve a very similar outcome to the one above, however, you would essentially have a terminal window you can access through commands to view the terminal that the bot is running in.  When we used this on a mordhau server it was because the game spat stuff out to the terminal that during normal operation was pointless to have clogging up the terminal, however, when things were not "normal operation" it helped to see these things in real time rather than checking a log file.  So, the screen allowed us to view the chain of messages when we wanted to, and ignore it when we didn't.
