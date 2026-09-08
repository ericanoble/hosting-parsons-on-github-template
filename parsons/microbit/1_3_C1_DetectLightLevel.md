---
layout: default
title: Detecting light level
---
## Detecting light level
<div id="1_3_C1-sortableTrash" class="sortable-code"></div> 
<div id="1_3_C1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="1_3_C1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="1_3_C1-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "from microbit import *\n" +
    "while True:\n" +
    "    if button_a.is_pressed():\n" +
    "        display.scroll(display.read_light_level())";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "1_3_C1-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "python3": true
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#1_3_C1-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#1_3_C1-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
<div id="1_3_C1_E1-sortableTrash" class="sortable-code"></div> 
<div id="1_3_C1_E1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="1_3_C1_E1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="1_3_C1_E1-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "# Instead of button input use input from the touch logo, accelerometer, microphone, compass, light sensor or temperature sensor\n" +
    "from microbit import *\n" +
    "while True:\n" +
    "    if pin_logo.is_touched():\n" +
    "        display.scroll(display.read_light_level())";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "1_3_C1_E1-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "python3": true
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#1_3_C1_E1-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#1_3_C1_E1-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
