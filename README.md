# Glass-Digital-Clock

**Note:** This Project uses [Javascript](https://www.javascript.com/).

This repo contains an example of a Glass Digital Clock

## Features

- A simple HTML interigation (Using Div Classes)
- Seconds, minutes, hours, date, day
- AM & PM

## Java Script (Clock)

```javascript
var time = document.getElementById("time");  //HTML div class use
var day = document.getElementById("day"); //HTML div class use
var midday = document.getElementById("midday"); //HTML div class use

var clock = setInterval(
    function calcTime(){
        var date_now = new Date(); //Current Date
        var hr = date_now.getHours(); //Hours
        var min = date_now.getMinutes(); //Minutes
        var sec = date_now.getSeconds(); //Seconds
        var middayValue = "AM"
        var days = ["Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday"]; //Days of the week
```
Note: Don't forget to import javascript, or else it won't load this script `<script src="script.js"></script>` put this `HTML` code

## Java Script (Value To Text)

```javascript   
        day.textContent = days[date_now.getDay()];

        middayValue = (hr >= 12) ? "PM" : "AM"; //Checks if PM or AM

        if(hr == 0){
            hr = 12;
        }
        else if(hr > 12){
            hr-=12;
        }

        hr = (hr < 10) ? "0" + hr : hr;
        min = (min < 10) ? "0" + min : min;
        sec = (sec < 10) ? "0" + sec : sec;

        time.textContent = hr + ":" + min + ":" + sec;
        midday.textContent = middayValue;
    },
    1000
);
```

## HTML (Help)

```html
<div class="clock"> // imports css class  
<div id="day"></div> // Day of the week
<div class="wrapper"> 
<div id="time"></div> // Time: Hour, Mins, Seconds
<div id="midday"></div> // AM or PM
```

## Usage

Feel free to `copy and code`, but be sure to give me credit for the base code!
