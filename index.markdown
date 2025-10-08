---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Multiple Parson's Problems on One Page
---
# Parsons Practice

## Parsons 1 (Line Based Grader)
Re-arrange the blocks below so they make the smoothie program

<div id="example-sortableTrash" class="sortable-code"></div> 
<div id="example-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="example-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="example-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "print(“You’re making a smoothie”)\n" +
    "ingredients_added = 0\n" +
    "ingredient_list = “”\n" +
    "while ingredients_added &lt; 5:\n" +
    "	ingredient = input(“Add an ingredient to your smoothie (or type &#039;done’): ”)\n" +
    "	if ingredient == “done”:\n" +
    "		print(“Finishing your smoothie early!”)\n" +
    "		break\n" +
    "	print(“Added ” + ingredient + “ to the blender.”)\n" +
    "	ingredient_list = ingredient_list + ingredient + “ ”\n" +
    "	ingredients_added += 1\n" +
    "print(“Your ” + ingredient_list + “smoothie is ready!”)\n" +
    "print(“Total number of ingredients: ” + str(ingredients_added))\n" +
    "if ingredient == done#distractor\n" +
    "if ingredient = &quot;done&quot;#distractor\n" +
    "print(&quot;ingredient)#distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "example-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.UnitTestGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "example-sortableTrash",
    "unittests": "import unittestparson\nclass myTests(unittestparson.unittest):\n  def test_0(self):\n    self.assertEqual(,,)\n_test_result = myTests().main()"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#example-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#example-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## Parsons 2 (Variable Check Grader)
Construct a program that swaps the values of variables <code>x</code> and <code>y</code> using the helper variable <code>tmp</code>. You can change the names of the variables (<span class="jsparson-toggle"></span>) by clicking them.

<div id="p2-sortableTrash" class="sortable-code"></div>
<div id="p2-sortable" class="sortable-code"></div>
<div style="clear:both;"></div>
<p>
    <input id="p2-feedbackLink" value="Get Feedback" type="button" />
    <input id="p2-newInstanceLink" value="Reset Problem" type="button" />
</p>
<script type="text/javascript">
(function(){
  var initial = "$$toggle::x::y::tmp$$ = $$toggle::x::y::tmp$$\n" +
    "$$toggle::x::y::tmp$$ = $$toggle::x::y::tmp$$\n" +
    "$$toggle::x::y::tmp$$ = $$toggle::x::y::tmp$$";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "p2-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.VariableCheckGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "p2-sortableTrash",
    "vartests": [
        {
            "message": "Testing with initial variable values x = 3 and y = 4",
            "initcode": "x = 3\ny = 4",
            "code": "",
            "variables": {}
        },
        {
            "message": "Testing with initial variable values x = 0 and y = 2",
            "initcode": "x = 0\ny = 2",
            "code": "",
            "variables": {}
        }
    ]
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#p2-newInstanceLink").click(function(event){
      event.preventDefault();
      parsonsPuzzle.shuffleLines();
  });
  $("#p2-feedbackLink").click(function(event){
      event.preventDefault();
      parsonsPuzzle.getFeedback();
 });
})();
</script>

## Parsons 3 (Unit Test Grader)
Your task is to construct a function which returns the index of the largest element in the array.

<div id="p3-sortableTrash" class="sortable-code"></div>
<div id="p3-sortable" class="sortable-code"></div>
<div style="clear:both;"></div>
<p>
    <input id="p3-feedbackLink" value="Get Feedback" type="button" />
    <input id="p3-newInstanceLink" value="Reset Problem" type="button" />
</p>
<script type="text/javascript">
(function(){
  var initial = "def maxindex(arg):\n" +
    " ans = 0\n" +
    " for i in range(len(arg)):\n" +
    " if arg[i] > arg[ans]:\n" +
    " ans = i\n" +
    " while True:\n" +
    "pass\n" +
    " return ans";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "p3-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.UnitTestGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "p3-sortableTrash",
    "unittests": "import unittestparson\nclass myTests(unittestparson.unittest):\n  def test_0(self):\n    self.assertEqual(,,)\n_test_result = myTests().main()"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#p3-newInstanceLink").click(function(event){
      event.preventDefault();
      parsonsPuzzle.shuffleLines();
  });
  $("#p3-feedbackLink").click(function(event){
      event.preventDefault();
      parsonsPuzzle.getFeedback();
  });
})();
</script>

## Parsons 4 (Language Translation Grader)
Print out "I am a Java program" three times using a for loop.

<div id="p4-sortableTrash" class="sortable-code"></div>
<div id="p4-sortable" class="sortable-code"></div>
<div style="clear:both;"></div>
<p>
    <input id="p4-feedbackLink" value="Get Feedback" type="button" />
    <input id="p4-newInstanceLink" value="Reset Problem" type="button" />
</p>
<script type="text/javascript">
(function(){
  var initial = "for (int i=0;i<3;i++) {\n" +
    "System.out.print(\\\"I \\\");\n" +
    "System.out.print(\\\"am \\\");\n" +
    "System.out.print(\\\"a Java program \\\");\n" +
    "}";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "p4-sortable",
    "max_wrong_lines": 1,
    "grader": ParsonsWidget._graders.LanguageTranslationGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "executable_code": "for x in range(3):\n    output += 'I '\n    output += 'am '\n    output += 'a Java program '\npass",
    "programmingLang": "java",
    "vartests": [
        {
            "message": "Testing...",
            "initcode": "output = ''",
            "code": "",
            "variables": {
                "output": "I am a Java program I am a Java program I am a Java program "
            }
        }
    ]
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#p4-newInstanceLink").click(function(event){
      event.preventDefault();
      parsonsPuzzle.shuffleLines();
  });
  $("#p4-feedbackLink").click(function(event){
      event.preventDefault();
      parsonsPuzzle.getFeedback();
   });
})();
</script>


## Parsons 5 (Turtle Grader)
Construct a program by dragging&amp;dropping and reordering lines. The constructed program should draw a triangle like shown below.

<div id="p5-sortableTrash" class="sortable-code"></div>
<div id="p5-sortable" class="sortable-code"></div>
<div style="clear:both;"></div>
<p>
    <input id="p5-feedbackLink" value="Get Feedback" type="button" />
    <input id="p5-newInstanceLink" value="Reset Problem" type="button" />
</p>
<script type="text/javascript">
(function(){
  var initial = "REPEAT 3 TIMES\n" +
    "  forward(100)\n" +
    "  left(120)\n" +
    "ENDREPEAT";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "p5-sortable",
    "max_wrong_lines": 1,
    "grader": ParsonsWidget._graders.TurtleGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "p5-sortableTrash",
    "executable_code": "for i in range(0,3):\nmyTurtle.forward(100)\nmyTurtle.left(120)\npass",
    "programmingLang": "pseudo",
    "turtleModelCode": "modelTurtle.forward(100)\nmodelTurtle.left(120)\nmodelTurtle.forward(100)\nmodelTurtle.left(120)\nmodelTurtle.forward(100)\nmodelTurtle.left(120)",
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#p5-newInstanceLink").click(function(event){
      event.preventDefault();
      parsonsPuzzle.shuffleLines();
  });
  $("#p5-feedbackLink").click(function(event){
      event.preventDefault();
      parsonsPuzzle.getFeedback();
  });
})();
</script>



