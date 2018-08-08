# Twitch Shell Script

This is a simple script that use the twitch api to access streams on twitch without:
  + Open a Browser
  + Go to the Twitch website by typing on the address bar or clicking on your bookmark
  + Mute all the crap video that autostart on the front page of twitch
  + See all the shitty ads
  + Lost 2 minutes of your life just to check if your favorite streamer is live.

All you have to do is run this script with one of the two options
  + twitchscript --live: if you want to check the list of your favorite streamer that are online
  + twitchscript --game: If you want to check the stream on for a certain game.
  + twitchscript --vod: If you want to browse and choose the VODs of a channel.

**YOU DON'T EVEN NEED A TWITCH ACCOUNT!**

# Gif to show the power or that shit

![test](https://media.giphy.com/media/8FffLJPtHZaJ1KDHom/giphy.gif)

# Dependencies:
  + Bash 4
  + mpv (0.14.0)
  + youtube-dl
  + firefox (or other browser than can launch url on a new windows)
  + [dmenu](https://tools.suckless.org/dmenu/) (This shit is awesome)
  + internet connection (ok.)

# Parameters:
  + Client ID for twitch (more infos on https://blog.twitch.tv/client-id-required-for-kraken-api-calls-afbb8e95f843)
  + Datas location for
    + List of desired channel
      In the form of
      ```
      channel1,channel2,channel3,...
      ```
    + List of fav games
      In the form of
      ```
      Games1
      Games2
      Games3
      Games4
      
      ```
    + Gamedatabase (cf https://github.com/BrachystochroneSD/dotscripts/tree/master/gamedatabase)
    
# TODO:
  + Use Chatty or Streamlink or something to access the chat without using the browser.
  + Fix the problem of hosted stream
  + Optimisation