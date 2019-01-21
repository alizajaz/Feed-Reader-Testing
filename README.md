# Project Overview

In this project you are given a web-based application that reads RSS feeds. The original developer of this application clearly saw the value in testing, they've already included [Jasmine](http://jasmine.github.io/) and even started writing their first test suite! Unfortunately, they decided to move on to start their own company and we're now left with an application with an incomplete test suite. That's where you come in.


## Why this Project?

Testing is an important part of the development process and many organizations practice a standard of development known as "test-driven development." This is when developers write tests first, before they ever start developing their application. All the tests initially fail and then they start writing application code to make these tests pass.

Whether you work in an organization that uses test-driven development or in an organization that uses tests to make sure future feature development doesn't break existing features, it's an important skill to have!


## What will I learn?

You will learn how to use Jasmine to write a number of tests against a pre-existing application. These will test the underlying business logic of the application as well as the event handling and DOM manipulation.


## How will this help my career?

Writing effective tests requires analyzing multiple aspects of an application including the HTML, CSS and JavaScript - an extremely important skill when changing teams or joining a new company.

Good tests give you the ability to quickly analyze whether new code breaks an existing feature within your codebase, without having to manually test all of the functionality.


# Development Strategy

For a refresher (or reference) before you begin writing code, we recommend reviewing the content from [JavaScript Testing](https://www.udacity.com/course/javascript-testing--ud549). Your project will be evaluated by a Udacity code reviewer according to the [Feed Reader Testing project rubric](https://review.udacity.com/#!/rubrics/18/view). Please review for detailed project requirements.

1. Familiarize yourself with the starter code
    * Open up `index.html` and review the functionality of the application within your browser
    * What is all the code in `app.js` doing? Be sure to read all code comments
    * Check out `style.css`. How is styling applied to the application?
2. Explore the Jasmine spec file in `feedreader.js`
    * This is the file in which you'll be writing your tests
    * Make sure to read all code comments here as well
    * Review the [Jasmine documentation](http://jasmine.github.io) if needed
3. Edit the `allFeeds` variable in `app.js` to make the provided test fail
    * See how Jasmine visualizes this failure in your application
    * Return the `allFeeds` variable to a passing state after reviewing the failed test
4. Write a test that loops through each feed in the `allFeeds` object and ensures it has a URL defined _and_ that the URL is not empty
    * For example, how would you use a `for...of` loop in this test?
5. Write a test that loops through each feed in the `allFeeds` object and ensures it has a name defined and that the name is not empty
    * Think about how you wrote the previous test. What are you testing for this time?
6. Write a new test suite named `"The menu"`
    * What are you `describe`-ing in this test suite?
7. Write a test that ensures the menu element is hidden by default
    * You'll have to analyze the HTML and the CSS to determine how the hiding/showing of the menu element is implemented
    * What code in `app.js` is directly involved with toggling the menu on and off?
8. Write a test that ensures the menu changes visibility when the menu icon is clicked. This test should have two expectations: does the menu display itself when clicked, and does it hide when clicked again?
    * Think about how you wrote the previous test. What is different this time around?
    * Which clickable element are you checking for?
    * How do you "simulate" a mouse click that element without actually clicking it?
9. Write a test suite named `"Initial Entries"`
    * What are you `describe`-ing in this test suite?
10. Write a test that ensures when the `loadFeed` function is called and completes its work, there is at least a single `.entry` element within the `.feed` container
    * How does Jasmine's `beforeEach()`function work?
    * How does the `loadFeed()` function in `app.js` work? Is it synchronous or asynchronous?
11. Write a test suite named `"New Feed Selection"`
    * What are you `describe`-ing in this test suite?
12. Write a test that ensures when a new feed is loaded by the `loadFeed` function that the content actually changes
    * How is this test different from the previous test?

Additionally, note that:

 * No test should be dependent on the results of another
 * Callbacks should be used to ensure that feeds are loaded before they are tested
 * Error handling should be implemented for undefined variables and out-of-bound array access
 * When complete, all of your tests should pass

When you're all finished, write a `README` file detailing all steps required to successfully run the application. If you have added additional tests, provide documentation for what these future features are and what the tests are checking for.

# Contributing

This repository is the starter code for _all_ Udacity students. Therefore, we most likely will not accept pull requests.



# My Contribution to this project
This project is about using Jasmine to write a number of tests against a pre-existing application. These are some of the guideline that i followed inorder to complete this project.

Step 1.
```sh
I start familialize about index.html,app.js,style.js,feedreader.js and of course review the Jasmine Documentation.

```
Step 2.
```sh
I know that i have to do something with feedreader.js inorder to change outcome. As given note: 
         /* This is our first test - it tests to make sure that the
         * allFeeds variable has been defined and that it is not
         * empty. Experiment with this before you get started on
         * the rest of this project. What happens when you change
         * allFeeds in app.js to be an empty array and refresh the
         * page?
         */
         since, they have already describe suite called 'RSS Feeds' so i added a spec with function it('are defined', function() {.At this point we just want to make sure allFeed variable is defined and has a length greater than 0.
```

Step 3.
```sh
    /* TODO: Write a test that loops through each feed
         * in the allFeeds object and ensures it has a URL defined
         * and that the URL is not empty.
         */
         
         As you can see you have to loop through each feed. there are many ways to loop, however, i used allFeeds.forEach(function(feed){. here we have to focus on "URL". 
         a. ensures it has a URL defined
         b that the URL is not empty.
         we can basically passed variable inside expect and check whether the variable is defined or not . Also, second line of code define the value of  length is greater than 0.
        
```
Step 4.
```sh
 Write a test that loops through each feed in the allFeeds object and ensures it has a name defined and that the name is not empty.
 (Similar to step 3 except chane the Url to name)
 
```

Step 5.
```sh
 /* TODO: Write a test that ensures the menu changes
          * visibility when the menu icon is clicked. This test
          * should have two expectations: does the menu display when
          * clicked and does it hide when clicked again.
          */
          
          for this, i went to console and see what happen when i click the menu icon first time and second time. What are the differences that you see during first click and second. I used jquery with hasClass method that return true or false.
          
 ```
 Step 6.
```sh
    /* TODO: Write a test that ensures when the loadFeed
           * function is called and completes its work, there is at least
           * a single .entry element within the .feed container.
           * Remember, loadFeed() is asynchronous so this test will require
           * the use of Jasmine's beforeEach and asynchronous done() function.
           */
For this test I must load any feed using the ‘loadFeed()’ function and when loaded, I should check that there is at least one element with the class ‘entry’ within the element with the class ‘feed’.And the length of the entry should be greater than 0. 

 ```
 
  Step 7.
```sh
    /* TODO: Write a test that ensures when a new feed is loaded
         * by the loadFeed function that the content actually changes.
         * Remember, loadFeed() is asynchronous.
         */

Since evrey test is independent, i have to load two feeds such as prevFeedData and newFeedData . Also, loadFeed is asynchronous, any code that depends on its completion or that must run after its completion, must go within the callback function provied to loadFeed. When the call is done, and all feed are done loading then the tests are ready to go.
 ```

          
