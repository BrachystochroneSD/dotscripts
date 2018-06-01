# Yet another Weather api shell script

Thoses script take weather data from random weather api service and print an output with an icon, humidity and temperature.

Cool for polybar or alike. You can set the update by calling the script inside your bar or creating a loop and let the script as a tray. (the dark sky is set with a loop as an example)

## Cool features:

Offline weather!
Thoses scripts curl datas for the current weather AND the forecast for the next days. It compare the time of the computer with the list of forecasted daily weather and choose the right day/hour. So.. yeah, it's not very accurate if the last updates of datas past two weeks, but it 


## List of dependencies :
+ Python
+ curl
+ jq
+ Weather-icon

## Parameters

+ APIkey/AppID : It's the key that you need to paste from your account on the Weather API website. 
+ datas files location : Just where your want to pur your datas
+ for Darksky only : UTC zone (in hour)

## Two script ?

There's two script with similar functions. The API weather website is just different. I thought the Darksky api wasn't very accurate and then I change to openweathermap.com. But now I think it's pretty much the same whit very little differences :

+ Darksky :
  - The forecast is daily, so the tempMin and tempMax are very different so I prefer to show the two of them.
  - One data file.
  - More icon
  - UTC zone must be set!!


+ OpenWeatherMap :
  - Here, the forecast is by hour, so much accurate and then I prefer to show the round integer between tempMin and Max.
  - The datas are splitted into "current" and "forecast".

## Polybar config

For example :
```
[bar/Bar]
font-3 = Weather Icons:size=12;2

[module/weather]
type = custom/script
exec = ~/.script/weatherdir/weather
format-underline = ${colors.pink}
format-font= 4
interval = 1800

```