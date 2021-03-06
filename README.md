## TwitteR - introductory session

This material covers a VERY basic introduction to some of the functionality provided by the `twitteR` package for R.

It borrows heavily from multiple sources: 

 - https://github.com/pablobarbera/social-media-workshop
 - http://www.rdatamining.com/docs/r-and-data-mining-examples-and-case-studies
 - http://www.r-bloggers.com/playing-with-twitter-data/

### R libraries

The main R package used during this session is `twitteR`.  You can install this via:

```r
install.packages("twitteR", repos="http://cran.stat.auckland.ac.nz")
```

### Getting started

In order to use the Twitter API* to gather data, you need to create a "Twitter app" (you also need a Twitter account).  This process generates an authentication tiken that can be used from within R to gain access to tweet data via the API.

 - Step 1: go to apps.twitter.com and sign in
 - Step 2: click on "Create New App"
 - Step 3: fill name, description, and website (it can be any website): make sure you leave 'Callback URL' empty.
 - Step 4: agree to user conditions
 - Step 5: get key and token information from "Keys and Access Tokens" tab: copy these and paste them into the R code below.

 *API = Application program interface: "set of routine definitions, protocols, and tools for building software and applications. A good API makes it easier to develop a program by providing all the building blocks, which are then put together by the programmer": https://en.wikipedia.org/wiki/Application_programming_interface

### Using the token info in R

```r
consumerKey = "XXXXXXXXXXXX"
consumerSecret = "YYYYYYYYYYYYYYYYYYY"
accessToken = "ZZZZZZZZZZZZZZ"
accessSecret = "AAAAAAAAAAAAAAAAAA"

library(twitteR)
setup_twitter_oauth(consumer_key=consumerKey, consumer_secret=consumerSecret,
		    access_token=accessToken, access_secret=accessSecret)
```

### Using the R twitteR package

Once the token information is set up, it can be used to query timeline data via the twitter API.

The code and instructions for this session are contained in the `twitteR-intro.Rmd` and `twitteR-intro.html` files in this repository.  Rendered HTML:

https://rawgit.com/mikblack/twitteR-intro/master/twitteR-intro.html

Scroll down to "Using the twitteR package" to get started in R.
