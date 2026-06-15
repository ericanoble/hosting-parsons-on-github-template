---
layout: default
title: Showing a string
---
### Showing a string
<div id="1_1_C2-sortableTrash" class="sortable-code"></div> 
<div id="1_1_C2-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="1_1_C2-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="1_1_C2-newInstanceLink" value="Reset Problem" type="button" />
<fieldset id="1_1_C2-feedback" style="margin-top:20px;"><legend>Feedback:</legend><div id="1_1_C2-feedback-text"></div></fieldset>
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "from microbit import *\n" +
    "while True:\n" +
    "    display.scroll(&quot;Hello World!&quot;)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "1_1_C2-sortable",
    "trashId": "1_1_C2-sortableTrash", 
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
  $("#1_1_C2-newInstanceLink").click(function(event){
    event.preventDefault();
    parsonsPuzzle.shuffleLines();
  $("#1_1_C2-feedback-text").html('');
  });
  $("#1_1_C2-feedbackLink").click(function(event){
    event.preventDefault();
    var feedback = parsonsPuzzle.getFeedback();
    var message = feedback.html || feedback.feedback;
    if (!message && feedback.length) { message = feedback.join('\n'); }
    message = message && !feedback.success ? message : 'Congratulations on solving your Parsons Problem!';
  $("#1_1_C2-feedback-text").html(message);
});
})(); 
</script>
