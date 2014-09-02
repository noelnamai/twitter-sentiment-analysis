## Problem 1: Get Twitter Data

As always, the first step is to [make sure your assignment materials up to date](https://class.coursera.org/datasci-002/wiki/GithubInstructions).

To access the live stream, you will need to install the [oauth2 library](https://pypi.python.org/pypi/oauth2/) so you can 
properly authenticate.

This library is already installed on the class virtual machine, but you can install it yourself in your Python environment. (The command ```$ pip install oauth2``` should work for most environments.)

The steps below will help you set up your twitter account to be able to access the live 1% stream.

1. Create a twitter account if you do not already have one.
2. Go to [https://dev.twitter.com/apps](https://apps.twitter.com/) and log in with your twitter credentials.
3. Click "Create New App"
4. Fill out the form and agree to the terms. Put in a dummy website if you don't have one you want to use.
5. On the next page, click the "API Keys" tab along the top, then scroll all the way down until you see the section "Your Access Token"
6. Click the button "Create My Access Token". You can Read more about Oauth authorization.
7. You will now copy four values into twitterstream.py. These values are your "API Key", your "API secret", your "Access token" and your "Access token secret". All four should now be visible on the API Keys page. (You may see "API Key"
referred to as "Consumer key" in some places in the code or on the web; they are synonyms.) Open twitterstream.py and 
set the variables corresponding to the api key, api secret, access token, and access secret. You will see code like the 
below:
```
api_key = "<Enter api key>"
api_secret = "<Enter api secret>"
access_token_key = "<Enter your access token key here>"
access_token_secret = "<Enter your access token secret here>"
```
8. Run the following and make sure you see data flowing and that no errors occur.


```
$ python twitterstream.py > output.txt
```
This command pipes the output to a file. Stop the program with Ctrl-C, but wait at least 3 minutes for data to accumulate. Keep the file output.txt for the duration of the assignment; we will be reusing it in later problems. Don't use someone else's file; we will check for uniqueness in other parts of the assignment.
9. If you wish, modify the file to use the [twitter search API](https://dev.twitter.com/docs/api/1.1/get/search/tweets) 
to search for specific terms. For example, to search for the term "microsoft", you can pass the following url to the 
twitterreq function:
```
https://api.twitter.com/1.1/search/tweets.json?q=microsoft
```
What to turn in: The first 20 lines of the twitter data you downloaded from the web. You should save the first 20 lines 
to a file ```problem_1_submission.txt``` by using the following command:
```
$ head -n 20 output.txt > problem_1_submission.txt
```
