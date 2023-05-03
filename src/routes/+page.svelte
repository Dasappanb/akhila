<script>
	import Counter from './Counter.svelte';
	import welcome from '$lib/images/svelte-welcome.webp';
	import welcome_fallback from '$lib/images/svelte-welcome.png';
</script>

<!DOCTYPE html>
<html lang="en">
<head>
<title>BMI Calculator | Home</title>
<link rel="icon" type="image/x-icon" href="/thumbnails/favicon.jpeg"/>
<meta charset="utf-8">
<meta http-equiv="X-UA-Compatiable" content="IE=edge">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<link rel="preconnect"
href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link
href="https://fonts.googleapis.com/css2?family=Barlow:
wght@900&display=swap" rel="stylesheet">
<link rel="stylesheet" href="style.css">
<script src="script.js"></script>
</head>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link
href="https://fonts.googleapis.com/css2?family=Barlow:
wght@900&display=swap" rel="stylesheet"><body>
<header>
<h1>BMI Calculator</h1>
<h6>Be healthy</h6>
<br>
<hr>
</header>
<div class="col">
<section>
<div class="container">
<p>Move the slider to find your BMI ⇄
</p><br>
<div class="row">
<input type="range" min="20" max="150" value="20" id="weight" oninput="calculate()">
<span id="weight-val">20
KG</span>
</div>
<div class="row">
<input type="range" min="100" max="230" value="100", id="height" oninput="calculate()">
<span id="height-val">100
CM</span>
</div>
<div class="res1">
<p id="result"></p>
<p id="category"></p>
</div>
</div>
</section>
<article>
<h2>What is BMI</h2>
<p>
<b>BMI (body mass index)</b> is a
calculated number representing a person's level of fat or
obesity level. According to the Centers for Disease Control
and Prevention (CDC), a BMI of 30 or above indicates
obesity. A high BMI can indicate high body fatness. BMI
screens for weight categories that may lead to health
problems, but it does not diagnose the body fatness
or health of an individual. </p><br>
<h3>Calculating BMI: The Formula</h3>
The formula to calculate BMI requires
information about a person's height in meters and weight
in kilograms. For weight
in pounds and height in inches, there is a
different formula, but due to rounding, it may not produce
the exact same results. The BMI formula is:<br><br>
<i>BMI = weight (in kilograms) / height (in
meters) ^2</i>
<br><br><br>


<br>
<h3>How is BMI used ?</h3>
<p>
BMI can be a screening tool, but it does not
diagnose the body fatness or health of an individual. To determine if BMI is a health risk, a
healthcare provider performs further assessments. Such assessments include skinfold
thickness measurements, evaluations of diet, physical
activity, and family history. </p>
<br>
<h3 class="overweight">Risks associated with
being overweight</h3>
<p>
Being overweight increases the risk of a
number of serious diseases and health conditions. Below
is a list of said risks, according to the Centers for Disease
Control and Prevention (CDC):
<ul>
<li>High blood pressure</li>
<li>Higher levels of LDL cholesterol, which is widely considered "bad cholesterol," lower levels
of HDL cholesterol, considered to be good cholesterol in
moderation, and high levels of triglycerides</li>
<li>Type II diabetes</li>
<li>Coronary heart disease</li>
<li>Stroke</li>
<li>Gallbladder disease</li>
<li>Osteoarthritis, a type of joint disease
caused by breakdown of joint cartilage</li>
<li>Sleep apnea and breathing
problems</li>
<li>Certain cancers (endometrial, breast, colon, kidney, gallbladder, liver)</li>
<li>Low quality of life</li>
<li>Mental illnesses such as clinical
depression, anxiety, and others</li>
<li>Body pains and difficulty with certain
physical functions</li>
<li>Generally, an increased risk of
mortality compared to those with a healthy BMI</li>
</ul>
<br>
<h3 class="underweight">Risks associated with
being underweight</h3>
<p>
Being underweight has its own associated
risks, listed below:
<ul>
<li> Malnutrition, vitamin deficiencies, anemia (lowered ability to carry blood vessels)</li>
<li>Osteoporosis, a disease that causes
bone weakness, increasing the risk of breaking a bone</li>
<li>A decrease in immune function</li>
<li>Growth and development issues, particularly in children and teenagers</li>
<li>Possible reproductive issues for
women due to hormonal imbalances that can disrupt the
menstrual cycle. Underweight women also have a higher
chance of miscarriage in the first trimester</li>
<li>Potential complications as a result
of surgery</li>
<li>Generally, an increased risk of
mortality compared to those with a healthy BMI</li>
</ul>

</article>
<br><br><br><br>
</div>
<footer>
<br>
<a href="#">Back to top</a>
<p>created by gptc students</p>
<details class="summary">
<summary>
Created by
</summary>
<p>
Anuj joy<br>
Shijith or<br>
Akhila ku
</p>
</details>
<br>
<p>&lt;&lt;&lt; &copy; 2023 B M I
&gt;&gt;&gt;</p>
</footer>
</body>
<script>
function calculate(){
var bmi;
var result = document.getElementById("result");
var weight =
parseInt(document.getElementById("weight").value);
document.getElementById("weight-val").textContent =
weight + " KG";
var height =
parseInt(document.getElementById("height").value);
document.getElementById( "height-val").textContent =
height + " CM";
bmi = (weight / Math.pow( (height/100), 2)).toFixed(1);
result.textContent = bmi;
if(bmi < 18.5){
category = "Underweight";
result.style.color = "#fafa29";
}
else
if( bmi >= 18.5 && bmi <= 24.9 ) {
category = "Normal Weight";
result.style.color = "#33cc33";
}
else
if( bmi >= 25 && bmi <= 29.9 ){
category = "Overweight";
result.style.color = "#ff9933";
}
else{
category = "Obese";
result.style.color = "#ff5e57";
}
document.getElementById("category").textContent =
category;
}
</script>
</html>
<style>
*{
box-sizing: border-box;
}
header{
background-color: #9795F0;
padding: 30px;
font-family: monospace;
font-size: 35px;
color: white;
}
.col{
background: linear-gradient(#9795F0
,#FBC8D4);
color: rgb(47, 46, 57);
}
h2,h3{
color: black;
}
img{
margin-left: 30px;
}
footer{
background-color: #d18395;
padding: 10px;
text-align: center;
color: white;
left: 0;
bottom: 0;
width: 100%;
}
.container{
background-color: #ffffff;
padding: 40px 30px;
margin-left: 100px;
margin-bottom: 50px;
width: 50%;
top: 50%;
left: 50%;
border-radius: 14px;
font-family: 'Poppins', sans-serif;
box-shadow: 25px 25px 30px rgba(0,0,0,0.15);
}
.row{
display: flex;
align-items: center;
justify-content: space-between;
margin-bottom: 40px;
}
.row,span{
font-weight: 500;
}
input[type="range"]{
width: 70%;
height: 3.5px; -webkit-appearance: none;
appearance: none;
background-color: #dcdcdc;
border-radius: 3px;
outline: none;
}
input[type="range"]::-webkit-slider-thumb{
-webkit-appearance: none;
appearance: none;
height: 15px;
width: 15px;
background-color: blueviolet;
border-radius: 50%;
cursor: pointer;
}
#result{
font-size: 30px;
font-weight: 700;
letter-spacing: 1px;
text-align: center;
color: red;
}
#category{
font-size: 18px;
text-align: center;
letter-spacing: 1px;
}

</style>

