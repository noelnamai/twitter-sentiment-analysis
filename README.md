## Twitter Sentiment Analysis in Python: Instructions

Twitter represents a fundamentally new instrument to make social measurements. Millions of people voluntarily express opinions across any topic imaginable --- this data source is incredibly valuable for both research and business.

For example, researchers have shown that the "mood" of communication on twitter [reflects biological rhythms](http://www.nytimes.com/2011/09/30/science/30twitter.html) and can even used to [predict the stock market](http://arxiv.org/pdf/1010.3003&embedded=true). A student here at UW used geocoded tweets to [plot a map of locations where "thunder" was mentioned in the context of a storm system in Summer 2012](http://cliffmass.blogspot.com/2012/07/thunderstorm-fest.html).

Researchers from Northeastern University and Harvard University studying the characteristics and dynamics of Twitter have an excellent resource for learning more about how Twitter can be used to analyze moods at national scale.

In this assignment, you will

* access the twitter Application Programming Interface(API) using python
* estimate the public's perception (the sentiment) of a particular term or phrase
* analyze the relationship between location and mood based on a sample of twitter data

Some points to keep in mind:

* This assignment is open-ended in several ways. You'll need to make some decisions about how best to solve the problem and implement them carefully.
* It is perfectly acceptable to discuss your solution on the forum, but don't share code.
* Each student must submit their own solution to the problem.
* You will have an unlimited number of tries for each submission.
* Your code will be run in a protected environment, so you should only use the Python standard libraries unless you are specifically instructed otherwise. Your code should also not rely on any external libraries or web services.

### The Twitter Application Programming Interface

Twitter provides a very rich REST API for querying the system, accessing data, and control your account. You can [read more about the Twitter API](https://dev.twitter.com/docs)

### Python 2.7.3 environment

If you are new to Python, you may find it valuable to work through the [codeacademy Python tutorials](http://www.codecademy.com/tracks/python). Focus on tutorials 1-9, plus tutorial 12 on File IO. In addition, many students have recommended [Google's Python class](https://developers.google.com/edu/python/).

You will need to establish a Python programming environment to complete this assignment. You can install Python yourself by [downloading it from the Python website](https://www.python.org/download/), or can use the [class virtual machine](https://www.python.org/download/).

### Unicode strings

Strings in the twitter data prefixed with the letter "u" are unicode strings. For example:

```
u"This is a string"
```

Unicode is a standard for representing a much larger variety of characters beyond the roman alphabet (greek, russian, mathematical symbols, logograms from non-phonetic writing systems such as kanji, etc.)

In most circumstances, you will be able to use a [unicode](https://docs.python.org/2/library/stdtypes.html#str.encode) object just like a string.

If you encounter an error involving printing unicode, you can use the encode method to properly print the international characters, like this:

```
unicode_string = u"aaaÃ Ã§Ã§Ã§Ã±Ã±Ã±"
encoded_string = unicode_string.encode('utf-8')
print encoded_string
```

### Getting Started

Once again: If you are new to Python, many students have recommended [Google's Python class](https://developers.google.com/edu/python/).
