# postToSlack.sh

## Setup
1. ```git clone git@github.com:maskeda/bash-slack.git```
2. Put file in your favorite bin location, i.e., ```cp postToSlack.sh /usr/local/bin/postToSlack.sh```
3. ```chmod a+x postToSlack.sh```

## Usage
```
usage: ./postToSlack.sh [-t "sample title"] [-b "message body"] [-c "mychannel"] [-u "slack url"]
	-t    the title of the message you are posting
	-b    The message body
	-c    The channel you are posting to
	-u    The slack hook url to post to
```

## Background
This script was created by <a href="https://github.com/sulhome">sulhome</a> for a blog he had written, <a href="http://www.sulhome.com/blog/12/post-messages-to-slack-from-bash" target="_blank">Post messages to slack from Bash</a>. This repo was forked from  <a href="https://github.com/sulhome">sulhome's</a> github repo <a href="https://github.com/sulhome/bash-slack">sulhome/bash-slack</a>.