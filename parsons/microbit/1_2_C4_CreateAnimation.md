---
layout: default
title: Creating an animation
---
## Creating an animation

## Extension
### Animation with built in and custom images
<div id="1_2_C4_E2-sortableTrash" class="sortable-code"></div> 
<div id="1_2_C4_E2-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="1_2_C4_E2-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="1_2_C4_E2-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "# This animation incorporates a built-in image of\n" +
    "# a heart and custom images with varying brightness\n" +
    "# so that when button a and b are pressed\n" +
    "# the heart fades\n" +
    "from microbit import *\n" +
    "while True:\n" +
    "    if button_a.is_pressed and button_b.is_pressed():\n" +
    "        display.show(Image.HEART)\n" +
    "        sleep(500)\n" +
    "        display.show(Image(&quot;07070:&quot;\\n                   &quot;77777:&quot;\\n                   &quot;77777:&quot;\\n                   &quot;07770:&quot;\\n                   &quot;00700&quot;))\n" +
    "        sleep(500)\n" +
    "        display.show(Image(&quot;05050:&quot;\\n                   &quot;55555:&quot;\\n                   &quot;55555:&quot;\\n                   &quot;05550:&quot;\\n                   &quot;00500&quot;))\n" +
    "        sleep(500)\n" +
    "        display.show(Image(&quot;03030:&quot;\\n                   &quot;33333:&quot;\\n                   &quot;33333:&quot;\\n                   &quot;03330:&quot;\\n                   &quot;00300&quot;))\n" +
    "        sleep(500)\n" +
    "        display.show(Image(&quot;01010:&quot;\\n                   &quot;11111:&quot;\\n                   &quot;11111:&quot;\\n                   &quot;01110:&quot;\\n                   &quot;00100&quot;))\n" +
    "        sleep(500)\n";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "1_2_C4_E2-sortable",
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
  $("#1_2_C4_E2-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#1_2_C4_E2-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
