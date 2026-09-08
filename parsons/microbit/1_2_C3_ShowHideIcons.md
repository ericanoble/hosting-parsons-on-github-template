---
layout: default
title: Showing and hiding icons
---
## Showing and hiding icons
<div id="1_2_C3-sortableTrash" class="sortable-code"></div> 
<div id="1_2_C3-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="1_2_C3-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="1_2_C3-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "from microbit import *\n" +
    "while True:\n" +
    "    if pin_logo.is_touched():\n" +
    "        display.show(Image.HAPPY)\n" +
    "    else:\n" +
    "        display.clear()";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "1_2_C3-sortable",
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
  $("#1_2_C3-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#1_2_C3-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
