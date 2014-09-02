## Problem 4: Compute Term Frequency

Write a Python script ```frequency.py``` to compute the term frequency histogram of the livestream data you harvested from Problem 1.

The frequency of a term can be calculated as ```[# of occurrences of the term in all tweets]/[# of occurrences of all terms in all tweets]```

Your script will be run from the command line like this:

```
$ python frequency.py <tweet_file>
```

You should assume the tweet file contains data formatted the same way as the livestream data.

Your script should print output to stdout. Each line of output should contain a term, followed by a space, followed by the frequency of that term in the entire file. There should be one line per unique term in the entire file. Even if 25 tweets contain the word lol, the term lol should only appear once in your output (and the frequency will be at least 25!) Each line should be in the format ```<term:string> <frequency:float>```

For example, if you have the pair ```(bar, 0.1245)``` in Python it should appear in the output as:

```
bar 0.1245
```

If you wish, you may consider a term to be a multi-word phrase, but this is not required. You may compute the frequencies of individual tokens only.

Depending on your method of parsing, you may end up computing frequencies for hashtags, links, stop words, phrases, etc. If you choose to filter out these non-words, that's ok too.

What to turn in: The file ```frequency.py```
