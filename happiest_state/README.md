## Problem 5: Which State is happiest?

Write a Python script ```happiest_state.py``` that returns the name of the happiest state as a string.

Your script ```happiest_state.py``` should take a file of tweets as input. It will be called from the command line like this:

```
$ python happiest_state.py <sentiment_file> <tweet_file>
```

The file ```AFINN-111.txt``` contains a list of pre-computed sentiment score.

Assume the tweet file contains data formatted the same way as the livestream data.

It's a good idea to make use of your solution to Problem 2.

There are different ways you might assign a location to a tweet. Here are three:

* Use the coordinates ```field``` (a part of the ```place``` object, if it exists, to geocode the tweet. This method gives the most reliable location information, but unfortunately this field is not always available and you must figure out some way of translating the coordinates into a state.
* Use the other metadata in the ```place``` field. Much of this information is hand-entered by the twitter user and may not always be present or reliable, and may not typically contain a state name.
* Use the ```user``` field to determine the twitter user's home city and state. This location does not necessarily correspond to the location where the tweet was posted, but it's reasonable to use it as a proxy.

You are free to develop your own strategy for determining the state that each tweet originates from.

You may find it useful to use this [python dictionary of state abbreviations](http://code.activestate.com/recipes/577305-python-dictionary-of-us-states-and-territories/).

You can ignore any tweets for which you cannot assign a location in the United States.

In this file, each line is a Tweet object, asdescribed in the [twitter documentation](https://dev.twitter.com/docs/platform-objects/tweets).

Note: Not every tweet will have a ```text``` field --- again, real data is dirty! Be prepared to debug, and feel free to throw out tweets that your code can't handle to get something working.Â For example, you might choose to ignore all non-English tweets.

Your script should print the two letter state abbreviation of the state with the highest average tweet sentiment to stdout.

Note that you may need a lot of tweets in order to get enough tweets with location data. Let the live stream run for a while if you wish.

Your script will not have access to the Internet, so you cannot rely on third party services to resolve geocoded locations!

What to turn in: The file ```happiest_state.py```
