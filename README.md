# Quote_Generator
## Date:14.03.2026
## Objective:
To create a simple thirukkural generator using HTML, CSS, and JavaScript that displays a new random thirukkural each time a button is clicked — similar to daily quote sections on blogs or productivity apps.

## Tasks:

### 1. Create the HTML Structure:
<ul>
  <li>Add a heading Thirukkural Generator</li>
  <li>Use a div or p to display the Thirukkural (Tamil couplet).</li>
  <li>Use another p or span to display the meaning or explanation.</li>
  <li>Add a button labeled “Get Thirukkural”.</li>
  <li>Add a label showing the Kural number.</li>
</ul>

### 2. Style the Layout Using CSS:

<ul>
  <li>Center everything on the page using Flexbox.</li>
  <li>Style the quote box with:
  <ul type="square">
    <li>Padding</li>
    <li>Background color</li>
    <li>Rounded borders</li>
    <li>Soft shadow</li>
    <li>Add hover effects for the button.</li>
  </ul>
  </li>
</ul>

### 3. Add JavaScript Functionality:
<ul>
  <li>Store an array of Thirukkural objects containing:
  <ul type="square">
    <li>Kural number</li>
    <li>Kural Meaning</li>
  </ul>
  </li>
  <li>When the button is clicked:
  <ul type="square">
    <li>Generate a random index using Math.random().</li>
    <li>Retrieve the corresponding Thirukkural object.</li>
    <li>Display the Kural number and meaning in the HTML.</li>
    <li>Update content dynamically using innerText.</li>
  </ul>
  </li>
</ul>

## Code:
```
<html>
<head>
     <title>Thirukkural Generator</title>

<style>
body{
    background: url('https://pplx-res.cloudinary.com/image/upload/pplx_search_images/67ec6aa2c162dbc102ed8e258e09618c71c684e9.jpg') center/cover no-repeat;
    font-family: Arial;
    display:flex;
    justify-content:center;
    align-items:center;
    height:100vh;
}

.container{
    background:white;
    padding:20px;
    width:400px;
    text-align:center;
    border-radius:10px;
    box-shadow:0 0 10px gray;
}

button{
    padding:10px 20px;
    background:green;
    color:white;
    border:none;
    border-radius:5px;
    cursor:pointer;
}

button:hover{
    background:darkgreen;
}

#kural{
    margin-top:20px;
    font-size:18px;
}

#meaning{
    margin-top:10px;
    color:#444;
}
</style>

</head>

<body>

<div class="container">
    <h2>Thirukkural Generator</h2>

    <p id="number">Kural No: </p>
    <p id="kural">Click the button to get a Thirukkural</p>
    <p id="meaning"></p>

    <button onclick="showKural()">Get Thirukkural</button>
</div>

<script>
var kurals = [
{
    number: 621,
    text: "தன் மொழி சிறப்பன்ன தாழ்த்தல் தகுதியாம் தம்மைத் தாழ்த்துதல்",
    meaning: "Humility is speaking modestly of one's own excellence."
},
{
    number: 11,
    text: "வான்நலமும் நன்னலமும் நீடுசெய்யும்\nஊனதலால் உலகம் தரும்",
    meaning: "Rain makes the heavens fertile and earth fruitful, sustaining the world."
},
{
    number: 12,
    text: "அன்பை வலியுரைப்பது அரியவர் அன்பின்றி வாழ்க்கை இன்றி",
    meaning: "Those who speak kindly without affection live without true life."
}
];

function showKural(){
var random = Math.floor(Math.random()*kurals.length);
document.getElementById("number").innerText="Kural No: "+kurals[random].number;
document.getElementById("kural").innerText=kurals[random].text;
document.getElementById("meaning").innerText=kurals[random].meaning;
}

</script>

</body>
</html>

```

## Output:
![alt text](<Screenshot (100).png>)
## Result:
A simple quote generator using HTML, CSS, and JavaScript that displays a new random motivational quote each time a button is clicked — similar to daily quote sections on blogs or productivity apps is created successfully.
