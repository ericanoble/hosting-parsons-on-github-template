---
layout: default
title: 1.1 Hello World!
---
## Object-oriented programming
Use the blocks below to simulate the behaviour of a thermostat that displays the name of a room followed by the temperature of that room in degrees.
Display "Living room" followed by "Bathroom".
<div id="1_1_oop-sortableTrash" class="sortable-code"></div> 
<div id="1_1_oop-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="1_1_oop-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="1_1_oop-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "from microbit import *\n" +
    "class Thermostat:                       \n" +
    "    def __init__(self, room, degrees):\n" +
    "        self.room = room                 \n" +
    "        self.degrees = degrees          \n" +
    "    def scroll_temperature(self):         \n" +
    "        display.scroll(self.room)       \n" +
    "        display.scroll(self.degrees)\n" +
    "living_room = Thermostat(&quot;Living room&quot;, 21)\n" +
    "bathroom = Thermostat(&quot;Bathroom&quot;, 14)\n" +
    "while True:\n" +
    "    living_room.scroll_temperature()\n" +
    "    bathroom.scroll_temperature()";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "1_1_oop-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "python3": true,
    "trashId": "1_1_oop-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#1_1_oop-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#1_1_oop-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
