---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Practice with While and For Loops
---
# Parsons Practice

## Smoothie Maker
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


