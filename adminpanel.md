---
layout: page
title: Admin Panel
description: Admin Panel - {[PROTECTED CONTENT]}
permalink: /admin/
---


<div>
<SCRIPT>
function passWord() {
var testV = 1;
var pass1 = prompt('Please Enter Your Password','');
while (testV < 3) {
if (!pass1) 
history.go(-1);
if (pass1.toLowerCase() == "49986") {
alert('Correct password | Welcome, admin!');
window.open('https://admin.tetretalk.gq');
break;
} 
testV+=1;
var pass1 = 
prompt('Access Denied - Try again! Access to Tetretalk Admin panel denied!','');
}
if (pass1.toLowerCase()!="password" & testV ==3) 
history.go(-1);
return "";
} 
  passWord()
</SCRIPT>
</div>
