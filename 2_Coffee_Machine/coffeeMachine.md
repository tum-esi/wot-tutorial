## Creating a Coffee Machine

1. Understand this standard: [Thing Description](https://www.w3.org/TR/wot-thing-description/)
	1. This standard is part of Web of Things, which is detailed in [the architecture document](https://w3c.github.io/wot-architecture/). This document can help you to understand the concept rather than the document format. 
	2. Web of Things is a concept that is being standardized by W3C. However, there are other people/organisations talking about it. Do not copy them but use them only to learn the concept. Some examples are from Mozilla and the book called Building the Web of Things.
	3. There are quite a bit of videos that explain WoT at the official [WoT Webpage](https://www.w3.org/WoT/videos/). 

2. Write a TD of a coffee machine that meets these requirements:

* title up to you to decide
* A Consumer should be able to read the state of the machine, like brewing, grinding, error etc.
* A Consumer should be able to brew a coffee of my choice by sending some request. You can be creative
about what your machine offers
* A Consumer should be able stop a coffee brewing process by sending some request. Just for fun, this should be done with a CoAP request.
* A Consumer should be able to turn it off remotely, only to turn it on manually later on.
* It should notify a Consumer when there is not enough water, coffee beans, when its bin needs to be
emptied or in case of an error.
* A Consumer should be able to see how much water, coffee beans are left, how full the bin is

This is intentionally vague, it is expected that you to come up with something custom. It doesn't have one correct answer. 

Test your TD with [Playground](http://plugfest.thingweb.io/playground/). If you think that your TD is actually valid but Playground says otherwise, write a GitHub issue for Playground.
  
3. Install [node-wot](https://github.com/eclipse/thingweb.node-wot) and whatever development environment you want. If you follow the installation steps, you will see the optional step `sudo npm run link`. I recommend to execute this step such that you can use the `wot-servient` command. Otherwise you have to call your scripts with a way longer command.
    0. Make sure that the example `counter.js` works.
        1. To interact with it, you can use Postman.
    1. Create the coffee machine server code. Of course, you won't interact with the hardware but it should respond to requests like its TD says and node-wot should produce a TD that is similar to the TD you wrote before. Test all your affordances via Postman and save them as a collection. There is a shortcut to this if you are lazy but adventurous to explore some of the tools.
    2. Do the same step above but install the node-wot packages of your choice via npm.

4. Now that you have a Thing working, think of a mashup idea involving this Thing and another one you can think of. Possibilities are endless so keep it simple. This is intentionally left vague. You would need to understand what a mashup is, then decide where the mashup code will work and how many entities should be involved. One example (which you should not copy) would be that you can do mashup of an alarm clock with the coffee machine so that each time the wake up alarm rings, a coffee brewing starts.
