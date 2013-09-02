php-twitter-proxy
=================

A server-side OAuth proxy for pulling a user's tweets and returning them as json. Use in conjunction with ajax to display a user's Twitter feed on a website. Compatibile with Twitter API 1.1


## Installation
PHP 5.3 and php5-curl are required

Copy the contents of `credentials.php.sample` to a new `credentials.php` file, and update with your API keys from Twitter.

Initialize the codebird submodule by executing
`git submodule init`
`git submodule update`

## Parameters
The following GET parameters are accepted by the script.
-	`screen_name` - Twitter screen name (required)
-	`count` - Number of tweets to return (required)
-	`exclude_replies` - Whether to exclude @ replies. Accepted values 0 or 1. Default is 1 (optional)
-	`include_rts` - Whether to exclude retweets. Accepted values 0 or 1. Default is 1 (optional)

## Output
The output is a json array of objects corresponding to each tweet. Each object has a `tweet` and `time` parameter for the tweet text and relative time string respectively.
