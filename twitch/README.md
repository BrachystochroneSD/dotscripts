# Twitch Shell Script

This is a simple script that use the twitch api to access streams on twitch without:
  + Open a Browser
  + Acceding the Twitch website
  + Mute all the crap on the front page of the website
  + Vewing all the shitty ads on the site
  + Lost 20 minutes of your life doing useless thing just to check if your favorite streamer is live.

All you have to do is run one of the two script
  + twitchlive: if you want to check the list of your favorite streamer
  + twitchgames: If you want to check the stream on for a certain game.


# Dependencies:
  + Bash 4
  + mpv (0.14.0)
  + youtube-dl
  + firefox (or other browser than can launch url on a new windows)
  + dmenu (This shit is awesome)
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
    + Gamedatabase (cf gamedbupdate script)
    
# TODO:
  + Make one unique script