---
layout: default
title: Showing icons
---
## Showing icons
<div id="1_2_C2-sortableTrash" class="sortable-code"></div> 
<div id="1_2_C2-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="1_2_C2-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="1_2_C2-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "from microbit import *\n" +
    "while True:\n" +
    "    if button_a.is_pressed(): \n     display.show(Image.SILLY)\n" +
    "    if button_b.is_pressed(): \n     display.show(Image.DUCK)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "1_2_C2-sortable",
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
  $("#1_2_C2-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#1_2_C2-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## Extension
### Custom icon
<div id="1_2_C2_E1-sortableTrash" class="sortable-code"></div> 
<div id="1_2_C2_E1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="1_2_C2_E1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="1_2_C2_E1-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "from microbit import *\n" +
    "while True:\n" +
    "    if button_a.is_pressed():\n" +
    "        display.show(Image(&#039;05050:&#039; \n                   &#039;05050:&#039; \n                   &#039;05050:&#039; \n                   &#039;99999:&#039; \n                   &#039;09990&#039;))";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "1_2_C2_E1-sortable",
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
  $("#1_2_C2_E1-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#1_2_C2_E1-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
