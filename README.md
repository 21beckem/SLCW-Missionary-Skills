# Missionary Skills User Guide
All about it - fill in later

## How to change the questions:

Once inside of the file manager, open the script.js file to edit the questions.  The first variable declaration inside this file is called formJson and stores all the data in an array of JSON objects.

This is what each object looks like:
```JSON
{
  "label" : "First Name (not Elder or Sister)",
  "type" : "text",
  "conditional" : false,
  "required" : true
}
```

* `"label"` is the text/prompt for the question.
* `"type"` is indicates what type of response will be accepted. Must be one of the following:
    * `"text"` - for short answer response
    * `"bool"` - for *yes* or *no*
    * `"range"` - for a slider between 1 and 5
* `"conditional"` Tells the website to only show this question of the next nonconditional question above it is marked as *yes*
* `"required"` tells whether or not the question should be required to submit the form.

## Common Fixes

* If you just changed some of the JSON and all of a sudden the page shows no quations at all, that means your JSON data cannot be parsed by the computer. Check the Dev console.