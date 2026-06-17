---
layout: default
title: Showing a number
---
### Showing a number
Re-arrange the blocks below so that the number 8 will appear on the micro:bit display.

<div id="1_1_C1-sortableTrash" class="sortable-code"></div> 
<div id="1_1_C1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="1_1_C1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="1_1_C1-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "from microbit import *\n" +
    "while True:\n" +
    "    display.show(8)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "1_1_C1-sortable",
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
  $("#1_1_C1-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#1_1_C1-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
