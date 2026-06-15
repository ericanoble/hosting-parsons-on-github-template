---
layout: default
title: 1.1 Hello World!
---

### 1_2_C1 Showing your names
<div id="1_2_C1-sortableTrash" class="sortable-code"></div> 
<div id="1_2_C1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="1_2_C1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="1_2_C1-newInstanceLink" value="Reset Problem" type="button" /> 
</p>
<fieldset id="1_2_C1-feedback" style="margin-top:20px;"><legend>Feedback:</legend><div id="1_2_C1-feedback-text"></div></fieldset>
<script type="text/javascript"> 
(function(){
  var initial = "from microbit import *\n" +
    "while True:\n" +
    "    if button_a.is_pressed():\n" +
    "        display.scroll(&#039;Nick&#039;)\n" +
    "    if button_b.is_pressed():\n" +
    "        display.scroll(&#039;Eva&#039;)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "1_2_C1-sortable",
    "trashId": "1_2_C1-sortableTrash",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#1_2_C1-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines();
      $("#1_2_C1-feedback-text").html('');
  }); 
  $("#1_2_C1-feedbackLink").click(function(event){ 
      event.preventDefault();
      var feedback = parsonsPuzzle.getFeedback();
      var message = feedback.html || feedback.feedback;
      if (!message && feedback.length) {
          message = feedback.join('\n');
      }
      message = message && !feedback.success ? message : 'Congratulations on solving your Parsons Problem!';
      $("#1_2_C1-feedback-text").html(message);
  });
})(); 
</script>
