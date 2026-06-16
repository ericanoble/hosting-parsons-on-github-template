---
layout: default
title: Unit Test
---
### Unit Test
<div id="unitTest-sortableTrash" class="sortable-code"></div> 
<div id="unitTest-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="unitTest-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="unitTest-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "def triangle_area(base, height):\n" +
    "    area = base * height / 2\n" +
    "    return area\n" +
    " area = base + height / 2#distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "unitTest-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.UnitTestGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "python3": true,
    "trashId": "unitTest-sortableTrash",
    "unittest_code_prepend": "",
    "unittests": "import unittestparson\nclass myTests(unittestparson.unittest):\n  def test_0(self):\n    self.assertEqual(triangle_area(6, 4),12.0,triangle_area(6, 4) should return 12.0)\n  def test_1(self):\n    self.assertEqual(triangle_area(10, 5),25.0,triangle_area(10, 5) should return 25.0)\n  def test_2(self):\n    self.assertEqual(triangle_area(3, 8),12.0,triangle_area(3, 8) should return 12.0)\n_test_result = myTests().main()"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#unitTest-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#unitTest-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
