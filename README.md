# sbotipy.py
This is a reddit bot that fetches top daily song posts from the subreddits r/ListenToThis and r/Music and generates a spotify playlist with those songs. 
Lots of great music is on these subreddits, but posted as an inconvenient youtube link, and this makes discovering new songs much easier. 

## Requirements/Installation
Praw: pip install praw  
Spotipy: pip install spotipy

Register a reddit app at https://www.reddit.com/prefs/apps/ and input that information into the praw.ini file.  
Register a spotify developer app and set the redirect uri to something like http://localhost:8888/callback.     
It is very important that the redirect URI is the exactly the same in both your spotify app settings and env variables in the following step. 
Set the following environmental variables with the following console commands (but don't actually include quotes):  
export SPOTIPY_CLIENT_ID=''  
export SPOTIPY_CLIENT_SECRET=''  
export SPOTIPY_REDIRECT_URI=http://localhost:8888/callback  

## How To Use
python sbotipy.py username subreddit numberOfSongs flairFilter

* specify the username you want to create the playlist for 
* specify the subreddit (either ListenToThis or Music)
* specify the number of songs you want to add 
* specify the flair you want to filter by, this is optional (e.g. 'Music Streaming' flair for r/Music) 
  
When you run the script for the first time, it will open an authentication portal in the browser, than redirect you to a url. Copy and paste that url into the command line like the script prompts, even if it looks like the URL is an unfound page.

### Example
python sbotipy.py 'Isaac Na' 'music' 10 'Music Streaming'

