<!DOCTYPE html>
<!-- This is based on DillingerLee's great template here:
https://github.com/Team-Code/KA_Offline -->
<html> 
 <head>
    <title>Trump Headlines for Laughs</title> 
</head>
 <body>
    <p align="center"> 
    <!--This draws the Canvas on the webpage -->
      <canvas id="mycanvas"></canvas> 
    </p>
 </body>
 
 <!-- Run all the JavaScript stuff -->
 <!-- Include the processing.js library -->
 <!-- See https://khanacademy.zendesk.com/hc/en-us/articles/202260404-What-parts-of-ProcessingJS-does-Khan-Academy-support- for differences -->
 <script src="https://cdn.jsdelivr.net/processing.js/1.4.8/processing.min.js"></script> 
 
 <script>
    var Headlines = function(processingInstance) {
     with (processingInstance) {
        size(600, 600); 
        frameRate(30);
        
        // ProgramCodeGoesHere
var txtColor = color(0, 0, 0);

var bckGrnd = color(200, 255, 255);

var prnMsg = 0;

// START PROGRAM EXECUTION

textAlign(CENTER);
background(bckGrnd);

var t1=1;
var t2=2;
var t3=3;
var t4=4;
var t5=5;
var t6=0;
var d1=1;
var c1=1;
var c2=1;
var dtxt = ["Today, ",
            "Yesterday, ",
            "Recently, ",
            "During a press briefing, ",
            "At a rally, ",
            "While responding to reporter's questions "];
var ctxt1 = ["that he may have ",
            "he appears to have ",
            "he apparently has ",
            "he has clearly "];
var ctxt2 = ["what can only be described as ",
            "the potential for ",
            "a disturbing return to "];
var text1 = ["said ",
            "did ",
            "tweeted ",
            "signaled ",
            "signed ",
            "repeated "];
var text2 = ["incredibly ",
            "unbelievably ",
            "stunningly ",
            "mind-numbingly ",
            "typically ",
            "unusually "];
var text3 = ["stupid ",
            "ill-advised ",
            "dangerous ",
            "harmful ",
            "demented ",
            "crack-brained ",
            "mean-spirited ",
            "awful "];
var text4 = ["started ",
            "caused ",
            "triggered ",
            "initiated ",
            "encouraged ",
            "fomented "];
var text5 = ["catastrophic ",
            "disastrous ",
            "chaotic ",
            "unnecessary ",
            "over-the-top ",
            "widespread "];
var text6 = ["racial confrontations.",
            "international incidents.",
            "political turmoils.",
            "economic fallout.",
            "domestic terrorism.",
            "negative public heath consequences."];
var length = 1;           
            
// new mouse has been clicked routine

mouseClicked = function() {
    fill (txtColor);
    length=dtxt.length;
    d1=round(random(0,length-1));
    length=ctxt1.length;
    c1=round(random(0,length-1));
    length=ctxt2.length;
    c2=round(random(0,length-1));
    length=text1.length;
    t1=round(random(0,length-1));
    length=text2.length;
    t2=round(random(0,length-1));
    length=text3.length;
    t3=round(random(0,length-1));
    length=text4.length;
    t4=round(random(0,length-1));
    length=text5.length;
    t5=round(random(0,length-1));
    length=text6.length;
    t6=round(random(0,length-1));
    background(bckGrnd);

    fill (txtColor);
    textSize(40);
    text(dtxt[d1] + "Donald Trump " + text1[t1] + "something that was so " +            text2[t2] + text3[t3] + ctxt1[c1] + text4[t4] + ctxt2[c2]+ text5[t5] +                 text6[t6], 15,100,570,450);

    prnMsg = 0;

};



//MAIN FUNCTION draw
var draw = function() {

fill (110, 4, 22);    
textSize(40);
if (prnMsg === 0) {
    text("Click to Read Next Headline!",25,540,550,40);   
    prnMsg = 1;
}

};

    }};

    // Get the canvas that Processing-js will use
    var canvas = document.getElementById("mycanvas"); 
    // Pass the function sketchProc (defined in myCode.js) to Processing's constructor.
    var processingInstance = new Processing(canvas, Headlines); 
 </script>

</html>
