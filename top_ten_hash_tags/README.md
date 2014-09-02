## Problem 6: Top ten hash tags

Write a Python script ```top_ten.py``` that computes the ten most frequently occurring hashtags from the data you gathered in Problem 1.

Your script will be run from the command line like this:

```
$ python top_ten.py <tweet_file>
```

You should assume the tweet file contains data formatted the same way as the livestream data.

In the tweet file, each line is a Tweet object, as described in the [twitter documentation](https://dev.twitter.com/docs/platform-objects/tweets). To find the hashtags, you should not parse the ```text``` field; the hashtags have already been extracted by twitter.

Your script should print to stdout each hashtag-count pair, one per line, in the following format:

Your script should print output to stdout. Each line of output should contain a hashtag, followed by a space, followed by the frequency of that hashtag in the entire file. There should be one line per unique hashtag in the entire file. Each line should be in the format ```<hashtag:string> <frequency:float>```

For example, if you have the pair ```(bar, 30)``` in Python it should appear in the output as:

```
bar 30
```

What to turn in: the file ```top_ten.py```
