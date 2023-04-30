# GenderMag Recorders Assistant Style Guide

## Formatting : 
  - Line length (column limit)
    - Column limit is 80 characters. Any line exceeding said limit must be wrapped.
  - Line wrapping
    - Lines preferably should be broken at a higher syntactic level.
    - The syntactic levels(from highest to lowest): assignment, division, function call, parameters, number constant.
    - Each continuation line must be indented at least +4 from the original line.
  - Semi colons
    - Semicolons are required immediately at the end of their respective lines.
  - Curly brackets/braces
    - Required by all control structures. The first statement of a non-empty block must begin on its own line.
    - Be concise, empty blocks can be closed immediately after opening.
    - No line break before opening brace
    - Line breaks after opening and closing brace, and before closing brace.
          ex.  function preActionQuestions(el){
                    //get persona name and pronouns to set question text
                    var personaName = getVarFromLocal("personaName");
                    var pronoun = getVarFromLocal("personaPronoun");
                    var possessive = getVarFromLocal("personaPossessive");
                    $(el).find("#preActQ").html("Will " + personaName+ " know what to do at this step?");
                    $(el).find("#preFacets").html("Which of " + personaName + 
                                                  "'s facets did you use to answer the above question?");
                    });
    
## Naming and Comments: 
  - Naming 
    - Method and package names are written in lowerCamelCase, private methods end with _
        ex.  privateMethod_()
    - Class, interface, record, typedef, and enum names are written in UpperCamelCase.
        ex.  class ExampleClass {
                constructor() {
                  // constructor method
                }
              }
    - Constant names use all uppercase words separated by underscores.
        ex. const MAXIMUM_NUMBER_OF_ITEMS = 10;
    - Method names are typically verbs / verb phrases
        ex. calculateSum()
  - Function header comments
    - Function name, description, and parameters need to be listed before each function.
  - File header comments
    - File name, functions, and descriptions need to be listed at the top of each file.
        ex. /* Function: importStylesheet
             * Description: This function is used to add another stylesheet to an element
             * Takes 2 arguments:
             * 		el: the element to which the stylesheet will be appended
             *		file: the LOCAL path of the template to use (e.g., "/styles/styles.css")
             *
             * Pre: element el must exist
             * Post: Stylesheet will be added to the element.
             */
            function importStylesheet(el, file){
  - Comments in general
    - Block comments should be on the same level as the rest of the code
    - Subsequent lines must be aligned with *
    - Parameter name comments are preferred to be included with a “=”
        ex.  //initialize obj with "status object" item
            function initStatusObject () {
                var obj = JSON.parse(localStorage.getItem("statusObject"));
                if (obj) {
                    //console.log("statusObject found");
                }
                else {
                    localStorage.setItem("statusObject", JSON.stringify(statusObject));  
                    //console.log("Initializing status object...");
                }
            }
  - File naming convention
    - All lowercase and can include underscores and dashes. 
    - Name is an overly simplified version of the task the function performs
       ex. function add_Numbers(num1, num2) {
                return num1 + num2;
              }

## Other general:
  - CSS alphabetical order
    - All statements in CSS files must be included in alphabetical order
          ex. button {
              background-color: #ffffff;
              border: 1px solid #000000;
              color: #000000;
              cursor: pointer;
              font-size: 16px;
              padding: 8px 16px;
            }
