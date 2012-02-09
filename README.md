htmlSQL - Version 0.5
=====================

htmlSQL is a experimental PHP class which allows you to access HTML
values by an SQL like syntax. This means that you don't have to write
complex functions or regular expressions to extract specific values.

**htmlSQL queries look like this:**

    SELECT href,title FROM a WHERE $class == "list"
           ^ Attributes    ^       ^ search query (can be empty)
             to return     ^
                           ^ HTML tag to search in
                             "*" is possible = all tags

This query should return an array with all links that contain the attribute `class="list"`.


The project has been abandoned
------------------------------

htmlSQL was a experiment I made in 2006. I'm **not** supporting or extending the library anymore, this repository is only for historical purposes.
But feel free to fork, modify and study the source code. If you need a reliable library for data scraping I recommend using **other modules** (see below).


Related projects:

* PHP: [SimpleXML](http://www.php.net/dom), [DOM](http://www.php.net/dom)
* Perl: [pQuery](http://search.cpan.org/~ingy/pQuery-0.07/lib/pQuery.pm)
* Python: [Scrapy](http://scrapy.org/)
* JavaScript: [node.js](http://blog.nodejitsu.com/jsdom-jquery-in-5-lines-on-nodejs)


Related Hacker News threads:

* [PHP class to query the web by an SQL like language](http://news.ycombinator.com/item?id=2097008)
* [Ask YC: What do you scrape? How do you scrape?](http://news.ycombinator.com/item?id=159025)


Requirements
------------

- Any flavor of PHP4+ should do
- [Snoopy PHP class - Version 1.2.3](http://sourceforge.net/projects/snoopy/) (optional - required for web transfers)
  You find all Snoopy related documents (copyright, readme, etc) in the snoopy_data/ subdirectory.


Usage
-----

Just include the "snoopy.class.php" and the "htmlsql.class.php" files
into your PHP scripts and look at the examples to get an idea of how 
to use the htmlSQL class. It should be very simple :-)


Background / idea
-----------------

I had this idea while extracting some data from a website. As I realized
that the algorithms and functions to extract links and other tags are
often the same - I had the idea to combine all functions to an universal
usable class. While drinking a coffee and thinking on that problem, I
thought it would be cool to access HTML elements by using SQL. So I
started creating this class...


Warning
-------

The `eval()` function is used for the WHERE statement. Make sure that all
user data is checked and filtered against malicious PHP code.
Never trust any user input!


Todo
----

* Enhance the HTML parser
* Test htmlSQL with invalid and bad HTML files
* Replace the ugly `eval()` method for the WHERE statement with an own method
* More error checks
* Include the LIMIT function/method like in SQL


Author
------

* [Jonas John](http://www.jonasjohn.de/)


License
-------

htmlSQL uses a modified BSD license, you find the full license text in the "htmlsql.class.php".
