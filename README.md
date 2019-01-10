when setting the export variables, don't actually include quotes in client id and secret 
when asked for the redirect uri, raw copy the uri you were directed to 
set redirect uri to localhost
# sbotipy.py
This is a reddit bot that fetches top daily song posts from the subreddit r/ListenToThis and generates a spotify playlist with those songs. Lots of great music is on the subreddit and this makes discovering new songs much easier. 

## Requirements/Installation
Praw: pip install praw  
Spotipy: pip install spotipy

Register a reddit app at https://www.reddit.com/prefs/apps/ and input that information into the praw.ini file.  
Register a spotify developer app and set the redirect uri to something like localhost.   
Set the following environmental variables with the following console commands (but don't actually include quotes):  
export SPOTIPY_CLIENT_ID=''  
export SPOTIPY_CLIENT_SECRET=''  
export SPOTIPY_REDIRECT_URI=http://localhost:8888/callback/  

## How To Use
python sbotipy.py username numberOfSongs 

* specify the username you want to create the playlist for 
* specify the number of songs you want to add from r/ListenToThis 
  
When you run the script for the first time, it will open an authentication portal in the browser, than redirect you to a url. Copy and paste that url into the command line like the script prompts.

### Example
python sbotipy.py 'Isaac Na' 10

