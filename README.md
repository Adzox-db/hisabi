<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>حساباتي</title>

<style>
*{
box-sizing:border-box;
margin:0;
padding:0;
}

body{
font-family:Arial,sans-serif;
background:linear-gradient(135deg,#eef2ff,#f8fafc);
color:#172033;
min-height:100vh;
}

header{
background:linear-gradient(135deg,#4f46e5,#7c3aed,#06b6d4);
color:white;
padding:20px;
text-align:center;
box-shadow:0 5px 20px #0002;
}

header h1{
font-size:30px;
}

.container{
max-width:700px;
margin:50px auto;
padding:20px;
}

.title{
text-align:center;
margin-bottom:30px;
}

.title h2{
font-size:32px;
color:#4f46e5;
margin-bottom:10px;
}

.title p{
color:#64748b;
}

/* القائمة */

.menu{
display:flex;
flex-direction:column;
gap:15px;
}

.menu a{
text-decoration:none;
background:white;
padding:20px;
border-radius:18px;
display:flex;
align-items:center;
justify-content:space-between;
color:#172033;
font-size:19px;
font-weight:bold;

box-shadow:0 8px 25px #0000000d;

border:2px solid transparent;

transition:.3s;

animation:appear .6s ease backwards;
}

.menu a:nth-child(2){
animation-delay:.1s;
}

.menu a:nth-child(3){
animation-delay:.2s;
}

.menu a:nth-child(4){
animation-delay:.3s;
}

.menu a:nth-child(5){
animation-delay:.4s;
}

.menu a:hover{
transform:translateX(-8px);
border-color:#6366f1;
box-shadow:0 12px 30px #4f46e533;
}

.icon{
font-size:28px;
}

.arrow{
font-size:25px;
color:#4f46e5;
transition:.3s;
}

.menu a:hover .arrow{
transform:translateX(-7px);
}

/* الأقسام */

.section{
display:none;
margin-top:25px;
background:white;
padding:25px;
border-radius:20px;
box-shadow:0 10px 30px #0001;
animation:appear .4s ease;
}

.section:target{
display:block;
}

.section h2{
color:#4f46e5;
margin-bottom:20px;
}

input{
width:100%;
padding:13px;
margin:7px 0;
border:2px solid #e2e8f0;
border-radius:10px;
font-size:16px;
outline:none;
}

button{
width:100%;
padding:13px;
border:0;
border-radius:10px;
background:linear-gradient(135deg,#4f46e5,#7c3aed);
color:white;
font-size:17px;
font-weight:bold;
cursor:pointer;
margin-top:10px;
}

.result{
margin-top:15px;
color:#4f46e5;
font-weight:bold;
text-align:center;
}

.back{
display:block;
text-align:center;
margin-top:15px;
color:#4f46e5;
text-decoration:none;
font-weight:bold;
}

footer{
margin-top:60px;
padding:25px;
text-align:center;
background:#111827;
color:white;
}

@keyframes appear{
from{
opacity:0;
transform:translateY(25px);
}
to{
opacity:1;
transform:translateY(0);
}
}

@media(max-width:600px){
.container{
margin:30px auto;
}

.title h2{
font-size:27px;
}

.menu a{
font-size:17px;
padding:17px;
}
}
</style>
</head>

<body>

<header>
<h1>🧮 حساباتي</h1>
</header>

<div class="container">

<div class="title">
<h2>شنو بغيتي تحسب؟</h2>
<p>اختار الأداة اللي محتاج</p>
</div>

<div class="menu">

<a href="#percentage">
<span><span class="icon">📊</span> اضغط هنا لحساب النسبة المئوية</span>
<span class="arrow">←</span>
</a>

<a href="#discount">
<span><span class="icon">💰</span> اضغط هنا لحساب التخفيض</span>
<span class="arrow">←</span>
</a>

<a href="#average">
<span><span class="icon">🎓</span> اضغط هنا لحساب المعدل الدراسي</span>
<span class="arrow">←</span>
</a>

<a href="#calculator">
<span><span class="icon">🧮</span> اضغط هنا للحاسبة</span>
<span class="arrow">←</span>
</a>

<a href="#about">
<span><span class="icon">ℹ️</span> اضغط هنا لمعرفة المزيد</span>
<span class="arrow">←</span>
</a>

</div>


<!-- النسبة -->

<div class="section" id="percentage">

<h2>📊 حساب النسبة المئوية</h2>

<input id="p" type="number" placeholder="النسبة %">

<input id="n" type="number" placeholder="العدد">

<button onclick="calcPercent()">احسب</button>

<div class="result" id="pr"></div>

<a class="back" href="#">↩️ رجوع للقائمة</a>

</div>


<!-- التخفيض -->

<div class="section" id="discount">

<h2>💰 حساب التخفيض</h2>

<input id="price" type="number" placeholder="الثمن">

<input id="disc" type="number" placeholder="نسبة التخفيض %">

<button onclick="calcDiscount()">احسب</button>

<div class="result" id="dr"></div>

<a class="back" href="#">↩️ رجوع للقائمة</a>

</div>


<!-- المعدل -->

<div class="section" id="average">

<h2>🎓 حساب المعدل</h2>

<input id="g1" type="number" placeholder="النقطة الأولى">

<input id="g2" type="number" placeholder="النقطة الثانية">

<input id="g3" type="number" placeholder="النقطة الثالثة">

<button onclick="calcAverage()">احسب المعدل</button>

<div class="result" id="ar"></div>

<a class="back" href="#">↩️ رجوع للقائمة</a>

</div>


<!-- الحاسبة -->

<div class="section" id="calculator">

<h2>🧮 حاسبة بسيطة</h2>

<input id="num1" type="number" placeholder="الرقم الأول">

<input id="num2" type="number" placeholder="الرقم الثاني">

<button onclick="operation('+')">➕ جمع</button>

<button onclick="operation('-')">➖ طرح</button>

<button onclick="operation('*')">✖️ ضرب</button>

<button onclick="operation('/')">➗ قسمة</button>

<div class="result" id="cr"></div>

<a class="back" href="#">↩️ رجوع للقائمة</a>

</div>


<!-- عن الموقع -->

<div class="section" id="about">

<h2>ℹ️ عن حساباتي</h2>

<p>
حساباتي موقع مجاني كيقدم أدوات بسيطة
للحساب والدراسة بطريقة سهلة وسريعة.
</p>

<br>

<p>
غادي نزيدو أدوات جديدة مستقبلاً.
</p>

<a class="back" href="#">↩️ رجوع للقائمة</a>

</div>

</div>

<footer>
© 2026 حساباتي
</footer>


<script>

function calcPercent(){

let p=Number(document.getElementById("p").value);
let n=Number(document.getElementById("n").value);

if(isNaN(p)||isNaN(n)){
document.getElementById("pr").innerHTML="⚠️ دخل المعلومات";
return;
}

document.getElementById("pr").innerHTML=
"✅ النتيجة: "+((p*n)/100).toFixed(2);
}


function calcDiscount(){

let price=Number(document.getElementById("price").value);
let disc=Number(document.getElementById("disc").value);

if(price<=0||disc<0||disc>100){
document.getElementById("dr").innerHTML=
"⚠️ تأكد من المعلومات";
return;
}

let saving=price*disc/100;
let finalPrice=price-saving;

document.getElementById("dr").innerHTML=
"💸 التوفير: "+saving.toFixed(2)+" درهم<br><br>"+
"💰 الثمن النهائي: "+finalPrice.toFixed(2)+" درهم";
}


function calcAverage(){

let a=Number(document.getElementById("g1").value);
let b=Number(document.getElementById("g2").value);
let c=Number(document.getElementById("g3").value);

if(isNaN(a)||isNaN(b)||isNaN(c)){
document.getElementById("ar").innerHTML=
"⚠️ دخل جميع النقط";
return;
}

let avg=(a+b+c)/3;

document.getElementById("ar").innerHTML=
"🎓 المعدل: "+avg.toFixed(2);
}


function operation(op){

let a=Number(document.getElementById("num1").value);
let b=Number(document.getElementById("num2").value);
let result;

if(op==="+") result=a+b;
if(op==="-") result=a-b;
if(op==="*") result=a*b;

if(op==="/"){
if(b===0){
document.getElementById("cr").innerHTML="⚠️ لا يمكن القسمة على صفر";
return;
}
result=a/b;
}

document.getElementById("cr").innerHTML=
"✅ النتيجة: "+result;
}

</script>

</body>
/html># hisabi