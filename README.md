# Countdown
<!DOCTYPE HTML>
<html>
<body>
<p Id="demo"></p>
<p Id="eD"></p>
<p Id="cD"></p>
<p Id="e"></p>
<p Id="f"></p>
<p Id="g"></p>
<button onclick="clearInterval(jinx)">Stop Time</button>
<button onclick = "setInterval(Clock,1000)">Restart </button>
<script>
{
var currentDate = new Date();
var endDate = new Date("May 1, 2018 00:00:00");
document.getElementById("demo").innerHTML = currentDate;
document.getElementById("eD").innerHTML = endDate;
var countDown = endDate - currentDate ;



}

var jinx = setInterval(Clock,1000);
function Clock()
{

if(countDown>0)
countDown=countDown-1000;
var sec = (countDown)/1000 ;
var S = Math.floor(sec);
var min = sec/60;
var M = Math.floor(min);
var hour = min/60 ;
var H = Math.floor(hour);
var day = hour/24;
var D = Math.floor(day);
var year = day/365; 
var Y = Math.floor(year);
var D1 = D - Y*365;
var H1 = H - D*24;
var M1 = M - H*60;
var S1 = S - M*60;
document.getElementById("f").innerHTML = Y + ":" + D1 + ":" + H1 + ":" + M1 + ":" +  S1 ;

return countDown ;
}
var gin = setInterval(Gimme,1000);
function Gimme()
{
var d = new Date();
document.getElementById("g").innerHTML = d ;
}
</script>
</body>
</html>

