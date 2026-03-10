<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Fishing RPG MAX</title>

<style>
body{
margin:0;
font-family:Arial;
background:#87CEEB;
text-align:center;
}

#game{
width:100vw;
height:60vh;
background:linear-gradient(#4facfe,#00f2fe);
position:relative;
overflow:hidden;
}

.fish{
width:50px;
height:30px;
border-radius:20px;
position:absolute;
bottom:80px;
}

.hpbg{
width:50px;
height:6px;
background:#333;
position:absolute;
}

.hp{
height:6px;
background:red;
}

#hook{
width:5px;
height:90px;
background:black;
position:absolute;
top:0;
left:50%;
display:none;
}

button{
margin:3px;
padding:6px;
}

</style>
</head>

<body>

<h3>
💰 <span id="money">0</span> |
🐟 Kho: <span id="bag">0</span> |
🎣 Damage: <span id="dmg">5</span> |
🗺 <span id="map">Biển nông</span>
</h3>

<div id="game">
<div id="hook"></div>
</div>

<button onclick="sell()">Bán cá</button>
<button onclick="upgrade()">Tăng damage (50)</button>
<button onclick="changeMap()">Đổi map</button>
<button onclick="changeChar()">Đổi nhân vật</button>

<p>Chạm màn hình để câu</p>

<script>

let game=document.getElementById("game")

let player={
money:0,
fish:0,
damage:5,
map:0,
char:0
}

let maps=[
{name:"Biển nông",mult:1},
{name:"Biển sâu",mult:2},
{name:"Dung nham",mult:3}
]

let chars=[
{name:"Ngư dân",bonus:0},
{name:"Thợ săn",bonus:3},
{name:"May mắn",bonus:0}
]

let fishes=[]

function spawnFish(){

let fish=document.createElement("div")
fish.className="fish"

let hpbg=document.createElement("div")
hpbg.className="hpbg"

let hp=document.createElement("div")
hp.className="hp"

hpbg.appendChild(hp)

game.appendChild(fish)
game.appendChild(hpbg)

let type=Math.random()

let hpVal=20
let value=10
let color="orange"

if(type>0.7){
hpVal=40
value=25
color="green"
}

if(type>0.9){
hpVal=80
value=80
color="purple"
}

fish.style.background=color

fishes.push({
x:Math.random()*window.innerWidth,
hp:hpVal,
max:hpVal,
value:value,
fish:fish,
hp:hp,
hpbg:hpbg
})

}

for(let i=0;i<5;i++) spawnFish()

function moveFish(){

fishes.forEach(f=>{

f.x+=2

if(f.x>window.innerWidth){
f.x=-50
}

f.fish.style.left=f.x+"px"
f.hpbg.style.left=f.x+"px"
f.hpbg.style.bottom="115px"

f.hp.style.width=(f.hp/f.max)*50+"px"

})

}

setInterval(moveFish,30)

let hook=document.getElementById("hook")
let dropping=false

game.addEventListener("touchstart",dropHook)
game.addEventListener("click",dropHook)

function dropHook(){

if(dropping) return

dropping=true

hook.style.display="block"
hook.style.top="0px"

let fall=setInterval(()=>{

let top=parseInt(hook.style.top)

if(top>window.innerHeight*0.55){

clearInterval(fall)
hook.style.display="none"
dropping=false

}else{

hook.style.top=top+8+"px"
hit()

}

},20)

}

function hit(){

let hookTop=parseInt(hook.style.top)
let hookX=window.innerWidth/2

fishes.forEach(f=>{

if(
hookTop>window.innerHeight*0.45 &&
f.x>hookX-30 &&
f.x<hookX+30
){

f.hp-=player.damage+chars[player.char].bonus

if(f.hp<=0){

player.fish++
player.money+=f.value*maps[player.map].mult

f.hp=f.max
f.x=-50

updateUI()

}

}

})

}

function sell(){

player.money+=player.fish*10
player.fish=0
updateUI()

}

function upgrade(){

if(player.money>=50){

player.money-=50
player.damage+=2
updateUI()

}

}

function changeMap(){

player.map++
if(player.map>=maps.length) player.map=0

updateUI()

}

function changeChar(){

player.char++
if(player.char>=chars.length) player.char=0

updateUI()

}

function updateUI(){

money.innerText=player.money
bag.innerText=player.fish
dmg.innerText=player.damage
map.innerText=maps[player.map].name

}

function save(){
localStorage.setItem("fishmax",JSON.stringify(player))
}

function load(){

let data=JSON.parse(localStorage.getItem("fishmax"))

if(data) player=data

}

load()
updateUI()

setInterval(save,3000)

</script>

</body>
</html>
