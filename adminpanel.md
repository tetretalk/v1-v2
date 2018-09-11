---
layout: page
title: Tetretalk Beta
description: Beta - {[PROTECTED CONTENT]}
permalink: /beta/
---


<div>
<SCRIPT>
function passWord() {
var testV = 1;
var pass1 = prompt('Please Enter Your Password to make sure you are an actual beta tester','');
while (testV < 3) {
if (!pass1) 
history.go(-1);
if (pass1.toLowerCase() == "49986") {
alert('Correct password | Welcome, Beta Tester!');
window.replace('https://beta.tetretalk.gq');
break;
} 
testV+=1;
var pass1 = 
prompt('Access Denied - Try again! Access to tetretalk beta denied.','');
}
if (pass1.toLowerCase()!="password" & testV ==3) 
history.go(-1);
return "";
} 
  passWord()
</SCRIPT>
</div>
