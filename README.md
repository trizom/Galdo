# Galdo
<!DOCTYPE html>
<html lang=“en”>
<head>
<title>PacMan</title>
<style>
/*All of our CSS code goes here… */
* {
   /* outline 1px dotted purple;   */
}

.pacman {
width: 50px;
height: 50px;
background-image: url(‘pacman.pgn’);
display: inline-block;
}

.wall {
width: 50px;
Height: 50px;
background-image: url(‘wall.pgn’);
display: inline-block;
}

.coin {
width: 50px;
height: 50px;
background-image: url(‘coin.pgn’);
display: inline-block;
}

.ground {
width: 50px;
height: 50px;
background-image: url(‘ground.pgn’);
display: inline-block;
}

div {
line-height: 0px;
margin: -2px;
vertical-align: top;
}

/*End of CSS */
</style>
</head>
<body>
<!— All of our HTML code goes here… —>

<div id=‘world’></div>
<!— … —>

<div class=‘wall’></div>
<div class=‘wall’></div>
<div class=‘wall’></div>
<div class=‘wall’></div>
<div class=‘wall’></div>
<br>
<div class=‘wall’></div>
<div class=‘pacman’></div>
<div class=‘ground’></div>
<div class=‘coin’></div>
<div class=‘wall’></div>
<br>
<div class=‘wall’></div>
<div class=‘wall’></div>
<div class=‘wall’></div>
<div class=‘wall’></div>
<div class=‘wall’></div>

<!— End of HTML—>
</body>
<script>
// All of our JavaScript code goes here…

// 1 = <div class=‘wall’></div>
// 2 = <div class=‘ground’></div>
// 3 = <div class=‘coin’></div>
// 5 = <div class=‘pacman’></div>


Var map = [
[1,1,1,1,1,1,1,1,1,1,1,1,1],
[1,2,2,2,2,2,1,2,2,2,2,2,1],
[1,2,1,1,1,2,1,2,1,1,1,2,1],
[1,2,1,2,2,2,2,2,2,2,1,2,1],
[1,2,2,2,1,1,5,1,1,2,2,2,1],
[1,2,1,2,2,2,2,2,2,2,1,2,1],
[1,2,1,1,2.2,1,2,2,1,1,2,1],
[1,2,2,2,2,2,1,2,2,2,2,2,1],
[1,1,1,1,1,1,1,1,1,1,1,1,1],
]
var pacman = {
x: 6;
Y: 4;
}

// algorithm codingdojo.com
// console.log(document);

function drawWorld() {
document.getElementById(‘world’).innerHTML = “”;
for(var y = 0; y< map.length; y = y +1 ) {
// Console.log(map[y])
for(var x = 0; x < map[y]; x = x + 1){
console.log(map y] [x])
if (map [y] [x] === 1) {

document.getElementById(‘world’).innerHTML += “<div class=‘wall’></div>”;
}
else if (map[y] [x] === 2){
document.getElementById(‘world’).innerHTML += “<div class=‘coin’></div>”;
}
else if (map[y] [x] === 3){
document.getElementById(‘world’).innerHTML += “<div class=‘ground’></div>”;
}
else if (map[y] [x] === 5){
document.getElementById(‘world’).innerHTML += “<div class=‘pacman’></div>”;
}
}
document.getElementById(‘world’).innerHTML += “<br>”;
}
}

document.onkeydown = function(e){
console.log(e.keyCode);
if (e.keyCode === 37){
// left
if (map[pacman.y][pacman.x-1] !== 1){
if (map[pacman.y][pacman.x-1] === 2){
 Score = score + 10;
}
map[pacman.y] [pacman.x] = 3;
pacman.x = pacman.x - 1;
map[pacman.y] [pacman.x] = 5;
drawWorld();
}
}
else if (e.keyCode === 38){
// up
if (map[pacman.y-1][pacman.x] !== 1){
map[pacman.y] [pacman.x] = 3;
pacman.y = pacman.y - 1;
map[pacman.y] [pacman.x] = 5;
drawWorld();
}
else if (e.keyCode === 39){
// right
if (map[pacman.y] [pacman.x+1] !== 1){
map[pacman.y][pacman.x] = 3;
pacman.x = pacman.x + 1;
map[pacman.y] [pacman.x] = 5;
drawWorld();
}
else if (keyCode === 40){
// down
if (map[pacman.y-1][pacman.x] !==1){
map[pacman.y] [pacman.x] = 3;
pacman.y = pacman.y + 1;
map[pacman.y] [pacman.x] = 5;
drawWorld();
}
}

drawWorld();


Function score(){
if()
}
