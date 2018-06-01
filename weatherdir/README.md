# Yet another Weather api shell script

Thoses script take weather data from random weather api service and print an output with an icon, humidity and temperature.

Cool for polybar or alike.

## Cool features:

Offline weather!
Thoses scripts curl datas for the current weather AND the forecast for the next days. It compare the time of the computer with the list of forecasted daily weather and choose the right day/hour. So.. yeah, it's not very accurate if the last updates of datas past two weeks, but it's better than nothing 


## List of dependencies:
+ Python
+ curl
+ jq
+ Weather-icon (or similar but you need to change the icon for each weather description)

## Parameters

+ APIkey/AppID : It's the key that you need to paste from your account on the Weather API website. 
+ datas files location : Just where your want to pur your datas
+ for Darksky only : UTC zone (in hour)

## Two script?

There's two script with similar functions. The API weather website is just different. I thought the Darksky api wasn't very accurate and then I changed to openweathermap.com. But now I think it's pretty much the same whith very little differences:

+ Darksky:
  - Daily forecast for the week
  - One data file
  - UTC zone must be set!!


+ OpenWeatherMap:
  - Daily forecast by hour, so much accurate (and then I prefer to show the round integer between tempMin and tempMax)
  - The datas are splitted into "current" and "forecast"

## Polybar config

Example:
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