<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Orange Dynasty Streak Tracker</title>
<style>
/* General Styles */
body {
    font-family: 'Segoe UI', sans-serif;
    background: linear-gradient(120deg, #ffecd2, #fcb69f);
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
}
.container {
    max-width: 900px;
    width: 100%;
    padding: 20px;
    text-align: center;
}
h1 { color: #ff6600; margin-bottom: 10px; text-shadow: 2px 2px 4px rgba(0,0,0,0.2);}
.upload-section {
    background: rgba(255,255,255,0.9);
    padding: 20px;
    border-radius: 20px;
    margin-bottom: 30px;
    box-shadow: 0 10px 20px rgba(0,0,0,0.15);
}
.upload-section input[type="text"],
.upload-section input[type="file"],
.upload-section input[type="number"] {
    margin: 10px 0;
    padding: 12px;
    width: 70%;
    border-radius: 12px;
    border: 1px solid #ccc;
    font-size: 16px;
}
button {
    padding: 12px 25px;
    background: #ff6600;
    color: white;
    border: none;
    border-radius: 12px;
    cursor: pointer;
    font-weight: bold;
    font-size: 16px;
    margin-top: 10px;
    transition: transform 0.2s, box-shadow 0.2s;
}
button:hover {
    transform: scale(1.05);
    box-shadow: 0 6px 12px rgba(0,0,0,0.2);
}

/* Badge Section */
.badge-section {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
}
.badge {
    position: relative;
    border-radius: 20px;
    overflow: hidden;
    background: rgba(255,255,255,0.8);
    box-shadow: 0 8px 16px rgba(0,0,0,0.2);
    transition: transform 0.3s;
}
.badge:hover {
    transform: scale(1.05);
}
.badge img {
    display: block;
    width: 200px;
    height: 200px;
    object-fit: cover;
    border-bottom: 3px solid #ff6600;
}
.badge p {
    margin: 8px 0;
    font-weight: bold;
    color: #ff6600;
}
.badge button {
    font-size: 12px;
    margin: 4px;
    padding: 6px 12px;
}

/* Sparkle Animation */
.sparkle {
    position: absolute;
    width: 10px;
    height: 10px;
    border-radius: 50%;
    background: #fff700;
    opacity: 0.9;
    animation: sparkle 1s infinite;
}
@keyframes sparkle {
    0%, 100% { transform: scale(1) translate(0,0); opacity: 0.9; }
    50% { transform: scale(1.5) translate(5px,-5px); opacity: 0.4; }
}

/* Leaderboard */
.leaderboard-section {
    margin-top: 30px;
}
.leaderboard-section table {
    width: 90%;
    margin: 0 auto;
    border-collapse: collapse;
    background: rgba(255,255,255,0.9);
    border-radius: 15px;
    overflow: hidden;
}
.leaderboard-section th, .leaderboard-section td {
    padding: 12px;
    border: 1px solid #ff6600;
    text-align: center;
}
.leaderboard-section th {
    background: #ff6600;
    color: white;
    font-size: 18px;
}
</style>
</head>
<body>
<div class="container">
<h1>🍊 Orange Dynasty Streak Tracker</h1>

<div class="upload-section">
    <input type="text" id="username" placeholder="Enter username"><br>
    <input type="file" id="imageUpload" accept="image/*"><br>
    <input type="number" id="streakDays" placeholder="Enter streak days"><br>
    <button id="generateBadge">Generate Badge</button>
</div>

<div class="badge-section" id="badgesContainer"></div>

<div class="leaderboard-section">
    <h2>Leaderboard 🏆</h2>
    <table>
        <thead>
            <tr><th>Rank</th><th>Username</th><th>Days</th></tr>
        </thead>
        <tbody id="leaderboardTable"></tbody>
    </table>
</div>
</div>

<script>
const usernameInput = document.getElementById('username');
const imageUpload = document.getElementById('imageUpload');
const streakDaysInput = document.getElementById('streakDays');
const generateBadgeBtn = document.getElementById('generateBadge');
const badgesContainer = document.getElementById('badgesContainer');
const leaderboardTable = document.getElementById('leaderboardTable');

let badges = JSON.parse(localStorage.getItem('badges')) || [];
renderBadges();
renderLeaderboard();

generateBadgeBtn.addEventListener('click', () => {
    const username = usernameInput.value.trim();
    const file = imageUpload.files[0];
    const days = parseInt(streakDaysInput.value);
    if(!username || !file || !days){ alert("Fill all fields"); return; }
    const reader = new FileReader();
    reader.onload = function(e){
        createBadge(e.target.result, days, username, badgeURL=>{
            badges.push({username, img: badgeURL, days});
            localStorage.setItem('badges', JSON.stringify(badges));
            renderBadges();
            renderLeaderboard();
        });
    };
    reader.readAsDataURL(file);
});

function renderBadges(){
    badgesContainer.innerHTML='';
    badges.forEach((b,i)=>{
        const div=document.createElement('div');
        div.classList.add('badge');
        div.innerHTML=`
            <img src="${b.img}">
            <p>${b.username} - ${b.days} Day${b.days>1?'s':''}</p>
            <button onclick="deleteBadge(${i})">Delete</button>
            <button onclick="downloadBadge('${b.img}','${b.username}_${b.days}day.png')">Download</button>
        `;
        // Add sparkles for 100+ day streaks
        if(b.days>=100){
            for(let s=0;s<6;s++){
                const sparkle=document.createElement('div');
                sparkle.classList.add('sparkle');
                sparkle.style.top=Math.random()*200+'px';
                sparkle.style.left=Math.random()*200+'px';
                div.appendChild(sparkle);
            }
        }
        badgesContainer.appendChild(div);
    });
}

function deleteBadge(i){
    badges.splice(i,1);
    localStorage.setItem('badges',JSON.stringify(badges));
    renderBadges();
    renderLeaderboard();
}

function downloadBadge(dataURL,filename){
    const a=document.createElement('a');
    a.href=dataURL;
    a.download=filename;
    a.click();
}

function createBadge(imageSrc, days, username, callback){
    const canvas=document.createElement('canvas');
    const ctx=canvas.getContext('2d');
    const img=new Image();
    const icon=new Image();
    img.onload=()=>{
        canvas.width=img.width;
        canvas.height=img.height+70;
        ctx.shadowColor=getColor(days);
        ctx.shadowBlur=20;
        ctx.drawImage(img,0,0);
        ctx.shadowBlur=0;
        ctx.fillStyle=getColor(days);
        ctx.fillRect(0,0,canvas.width,50);
        ctx.fillStyle='#fff';
        ctx.font='bold 28px Arial';
        ctx.textAlign='center';
        ctx.fillText(`${days} Day${days>1?'s':''}`,canvas.width/2,32);
        icon.onload=()=>{
            ctx.drawImage(icon,canvas.width-40,10,30,30);
            callback(canvas.toDataURL());
        };
        if(days>=100) icon.src='https://upload.wikimedia.org/wikipedia/commons/thumb/f/f4/Star_icon-72a7cf.svg/64px-Star_icon-72a7cf.svg.png';
        else if(days>=50) icon.src='https://upload.wikimedia.org/wikipedia/commons/thumb/5/55/Diamond_icon.png/64px-Diamond_icon.png';
        else if(days>=30) icon.src='https://upload.wikimedia.org/wikipedia/commons/thumb/1/16/Platinum_icon.png/64px-Platinum_icon.png';
        else icon.src='https://upload.wikimedia.org/wikipedia/commons/thumb/5/5a/Trophy_icon.png/64px-Trophy_icon.png';
    };
    img.src=imageSrc;
}

function getColor(days){
    if(days>=100) return '#ff00ff';
    if(days>=50) return '#00ffff';
    if(days>=30) return '#e5e4e2';
    if(days>=15) return '#ffd700';
    if(days>=5) return '#c0c0c0';
    return '#cd7f32';
}

function renderLeaderboard(){
    leaderboardTable.innerHTML='';
    const sorted=[...badges].sort((a,b)=>b.days-b.days);
    sorted.forEach((b,i)=>{
        const tr=document.createElement('tr');
        tr.innerHTML=`<td>${i+1}</td><td style="color:${getColor(b.days)}">${b.username}</td><td>${b.days}</td>`;
        leaderboardTable.appendChild(tr);
    });
}
</script>
</body>
</html>
