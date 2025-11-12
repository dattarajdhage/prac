JS  Experiment No  1   =area of triangle
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<script src="EXP1.js" > 
</script>
<body>
</body>
</html>
//Area Of Triangle
let base=10;
let height=20;
let triangleArea = 0.5*base*height;
document.write("Area of Triangle = " + triangleArea+ " <br>");
// Area of Circle 
let radius= 15 ;
let CircleArea = Math.PI * radius * radius;
document.write(" Area of circle = " + CircleArea.toFixed(2));
----------------------------------------------------------------------------------------------------------------------------
JS  Experiment no 2 = table
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<script src = EXP3.js> </script>
<body>    
</body>
</html>
let num = parseInt(prompt("Enter a number"));
for( let i = 1 ;i<= 10 ;i++){
   document.write(num + " x " + i + " = "+ (num*i) + "<br>");
}
----------------------------------------------------------------------------------------------------------------------------
    exp 3 
    // JavaScript Program: String Operations

<!DOCTYPE html>
<html>
<head>
  <title>String Operations in JavaScript</title>
</head>
<body>

  <h2>JavaScript String Operations</h2>

  <label>Enter a string:</label><br>
  <input type="text" id="inputString" placeholder="Enter text here"><br><br>

  <label>Replace character:</label><br>
  <input type="text" id="oldChar" maxlength="1" placeholder="Old char">
  <input type="text" id="newChar" maxlength="1" placeholder="New char"><br><br>

  <button onclick="reverseStr()">Reverse String</button>
  <button onclick="replaceChar()">Replace Character</button>
  <button onclick="checkPalindrome()">Check Palindrome</button>

  <div id="result"></div>

  <script>
    // Function to reverse a string
    function reverseStr() {
      const str = document.getElementById("inputString").value;
      const reversed = str.split('').reverse().join('');
      document.getElementById("result").innerText = "Reversed String: " + reversed;
    }

    // Function to replace characters in a string
    function replaceChar() {
      const str = document.getElementById("inputString").value;
      const oldChar = document.getElementById("oldChar").value;
      const newChar = document.getElementById("newChar").value;
      if (oldChar === "") {
        document.getElementById("result").innerText = "Please enter a character to replace.";
        return;
      }
      const replaced = str.split(oldChar).join(newChar);
      document.getElementById("result").innerText = 
        "After replacing '" + oldChar + "' with '" + newChar + "': " + replaced;
    }

    // Function to check if string is palindrome
    function checkPalindrome() {
      const str = document.getElementById("inputString").value;
      const cleaned = str.toLowerCase().replace(/[^a-z0-9]/g, '');
      const reversed = cleaned.split('').reverse().join('');
      const isPal = cleaned === reversed;
      document.getElementById("result").innerText = 
        isPal ? "It is a Palindrome!" : "Not a Palindrome.";
    }
  </script>

</body>
</html>

  
----------------------------------------------------------------------------------------------------------------------------

JS  Experiment no 4 = compare string
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Compare Strings</title>
</head>
<body>
    <script src="exp4.js"></script>
</body>
</html> 
let str1= prompt("Enter first string:");
 let str2 = prompt("Enter second string:");
// Using localeCompare let compare str1.localeCompare(str2);
//Direct comparison
 if(str1=== str2) {
document.write("Strings are exactly equal.<br>"); }
 else {
    document.write("Strings are different.<br>");
    }
// Using comparison result
if(compare= 0) {
document.write("Strings are same (localeCompare).");
} else if(compare < 0) {
document.write("First string comes before second.");
} else {
document.write("First string comes after second.");
}

----------------------------------------------------------------------------------------------------------------------------

JS   Experiment no 5 = timer


<!DOCTYPE html>
<html>
<body>
<h1 id="timer"></h1>
<script>
let seconds = 10; 
let countdown = setInterval(function() {
document.getElementById("timer").innerHTML = seconds;
seconds--;
if(seconds < 0) {
clearInterval(countdown);
document.getElementById("timer").innerHTML = "Time's up!";
}
}, 1000);
</script>
</body>
</html>



----------------------------------------------------------------------------------------------------------------------------


JS EXP6 = array

<!doctype html> 
<html> 
<head> 
  <title>Array Operations</title> 
</head> 
<body> 
  <h2>Array Operations</h2> 
  <input id="arrInput" type="text" placeholder="Enter comma separated values"> 
  <button onclick="loadArray()">Load Array</button> 
  <p id="display">[]</p> 

  <input id="removeValue" type="text" placeholder="Value to remove"> 
  <button onclick="removeElement()">Remove</button> 

  <input id="checkValue" type="text" placeholder="Value to check"> 
  <button onclick="checkElement()">Check</button> 
  <span id="checkResult"></span> 

  <button onclick="emptyArray()">Empty Array</button> 

  <script>let arr = []; 

