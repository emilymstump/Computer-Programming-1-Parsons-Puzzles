---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Practice with While and For Loops
---

## 2 Through 20 Even
Write a program that prints even numbers 2 through 20 using a while loop.

<div id="evens-sortableTrash" class="sortable-code"></div> 
<div id="evens-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="evens-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="evens-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "number = 2\n" +
    "while number &lt;= 20:\n" +
    "    print(number)\n" +
    "    number += 2";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "evens-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "evens-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#evens-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#evens-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


## Divisibility
We want to ask a user for two numbers and then divide them. The issue is that we cannot divide a number by 0. You’ll need to have a while loop that forces a user to continue entering a denominator value until their input is not zero. If the user enters a 0, tell them they cannot enter zero and have them enter another number. Once they have a nonzero denominator, then check whether the numerator is divisible by the denominator.

<div id="divide-sortableTrash" class="sortable-code"></div> 
<div id="divide-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="divide-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="divide-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "numerator = int(input(&quot;Enter a numerator: &quot;))\n" +
    "denominator = int(input(&quot;Enter denominator: &quot;))\n" +
    "while denominator == 0:\n" +
    "    print(&quot;You can&#039;t divide by zero!&quot;)\n" +
    "    denominator = int(input(&quot;Enter a nonzero denominator: &quot;))\n" +
    "if int(numerator / denominator) * denominator == numerator:\n" +
    "    print(&quot;Divides evenly!&quot;)\n" +
    "else:\n" +
    "    print(&quot;Doesn&#039;t divide evenly.&quot;)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "divide-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "divide-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#divide-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#divide-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## Divisibility
We want to ask 
<div id="divide2-sortableTrash" class="sortable-code"></div> 
<div id="divide2-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="divide2-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="divide2-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "while denominator == 0:\n" +
    "    print(&quot;You can&#039;t divide by zero!&quot;)\n" +
    "    denominator = int(input(&quot;Enter a nonzero denominator: &quot;))\n" +
    "if int(numerator / denominator) * denominator == numerator:\n" +
    "    print(&quot;Divides evenly!&quot;)\n" +
    "else:\n" +
    "    print(&quot;Doesn&#039;t divide evenly.&quot;)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "divide2-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.UnitTestGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "divide2-sortableTrash",
    "unittests": "import unittestparson\nclass myTests(unittestparson.unittest):\n  def test_0(self):\n    self.assertEqual(,,)\n_test_result = myTests().main()"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#divide2-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#divide2-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
