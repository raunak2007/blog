---
toc: true
layout: post
description: Binary Calculator
title: Binary Calculator
categories: [markdown, csp]
permalink: /BinaryCalculator/
---

<html>
 <body>
<!-- html table -->
<table>
  <tr>
    <td colspan="4"> <input class="display-box" type="text" id="output"/> </td>
  </tr>
  <tr>
    <td> <input type="button" value="1" class="btn btn-outline-primary" onclick="input('1')" /> </td>
    <td> <input type="button" value="2" class="btn btn-outline-primary" onclick="input('2')" /> </td>
    <td> <input type="button" value="3" class="btn btn-outline-primary" onclick="input('3')" /> </td>
    <td> <input type="button" value="/" class="btn btn-outline-primary" onclick="input('/')" /> </td>
  </tr>
  <tr>
    <td> <input type="button" value="4" class="btn btn-outline-primary" onclick="input('4')" /> </td>
    <td> <input type="button" value="5" class="btn btn-outline-primary" onclick="input('5')" /> </td>
    <td> <input type="button" value="6" class="btn btn-outline-primary" onclick="input('6')" /> </td>
    <td> <input type="button" value="-" class="btn btn-outline-primary" onclick="input('-')" /> </td>
  </tr>
  <tr>
    <td> <input type="button" value="7" class="btn btn-outline-primary" onclick="input('7')" /> </td>
    <td> <input type="button" value="8" class="btn btn-outline-primary" onclick="input('8')" /> </td>
    <td> <input type="button" value="9" class="btn btn-outline-primary" onclick="input('9')" /> </td>
    <td> <input type="button" value="+" class="btn btn-outline-primary" onclick="input('+')" /> </td>
  </tr>
  <tr>
    <td> <input type="button" value="C" class="btn btn-outline-primary" onclick="empty()" /> </td>
    <td> <input type="button" value="0" class="btn btn-outline-primary" onclick="input('0')" /> </td>
    <td> <input type="button" value="=" class="btn btn-outline-primary" onclick="input('calculate')" id="btn" /> </td>
    <td> <input type="button" value="*" class="btn btn-outline-primary" onclick="input('*')" /> </td>
  </tr>
</table>
</body>
</html>
<script>  
// clear function
function empty() {
  inputs = ""
  document.getElementById("output").value = ""
  oldinput = ""
  operator = ""
}
// defining variables
let inputs = ""
let oldinput = ""
let operator = ""
function input(data) {
  const parsed = Number.parseInt(data)
  let input = ""
//  binary converter 
function decimal_to_binary(a) {
let binary = '';
  while (a>0)
   {
binary = (a%2) + binary;
    a = Math.floor(a/2);
     }
return binary;
}
// checks if its a number
  if (!isNaN(parsed)){
    inputs += parsed.toString()
    document.getElementById("output").value = oldinput + operator + inputs
    console.log(decimal_to_binary(inputs))
// calculate function
  }else if (data ==='calculate') {
    if (operator ==='+') {
      document.getElementById("output").value = decimal_to_binary(parseInt(inputs) + parseInt(oldinput))
      oldinput = ""
      operator = ""
      input = ""
    }
    if (operator ==='-') {
      document.getElementById("output").value = decimal_to_binary(parseInt(inputs) - parseInt(oldinput))
      oldinput = ""
      operator = ""
      input = ""
    }
    if (operator ==='/') {
      document.getElementById("output").value = decimal_to_binary(parseInt(inputs) / parseInt(oldinput))
      oldinput = ""
      operator = ""
      input = ""
    }
    if (operator ==='*') {
      document.getElementById("output").value = decimal_to_binary(parseInt(inputs) * parseInt(oldinput))
      oldinput = ""
      operator = ""
      input = ""
    }
  } else{ 
// this gets the operator and sets the parameters for the calculator function   
    console.log(data)
    console.log("applying " + data + " to " + inputs)
    document.getElementById("output").value = inputs + data
    operator = data
    oldinput = inputs
    inputs = ""
  } 
}
</script>
<style>