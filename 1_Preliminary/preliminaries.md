# **TASKS**

## Preliminaries

1. Learning basic Linux
    1. Reach at least lvl 10 in this game: [Overthewire](http://overthewire.org/wargames/bandit/) (~ 2-2,5 hours)

2. Learning Markdown
    1. Finish this tutorial: [Markdown](https://www.markdowntutorial.com/) (~ 1 hour)

3. Learning GitHub and Git
    1. Finish this tutorial: [GitHub](https://guides.github.com/activities/hello-world/) (~ 30 mins)
		1. Pro git documentation: https://git-scm.com/book/en/v2
        2. Some help: https://rogerdudler.github.io/git-guide/
        3. Some more help: http://marklodato.github.io/visual-git-guide/index-en.html

4. Learning a bit of HTTP via Postman
    1. Download Postman at https://www.postman.com/
    2. You can play around with it by following https://learning.postman.com/docs/developer/echo-api/ or try interacting with another HTTP API like the one of GitHub https://docs.github.com/en/rest.

5. Learning Node.js: Choose one of the following
    1. (Free) Simple tutorial: [Tutorialspoint](https://www.tutorialspoint.com/nodejs/index.htm)
    2. (Free) More about the language and frequently used patterns: [Eloquent](https://eloquentjavascript.net/)
    3. (Paid) [Udemy](https://www.udemy.com/the-complete-nodejs-developer-course-2/) (> 10 hours)
  
  No matter what tutorial, you choose make sure to learn what is:
* The language syntax (e.g. how is a for loop is written, how do you declare variables)
* Working with local packages, npm, publishing packages. Understand what is a package.json
* Asynchronous programming with callbacks, promises. You can use the `readFile` function of the `fs` package. It has different usages which should make this clear. 
* JSON format. Make sure you are comfortable with parsing and navigating JSONs.
* Handling basic HTTP requests and sending HTTP requests. You can check [Express.js](https://expressjs.com/) for handling HTTP requests and the [fetch](https://www.npmjs.com/package/node-fetch) for sending them.

6. Learning JSON and JSON Schema:
   1. JSON: JSON is a data payload format, comparable to XML. JSON is very very popular so you should be able to find a lot of help online. A tutorial is [this](https://www.tutorialspoint.com/json/json_overview.htm). Never forget that JSON is not specific to any language or platform. You can use [this](https://jsonlint.com/) to validate your JSON.
      1. Write the following JSON: An object with properties of every JSON type
      2. Write the following JSON: An array with items of every JSON type

   2. JSON Schema: Finish this non-interactive tutorial: [JSON-schema](https://json-schema.org/understanding-json-schema/) (~ 4 hours). This is basically explaining the [specification of JSON Schema](https://json-schema.org/specification.html).
      1. During this tutorial, keep writing small JSON Schemas and validating them with an online JSON Schema validator. [An example](https://www.jsonschemavalidator.net/)
      2. Write a JSON Schema for the JSON you wrote in 6.1.1. This means that your JSON in 6.1.1 should pass this schema but e.g. a JSON with a property that should be boolean but isn't should not pass.
      3. Same for 6.1.2
      4. Write a JSON Schema that gives the following validation results:
   
      ```
        [1,2,3,4]  OK

        [3,2,4,1] OK

        [1,2,3,4,3] Not OK

        [1,2,3,5] Not OK

        [1,1,1,1] Not OK
	
      ```

      5. Write a JSON Schema that gives the following validation results (this is not an easy exercise):

   ```
            { "led": 32 ,
            "color": {"red":20, "blue":40, "green":20 }
            }  OK

            { "led": 32 ,
            "color": {"red":20, "blue":40, "green":20 },
            "tyuiejtysahb": any type except array
            } Not OK

            { "led": 32 ,
            "color": {"red":20, "blue":40, "green":20 },
            "safdgsdtgjs": []
            } OK

            { "led": 32 ,
            "color": {"red":20, "blue":40, "green":20 },
            "aosfdihsdsa":[]
            } OK

            { "led": 32 ,
            "color": {"red":20, "blue":40, "green":20 },
            "gahfodasfh":[]
            } OK
   ```
