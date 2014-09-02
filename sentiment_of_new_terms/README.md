## Problem 3: Derive the sentiment of new terms

In this part you will be creating a script that computes the sentiment for the terms that do not appear in the file AFINN-111.txt.

Here's how you might think about the problem: We know we can use the sentiment-carrying words in AFINN-111.txt to deduce the overall sentiment of a tweet. Once you deduce the sentiment of a tweet, you can work backwards to deduce the sentiment of the non-sentiment carrying words that do not appear in AFINN-111.txt. For example, if the word ```soccer``` always appears in proximity with positive words like ```great``` and ```fun```, then we can deduce that the term soccer itself carries a positive sentiment.

Don't feel obligated to use it, but the following paper may be helpful for developing a sentiment metric. Look at the Opinion Estimation subsection of the Text Analysis section in particular.

[O'Connor, B., Balasubramanyan, R., Routedge, B., & Smith, N. From Tweets to Polls: Linking Text Sentiment to Public Opinion Time Series. (ICWSM), May 2010.](http://www.cs.cmu.edu/~nasmith/papers/oconnor+balasubramanyan+routledge+smith.icwsm10.pdf)

You are provided with a skeleton file, term_sentiment.py, which can be executed using the following command:

```
$ python term_sentiment.py <sentiment_file> <tweet_file>
```

Your script should print output to stdout. Each line of output should contain a term, followed by a space, followed by the sentiment. That is, each line should be in the format ```<term:string> <sentiment:float>```

For example, if you have the pair ```("foo", 103.256)``` in Python, it should appear in the output as:

```
foo 103.256
```

The order of your output does not matter.

What to turn in: The file ```term_sentiment.py```

How we will grade Part 3: We will run your script on a file that contains strongly positive and strongly negative tweets and verify that the non-sentiment-carrying terms in the strongly positive tweets are assigned a higher score than the non-sentiment-carrying terms in negative tweets.Â Your scores need not (and likely will not) exactly match any specific solution.

If the grader is returning "Formatting error: ", make note of the line of text returned in the message. This line corresponds to a line of your output. The grader will generate this error if ```line.split()``` does not return exactly two items. One common source of this error is to not remove the two calls to the "lines" function in the solution template; this function prints the number of lines in each file. Make sure to check the first two lines of your output!
