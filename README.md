<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="HNGx.css" />
    <title>HNGx</title>
    </head>
    <body> 
       <div class="picture">
        <div class="profile">
         
        <div>
            <div class="bio">
            <h1 data-testid="slackUserName">Okanlawon Suliyat</h1>
            <img src="suliyat.jpg" alt="Abisola07"
            data-testid="slackDisplayImage"/>
            <p id="day"data-testid="current day of the week"></p>
            <p id="time"data-testid="currentUTCTime""></p>
            <p data-testid="myTrack">TRACK:FRONTEND</p>
            <a href="https://github.com/Suliyat07"data-testid="githubURL">GitHub</a>
        </div>
        <script src="HNGx.js"></script>
    </body>
    </head>



body {
    background-color :green;
}
.picture{
    width: 100px;
    height: 100px;
    border-radius: 50%;
    border:5px;    
}
.profile {
  background-color: green;
  border-radius: 20px;
  padding: 40px;
  width: fit-content;
  height: auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.picture img {
  width: 150%;
  height: 300%;
  display: block;
}
.bio {
  margin-top: 10px;
  display: flex;
  flex-direction: column;
  align-items: center;
  align-content: space-around;
}
a {
  border: 5px;
  border-radius: 10px;
  background-color: green;
  padding: 10px;
  color:white;
  font-weight: bold;
  font-size: medium;
}


// Days 
const date = new Date();
const currentDate = date.getUTCDay();
const days = [
  "Sunday",
  "Monday",
  "Tuesday",
  "Wednesday",
  "Thursday",
  "Friday",
  "Saturday",
];
const currentDay = days[currentDate];
// Display the Day
document.getElementById(
  "day"
).innerHTML = `<b> Day Of The Week:</b> ${currentDay}`;
// Time Js
function seconds() {
  const date = new Date();
  const currentTime = date.getTime();
  document.getElementById(
    "time"
  ).innerHTML = `<b> UTC Time: </b>  ${currentTime}`;
}
// An interval to update the seconds every 1000 seconds
setInterval(seconds, 1000);
