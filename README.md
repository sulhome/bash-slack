# postToSlack.sh

postToSlack.sh is a bash script that will allow the ability to send slack channel messages via the command line or through other scripts.

## Setup
1. ```git clone git@github.com:maskeda/bash-slack.git```
2. Put file in your favorite bin location, i.e., ```cp postToSlack.sh /usr/local/bin/postToSlack.sh```
3. ```chmod a+x postToSlack.sh```

## Usage
This bash script is utilizing <a href="https://curl.haxx.se/" />curl</a> to post a message to a given slack channel. The script expects 4 arguments:
```
usage: ./postToSlack.sh [-t "sample title"] [-b "message body"] [-c "mychannel"] [-u "slack url"]
	-t    the title of the message you are posting
	-b    The message body
	-c    The channel you are posting to
	-u    The slack hook url to post to
```

Command line example:
```postToSlack -t "this is a title" -b "this is a message body" -c "sulhome" -u "<slack hook url>"```

## Calling from other scripts
Example from <a href="https://github.com/sulhome">sulhome</a>:

```
#!/usr/bin/env bash

statusCode=$(postToSlack -t "this is a title" -b "this is another a message body" -c "sulhome" -u "<slack hook url>")

if [[ ${statusCode} == "200" ]]; then
    echo "posted successfully"
else
    echo "error"
fi
```

## Background
This script was created by <a href="https://github.com/sulhome">sulhome</a> for a blog he had written, <a href="http://www.sulhome.com/blog/12/post-messages-to-slack-from-bash" target="_blank">Post messages to slack from Bash</a>. This repo was forked from  <a href="https://github.com/sulhome">sulhome's</a> github repo <a href="https://github.com/sulhome/bash-slack">sulhome/bash-slack</a>.
