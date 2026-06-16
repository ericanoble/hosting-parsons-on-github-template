<div id="turtle-sortableTrash" class="sortable-code"></div> 
<div id="turtle-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="turtle-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="turtle-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "myTurtle.forward(60)\n" +
    "myTurtle.left(90)\n" +
    "myTurtle.forward(80)\n" +
    "myTurtle.left(143)\n" +
    "myTurtle.forward(100)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "turtle-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.TurtleGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "python3": true,
    "executable_code": "",
    "programmingLang": "pseudo",
    "turtleModelCode": "modelTurtle.forward(60)\nmodelTurtle.left(90)\nmodelTurtle.forward(80)\nmodelTurtle.left(143)\nmodelTurtle.forward(100)"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#turtle-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#turtle-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
