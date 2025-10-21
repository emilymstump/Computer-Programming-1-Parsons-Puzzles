---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Practice with For Loops
---

## Average Test Score
Write a program that asks the user for three test scores. The program should then report the average of these three scores.

<div id="test-sortableTrash" class="sortable-code"></div> 
<div id="test-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="test-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="test-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "total = 0\n" +
    "for i in range(3):\n" +
    "    score = float(input(&quot;Enter a test score&quot;))\n" +
    "    total = total + score\n" +
    "average = total/3\n" +
    "print(&quot;Average score:&quot;,average)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "test-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "test-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#test-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#test-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## How many names?
Some people have just a first name and a last name. Some people also have a middle name. Some people have five middle names. Write a program that asks the user how many names they have. (If they have a first name, two middle names, and a last name, for example, they would type 4.) Then, using a for loop, ask the user for each of their names. Finally, print their full name.

<div id="names-sortableTrash" class="sortable-code"></div> 
<div id="names-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="names-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="names-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "number = int(input(&quot;How many names do you have? &quot;))\n" +
    "full_name = input(&quot;Enter your first name: &quot;)\n" +
    "for i in range(number-1):\n" +
    "    next_name = input(&quot;Enter your next name: &quot;)\n" +
    "    full_name = full_name + &quot; &quot; + next_name\n" +
    "print(&quot;Your name is &quot; + full_name)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "names-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "names-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#names-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#names-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


## Categories
Write a program that asks the user for three categories. For each category, ask the user for three things in that category. You should print something for each category that states the category and the three things in that category.

<div id="categories-sortableTrash" class="sortable-code"></div> 
<div id="categories-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="categories-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="categories-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "for i in range(3):\n" +
    "    category = input(&quot;Enter a category: &quot;)\n" +
    "    things = &quot;&quot;\n" +
    "    for j in range(3):\n" +
    "        new_thing = input(&quot;Enter something in the category &quot; + category + &quot;: &quot;)\n" +
    "        things = things + &quot; &quot; + new_thing\n" +
    "    print(category + &quot;: &quot; + things)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "categories-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "categories-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#categories-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#categories-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


## Average of Numbers
Write a program that averages together all numbers that a user inputs. First, ask the user how many numbers they want to average. Then use a for loop to ask the user for each number one by one. Finally, print the average of all the numbers.

<div id="numbers-sortableTrash" class="sortable-code"></div> 
<div id="numbers-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="numbers-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="numbers-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "number = int(input(&quot;How many numbers do you want to average? &quot;))\n" +
    "total = 0\n" +
    "for i in range(number):\n" +
    "    next_number = int(input(&quot;Enter a number: &quot;))\n" +
    "    total = total + next_number\n" +
    "average = total/number\n" +
    "print(average)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "numbers-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "numbers-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#numbers-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#numbers-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


## Multiplication Table
Write a program that creates a multiplication table. A multiplication table is a table in which each entry is equal to the product of the corresponding row and column number. Have the numbers start at 1. Ask the user to input what number they want the table to go up to.

Example output if the user picks 5:

&nbsp;&nbsp;&nbsp;1&nbsp;&nbsp;2&nbsp;&nbsp;3&nbsp;&nbsp;4&nbsp;&nbsp;5
    
1&nbsp;&nbsp;1&nbsp;&nbsp;2&nbsp;&nbsp;3&nbsp;&nbsp;4&nbsp;&nbsp;5
 
2  2  4  6  8 10
 
3  3  6  9 12 15
 
4  4  8 12 16 20
 
5  5 10 15 20 25

<div id="mult-sortableTrash" class="sortable-code"></div> 
<div id="mult-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="mult-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="mult-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "num_rows = int(input(&quot;How many rows (between 1 and 9)? &quot;))\n" +
    "first_row = &quot; &quot;\n" +
    "for i in range(num_rows):\n" +
    "    first_row = first_row + &quot;  &quot; + str(i+1)\n" +
    "print(first_row)\n" +
    "for i in range(1,num_rows+1):\n" +
    "    next_row = str(i)\n" +
    "    for j in range(1,num_rows+1):\n" +
    "        table_entry = i*j\n" +
    "        if table_entry &lt; 10:\n" +
    "            next_row = next_row + &quot;  &quot; + str(table_entry) # Extra space for single digit numbers\n" +
    "        else:\n" +
    "            next_row = next_row + &quot; &quot; + str(table_entry)\n" +
    "    print(next_row)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "mult-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "mult-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#mult-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#mult-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
