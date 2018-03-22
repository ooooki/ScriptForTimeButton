# ScriptForTimeButton
Script which repeatedly clicks on Button 

This script will be useful where button is already enabled, and response the response depends on the server.
Since I don't know much of javascript cannot stop the script once the response is received. This is todo.
Use this - 	clearInterval(time); to stop the script, add it after script 1 activated.


Steps:
1) On the website,open chrome console.
2) Paste the script.
3) Enter

100 time limit in the script can be changed as per your need.
Line b = "Confirm"  can be changed to the title of the button
Line 'type'="submit" can be found out by inspecting the element.

---------------------------------
var time=setInterval(function(){

function getElementsByAttrib(attrib) {
    return document.querySelectorAll('[' + attrib + ']');
}
var elements = getElementsByAttrib('type="submit"');
MySubmit = elements[0];

 if(MySubmit != null && MySubmit !='undefined'){
  var b = MySubmit.innerHTML;
  if(b == "Add")
  {
     console.log("Script 1 Activated");
     MySubmit.click();

   } else {
   console.log("Script Activated");
   }
 }
 else
 {
  console.error("Control not found.");
 }
},100);
------------------------------
