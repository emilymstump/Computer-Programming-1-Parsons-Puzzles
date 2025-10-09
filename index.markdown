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

## Higher/Lower
Write a program that makes the user guess a particular number between 1 and 100. Save the number to be guessed in a variable called magic_number. If the user guesses a number higher than the secret number, you should say Too high!. Similarly, you should say Too low! if they guess a number lower than the secret number. Once they guess the number, say Correct!

<div id="highlow-sortableTrash" class="sortable-code"></div> 
<div id="highlow-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="highlow-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="highlow-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "magic_number = 3\n" +
    "while True:\n" +
    "    guess = int(input(&quot;Enter a guess: &quot;))\n" +
    "    if guess == magic_number:\n" +
    "        print(&quot;Correct!&quot;)\n" +
    "        break\n" +
    "    elif guess &gt; magic_number:\n" +
    "        print(&quot;Too high!&quot;)\n" +
    "    else:\n" +
    "        print(&quot;Too low!&quot;)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "highlow-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "highlow-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#highlow-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#highlow-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## Calculating Averages
Ask the user to input as many numbers as they would like (one at a time). Each time they put in a number, ask them whether they would like to put in another number or whether they are done. When the user indicates that they are done, then print out the average of all the numbers they inputted.

<div id="average-sortableTrash" class="sortable-code"></div> 
<div id="average-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="average-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="average-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "total = 0\n" +
    "n = 0\n" +
    "while True:\n" +
    "    next_number = float(input(&quot;Enter the next number: &quot;))\n" +
    "    total = total + next_number\n" +
    "    n += 1\n" +
    "    another = input(&quot;Do you want to input another number? (yes/no): &quot;)\n" +
    "    if another == &quot;no&quot;:\n" +
    "        print(&quot;The average is&quot;, total/n)\n" +
    "        break";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "average-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "average-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#average-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#average-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
  $("#highlow-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## Countdown Timer
Ask the user for a starting number, then count down to zero, printing each number along the way. At the end, print "Blast off!"

<div id="countdown-sortableTrash" class="sortable-code"></div> 
<div id="countdown-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="countdown-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="countdown-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "number = int(input(&quot;Enter a number: &quot;))\n" +
    "while number &gt; 0:\n" +
    "    print(number)\n" +
    "    number -= 1\n" +
    "print(&quot;Blast off!&quot;)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "countdown-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "countdown-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#countdown-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#countdown-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
