## Creating a Coffee Machine

1. Understand this standard: [Thing Description](https://www.w3.org/TR/wot-thing-description/)
	1. This standard is part of Web of Things, which is detailed in [the architecture document](https://w3c.github.io/wot-architecture/). This document can help you to understand the concept rather than the document format. 
	2. Web of Things is a concept that is being standardized by W3C. However, there are other people/organisations talking about it. Do not copy them but use them only to learn the concept. Some examples are from Mozilla and the book called Building the Web of Things.

2. Write a TD of a coffee machine that meets these requirements:

* name and id up to you to decide
* I should be able to read the state of the machine, like brewing, grinding, error etc.
* I should be able to brew a coffee of my choice by sending some request. You can be creative
about what your machine offers
* I should be able stop a coffee brewing process by sending some request. Just for fun, this should be done with a CoAP request.
* I should be able to turn it off remotely, only to turn it on manually later on
* It should notify me when there is not enough water, coffee beans, when its bin needs to be
emptied or in case of an error X
* I should be able to see how much water, coffee beans are left, how full the bin is

This is intentionally vague, I am expecting you to come up with something. It doesn't have one correct answer. 

Test your TD with [Playground](http://plugfest.thingweb.io/playground/). If you think that your TD is actually valid but Playground says otherwise, write a GitHub issue.

* In the end, commit this TD to the GitHub of Playground under WebContent/Examples/Valid. How you should do this is up to you to figure out but should not be a problem if you did the GitHub tutorial ^^
  
3. Install [node-wot](https://github.com/eclipse/thingweb.node-wot) and whatever development environment you want. If you follow the installation steps, you will see the optional step `sudo npm run link`. I recommend to execute this step such that you can use the `wot-servient` command. Otherwise you have to call your scripts with a way longer command.
    0. Make sure that the example `counter.js` works.
        1. To interact with it, you can use [Postman](https://www.getpostman.com/).
    1. Create the coffee machine server code. Of course, you won't interact with the hardware but it should respond to requests like its TD says and node-wot should produce a TD that is similar to the TD you wrote before. 
	   1. To interact with it, you can use [Postman](https://www.getpostman.com/).
	   2. Then test your implementation with [WoT Test Bench](https://github.com/tum-ei-esi/testbench). **Warning** This tool might be a bit buggy. Ask Ege immediately if you see unintended behavior.
* node-wot is based on [WoT Scripting API](https://w3c.github.io/wot-scripting-api/), so you can always look there to understand what the functions do.

4. Now that you have a Thing working, think of a mashup idea involving this Thing and another one you can think of. Possibilities are endless so keep it simple. This is intentionally left vague. You would need to understand what a mashup is, then decide where the mashup code will work and how many entities should be involved.

 Before proceeding, check out the following tools: [WoT webui](http://plugfest.thingweb.io/webui), [virtual-thing](https://www.npmjs.com/package/virtual-thing)