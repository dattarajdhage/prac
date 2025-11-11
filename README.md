JS  Experiment No  1


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

JS  Experiment no 2


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


JS  Experiment no 4


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