function loadArray() { 
  let val = document.getElementById("arrInput").value; 
  arr = val.split(",").map(x => x.trim()).filter(x => x !== ""); 
  document.getElementById("display").innerText = JSON.stringify(arr); 
} 
function removeElement() { 
  let v = document.getElementById("removeValue").value; 
  arr = arr.filter(x => x !== v); 
  document.getElementById("display").innerText = JSON.stringify(arr); 
} 
function checkElement() { 
  let v = document.getElementById("checkValue").value; 
  let found = arr.includes(v); 
  document.getElementById("checkResult").innerText = found ? "Found" : "Not Found"; 
} 
function emptyArray() { 
  arr = []; 
  document.getElementById("display").innerText = JSON.stringify(arr); 
}</script> 
</body> 
</html>

----------------------------------------------------------------------------------------------------------------------------


JS  EXP7 = set operation

<!doctype html> 
<html> 
<head> 
  <title>Set Operations</title> 
</head> 
<body> 
  <h2>Set Operations</h2> 

  <input id="setA" type="text" placeholder="Enter Set A (comma separated)"> 
  <input id="setB" type="text" placeholder="Enter Set B (comma separated)"> 
  <br><br> 

  <button onclick="union()">Union</button> 
  <button onclick="intersection()">Intersection</button> 
  <button onclick="difference()">Difference (A-B)</button> 
  <button onclick="symmetricDifference()">Symmetric Difference</button> 

  <p id="result"></p> 

  <script >
      function getSets() { 
  let A = document.getElementById("setA").value.split(",").map(x => x.trim()).filter(x => x); 
  let B = document.getElementById("setB").value.split(",").map(x => x.trim()).filter(x => x); 
  return [new Set(A), new Set(B)]; 
} 

function union() { 
  let [A, B] = getSets(); 
  let result = [...new Set([...A, ...B])]; 
  document.getElementById("result").innerText = "Union: " + result; 
} 

function intersection() { 
  let [A, B] = getSets(); 
  let result = [...A].filter(x => B.has(x)); 
  document.getElementById("result").innerText = "Intersection: " + result; 
} 

function difference() { 
  let [A, B] = getSets(); 
  let result = [...A].filter(x => !B.has(x)); 
  document.getElementById("result").innerText = "Difference (A-B): " + result; 
} 

function symmetricDifference() { 
  let [A, B] = getSets(); 
  let result = [...A].filter(x => !B.has(x)).concat([...B].filter(x => !A.has(x))); 
  document.getElementById("result").innerText = "Symmetric Difference: " + result; 
} 
  </script> 
</body> 
</html> 

----------------------------------------------------------------------------------------------------------------------------

 JS   EXP8 = mouse event


<!DOCTYPE html> 
<html> 
<head> 
<title>Homepage Events</title> 
<link rel="stylesheet" href="Exp8.css"> 
    <style>
        body { 
text-align: center; 
padding: 50px; 
transition: background-color 0.3s; 
} 
input { 
padding: 10px; 
font-size: 16px; 
}</style>
</head> 
<body> 
<h1>Welcome to the Homepage</h1> 
<input type="text" placeholder="Focus on me" id="focusInput"> 
<script >
    document.body.addEventListener("mouseover", function() { 
document.body.style.backgroundColor = "#e72d2dff"; 
}); 
document.body.addEventListener("mouseout", function() { 
document.body.style.backgroundColor = "#ffffff"; 
}); 
document.getElementById("focusInput").addEventListener("focus", function() { 
this.style.border = "2px solid blue"; 
}); 
document.getElementById("focusInput").addEventListener("blur", function() { 
this.style.border = "1px solid #ccc"; 
});
</script> 
</body> 
</html>

----------------------------------------------------------------------------------------------------------------------------

JS Exp9 = student info


Exp9.html 
<!DOCTYPE html> 
<html> 
<head> 
  <title>Student Information Form</title> 
</head> 
    <style>
        body { 
  text-align: center; 
  padding: 50px; 
  font-family: Arial, sans-serif; 
  background-color: lavender; 
} 

.form-row { 
  margin: 10px 0; 
} 

label { 
  display: inline-block; 
  width: 100px; 
  text-align: right; 
  margin-right: 10px; 
} 

input, select { 
  width: 200px; 
  padding: 5px; 
  border: 1px solid #ccc; 
  outline: none; 
} 

input.error, select.error { 
  border: 2px solid red; 
  background-color: #ffe6e6; 
} 

button { 
  padding: 8px 16px; 
  margin-top: 10px; 
  cursor: pointer; 
}
    </style>
