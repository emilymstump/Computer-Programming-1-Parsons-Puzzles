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
    "    number += 2\n" +
    "while number &lt;=20#distractor\n" +
    "while number &lt; 20:#distractor\n" +
    "number = number + 1#distractor";
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
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


