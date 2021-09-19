## Setup
###
1. To use the API we must get the oAuth
2. The oAuth key must be stored in a .env file inside the same directory as the source code
3. I had to download pip, and python3 to use this code.  I had to install python-dotenv to allow environment variables to be pulled from the .env file and discord.py to use discord API functions.  I also had to add sources to the /etc/apt/sources-.list using this thread https://askubuntu.com/questions/1254309/not-installing-pip-on-ubuntu-20-04

## Usage
###
- If you type in '!princess', my bot will spit out a random princess bride quote into the terminal as well as the original functionality

## Research 
###
To run this bot without needing an active terminal connection and the script running, I could:

clone the repo and set up the .env on a new machine we have for this course, then run the script in the background using &