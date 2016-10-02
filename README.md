TAMUHACK 2016


The Anti-Bully Bot


A project by:

Francine Lapid 
Alexis Maldonado 
Christian Ortega 
Noah Ortega

NOTES:

install praw
install oauthutil
install pip IBM Waton Tone Analyzer


Introduction:

Everyday millions of people use the internet for various purposes, much of which involves user-to-user interaction that includes social media websites such as Facebook, Twitter, Youtube, and chat functions of video games. Although there are many nice people on the internet, there are many who are not and turn to cyberbullying -- an unacceptable act that must be dealt with.

The goal of this project is to reduce and ultimately eliminate online harassment by creating a bot that can help solve this issue while also spreading online harassment awareness. This bot will be created to monitor and deal with encounters of harassment on reddit.com, but could eventually be used on other websites assuming the websites allows anti-bullying bots.

This bot will primarily deal with the prevention of online harassment by tackling the issues of the following: mob mentality (where a small number of users create a bullying avalanche effect), doxing (where users publish private or identifying information about a particular individual on the internet), and documentation (recording the instances in which a user is harassed).

Design:

The bot is created by using the Reddit API called praw. The bot logs into reddit.com and continuously runs the program.

In order to address mob mentality, the bot first pulls posts from the “hot” filter tab at the top of the page, which has posts in sorted from most popular to least popular (note: the code can be changed to look at all posts on reddit.com). Then, the bot iterates through each post and comment and detects if a comment is personal information (address, phone number, email address). If the comment is deemed as containing personal information (containing an address and either a phone number and an email address), the comment will be reported and a .txt file of the incident will be generated with the time, username of the harasser, why the comment was flagged, and the original comment. Additionally, the user will be sent a private message alerting that they have posted personal information to a reddit post, and explaining that cyberbulling is not acceptable and provide a link to take the pledge to create a more safe, harassment-free world.

Additionally, the bot also runs a tone detection on the comments through the use of IBM’s Watson Tone Detection API. If the tone of a comment exceeds the “anger” and/or “disgust” threshold established, then the bot will auto-comment a paragraph explaining that bullying is not acceptable through any forms of media. Through this function, the “mob mentality” that occurs on online forums, such as Reddit, will be prevented by reminding users that such negative behavior is unacceptable and that online users are people.

Summary

This proof-of concept application of the anti-bullying bot successfully monitors and deals with situations of online harassment by running continuouly. It is known that many major social media websites do not allow bots, though perhaps this is something websites should begin to consider. For now, APIs such as IBM’s Tone Detection API could be used to study and analyze the data of cyberbullying to develop efficient and effective ways of combating harassment.
