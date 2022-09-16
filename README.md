# Facebook Chat Statistics

A small program written in Python 3 that lets you see statistics of any Facebook Messenger conversation. This project started of as a Valentines day surprise for my girlfriend inspired by [this](https://www.reddit.com/r/dataisbeautiful/comments/7xicua/my_girlfriend_made_a_visualization_of_all/) Reddit post.

## Features

The program fetches data such as:

* Start time
* End time
* Number of days
* Number of messages
* Number of words
* Average length of messages
* Average messages per day
* Most used emojis

It also generates a PDF containing the following plots (see pictures below)

* Who texts the most
* Timeline
* Activity by day
* Activity by weekday
* Most used emojis and who sent them

## Images

<img src="pics/who_texts_the_most.png"/>
<img src="pics/timeline.png">
<img src="pics/activity_by_day.png">
<img src="pics/activity_by_week.png">
<img src="pics/top_10_emojis.png">

## Running locally

Firstly you will need to [download](https://github.com/davidkrantz/FacebookChatStatistics/archive/master.zip) or clone the repository, the latter can be done by typing
```
git clone https://github.com/davidkrantz/FacebookChatStatistics.git
```
in your terminal.

### Download your Facebook conversations to a .json file
Download your Facebook data by following [these](https://www.facebook.com/help/212802592074644?helpref=uf_permalink) instructions and chosing the format to be JSON. Note that you only have to download your messages in order for this program to work.
I had to combine my messages to a larger json file using the terminal:

go to the folder where all json files are, select all and rename the first one as "yourchoice", by doing this all will be in sequential order i.e. yourchoice1,yourchoice2 ...

next go to cmd and type : copy *.json "outputfilename".json

All of your json files are merged sequentially into the "outputfilename".json file

### Download the font to show emojis
If you don't do this, some emojis may not show correctly. You should download this family https://fonts.google.com/noto/specimen/Noto+Emoji and extract it and put them all under a folder named "static" which is inside the same folder as the code. (if it doesn't exist, create it).

### Run it
1. First you will have to install the needed packages. These are listed in the `requirements.txt` file and *should* be easily installed using `pip` with
```
pip3 install -r /path/to/requirements.txt
```

2. Run the script as below with the path to your JSON conversation as an argument, for example
```
python3 facebook_chat_statistics.py /Path/To/Conversation.json
```

**NOTE:** The number of top emojis is default set to 10, but can easily be changed to some other integer by changing the line `nbr_of_top_emojis = 10` in `facebook_chat_statistics.py`.

### Enjoy!
