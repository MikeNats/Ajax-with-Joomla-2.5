Ajax-with-Joomla-2.5
====================
Initially i had the below problem:

I have in my html page a link with class name ="flyer" and href="MY_HREF".
When the user click's in the link I want to load a "custom html" module with specific ID.
Can you please advise me how will be the syntax of the MY_HREF.

For example http://www.mywebsite/com_custom/id=ID.html ???


And here is the solution



1)We create our html module and we set a custom position e.x myposition

2)We create an article and we load our module {loadposition myposition}.

    Note that every article has its own ID and ALIAS.

3)The final url for our ajax call is: http://myurl.gr/ID-ALIAS.html?tmpl=component&type=raw

Note that if you add any content to the article you will get the html of the article + the html of the module.

The ajax call code is:

MY_HREF = ID-ALIAS.html

In the ajax-implementation file you will find the code.