<body> 
  <h2>Student Information Form</h2> 

  <form id="studentForm"> 
    <div class="form-row"> 
      <label for="name">Name:</label> 
      <input type="text" id="name"> 
    </div> 
    <div class="form-row"> 
      <label for="address">Address:</label> 
      <input type="text" id="address"> 
    </div> 
    <div class="form-row"> 
      <label for="city">City:</label> 
      <input type="text" id="city"> 
    </div> 
    <div class="form-row"> 
      <label for="state">State:</label> 
      <input type="text" id="state"> 
    </div> 
    <div class="form-row"> 
      <label for="gender">Gender:</label> 
      <select id="gender"> 
        <option value="">--Select--</option> 
        <option value="Male">Male</option> 
        <option value="Female">Female</option> 
        <option value="Other">Other</option> 
      </select> 
    </div> 
    <div class="form-row"> 
      <label for="mobile">Mobile:</label> 
      <input type="text" id="mobile"> 
    </div> 
    <div class="form-row"> 
      <label for="email">Email:</label> 
      <input type="text" id="email"> 
    </div> 
    <button type="submit">Submit</button> 
  </form> 

  <script>
      document.getElementById("studentForm").addEventListener("submit", function(e) { 
  e.preventDefault(); 

  // Clear previous errors 
  let fields = document.querySelectorAll("input, select"); 
  fields.forEach(f => f.classList.remove("error")); 

  let name = document.getElementById("name").value.trim(); 
  let address = document.getElementById("address").value.trim(); 
  let city = document.getElementById("city").value.trim(); 
  let state = document.getElementById("state").value.trim(); 
  let gender = document.getElementById("gender").value.trim(); 
  let mobile = document.getElementById("mobile").value.trim(); 
  let email = document.getElementById("email").value.trim(); 

  if (!name || !address || !city || !state || !gender || !mobile || !email) { 
    alert("All fields are required."); 
    if (!name) document.getElementById("name").classList.add("error"); 
    if (!address) document.getElementById("address").classList.add("error"); 
    if (!city) document.getElementById("city").classList.add("error"); 
    if (!state) document.getElementById("state").classList.add("error"); 
    if (!gender) document.getElementById("gender").classList.add("error"); 
    if (!mobile) document.getElementById("mobile").classList.add("error"); 
    if (!email) document.getElementById("email").classList.add("error"); 
    return; 
  } 

  if (!name.match(/^[A-Za-z\s]+$/)) { 
    alert("Invalid Name. Only alphabets allowed."); 
    document.getElementById("name").classList.add("error"); 
    return; 
  } 

  if (!mobile.match(/^\d{10}$/)) { 
    alert("Invalid Mobile. Enter a 10-digit number."); 
    document.getElementById("mobile").classList.add("error"); 
    return; 
  } 

  if (!email.match(/^[^\s@]+@[^\s@]+\.[^\s@]+$/)) { 
    alert("Invalid Email format."); 
    document.getElementById("email").classList.add("error"); 
    return; 
  } 

  let studentData = { name, address, city, state, gender, mobile, email }; 
  localStorage.setItem("studentData", JSON.stringify(studentData)); 

  window.location.href = "success.html"; 
});
  </script> 
</body> 
</html>


  --   Success.html 
<!DOCTYPE html> 
<html> 
<head> 
  <title>Form Submitted</title> 
  <link rel="stylesheet" href="Exp9.css"> 
  <style> 
    table { 
      margin: 20px auto; 
      border-collapse: collapse; 
      width: 50%; 
      background: white; 
      box-shadow: 0 0 10px rgba(0,0,0,0.2); 
    } 
    th, td { 
      padding: 10px; 
      border: 1px solid #555; 
      text-align: left; 
    } 
    th { 
      background-color: lavender; 
      text-align: center; 
    } 
  </style> 
</head> 
<body> 
  <h2 style="color: green;">Form Submitted Successfully!</h2> 
  <div id="details"></div> 
  <br> 
  <button onclick="window.location.href='Exp9.html'">Back to Form</button> 

  <script> 
    let studentData = JSON.parse(localStorage.getItem("studentData")); 
    if (studentData) { 
      document.getElementById("details").innerHTML = ` 
        <table> 
          <tr><th colspan="2">Entered Details</th></tr> 
          <tr><td><strong>Name</strong></td><td>${studentData.name}</td></tr> 
          <tr><td><strong>Address</strong></td><td>${studentData.address}</td></tr> 
          <tr><td><strong>City</strong></td><td>${studentData.city}</td></tr> 
          <tr><td><strong>State</strong></td><td>${studentData.state}</td></tr> 
          <tr><td><strong>Gender</strong></td><td>${studentData.gender}</td></tr> 
          <tr><td><strong>Mobile</strong></td><td>${studentData.mobile}</td></tr> 
          <tr><td><strong>Email</strong></td><td>${studentData.email}</td></tr> 
        </table> 
      `; 
    } 
  </script> 
</body> 
</html>
