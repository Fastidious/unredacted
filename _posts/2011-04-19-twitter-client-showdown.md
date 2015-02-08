---
date: 2011-04-19 14:56:20 +0200
title: "Twitter Client Showdown"
category: research
tags:
  - interactions
  - ios
  - mobile
  - usability
---

Amidst the noise surrounding Twitter's new third party restrictions, [Tweetbot]---the long-awaited Twitter client from Tapbots---is finally out for iPhone and iPod Touch. The overwhelmingly positive feedback is a clear sign that the app met and even exceeded expectations.

To examine whether Tweetbot is a viable replacement for the official app, we will pit the two clients against each other using a GOMS-inspired, oversimplified [human information processing model][HIP] on a set of tasks performed by average user on Twitter.

{% include figure.html file="tweet-options.jpg" alt="Tweet options" caption="Tweet options displayed after a single tap." %}

### The Rules

Before jumping in, let's introduce some of the concepts used in this model:

* *An interaction* is any point of contact between the user and the interface, such as a tap or a swipe. Each interaction is assigned a value based on the time required to execute it. For the sake of simplicity, a *single tap* is given a nominal value of `1` and used as a base unit for other interactions.

* *A task* is any set of actions sharing the same end goal. There may be one or more set of interactions to carry out the same task. The time required to achieve a given task is considered to be equal to the sum of the individual values of each interaction involved. The lower the sum, the more efficient the interface.

* Unless stated otherwise, typing time was zeroed out.

* When two or more methods of achieving a given task are possible, only the most efficient one is used in the comparison. The impact on the overall work-flow is also taken into account.

* Only the default behavior of the triple tap is taken into consideration for Tweetbot.

The values assigned to each interaction are as follows:

| Interaction | Value
|-|:-:|
| Tap | 1
| Double tap | 1.5 |
| Swipe | 1.5 |
| Triple tap | 2 |
| Long tap | 2 |

Thinking time was assigned a value of `0.5`, and will be referred to as MOP (multi-option prompt) in the tests. For simplification purposes, the number of options was not taken into account, nor was the habit factor.

### Round 1: Basic Tasks

We'll start by having a look at how efficiently the two clients handle basic tasks such as tweeting and replying:

| Task | Tweetbot | Twitter
|-|:-:|:-:|
| Send a Tweet<sup>1</sup> | 2 | 2 |
| Reply<sup>1 2</sup>  | 3 | 4 |
| Retweet (native) | 4 | 4.5 |
| Send a new DM<sup>3</sup> | 6.5 | 5.5 |
| Open a link | 1.5 | 2 |

1. No hashtags or @ signs.
2. No other users mentioned in the original tweet
3. The tap to get to the Messages view is zeroed out

**Outcome:** draw.

The two clients are equally efficient when it comes to tweeting and retweeting. Tweetbot cleverly handles single replies and links thanks to double and triple taps, while the official client makes sending a new direct message significantly less cumbersome.

{% include figure.html file="twitter-dm.jpg" alt="Direct messaging" caption="Sending a direct message." %}

### Round 2: Hashtags, Mentions, and Group Replies

Let's now spice up the comparison with some hashtags and @ mentions:

| Task | Tweetbot | Twitter
|-|:-:|:-:|
| Compose a tweet with # and @ | 7 | 4 |
| Compose a tweet with 3 # and 2 @ | 15 | 7 |
| View conversations<sup>1</sup> | 1.5 | 2 |
| Reply all (MMT)<sup>2</sup> | 4.5 | 5 |
| Reply single (MMT)<sup>2</sup> | 4.5 | 4 |

1. Where the user takes part
2. Multi-mention tweet

**Outcome:** Twitter for iPhone wins.

Thanks to shortcuts, the official Twitter client trumps Tweetbot when it comes to composing tweets containing hashtags and @ symbols. Theoretically, the two clients handle multi-mention replies with almost equal efficiency. Practically, Twitter's less intrusive solution gives it the upper hand.

{% include figure.html file="replying-all.jpg" alt="Replying all" caption="Replying a tweet with multiple @ mentions." %}

### Round 3: User Actions & Lists

Now for the less frequent tasks:

| Task | Tweetbot | Twitter
|-|:-:|:-:|
| Follow / Unfollow | 3.5 | 5 |
| Report a user |5 | 8 |
| Translate a tweet | 4.5 | 5 |
| Favorite a tweet | 2.5 | 3 |
| Delete a tweet | 3.5 | 4 |
| Switch time-lines | 2.5 | 3 |

**Outcome:** Tweetbot wins.

The official client didn't stand a chance here; Tweetbot's long tap is a godsend.

{% include figure.html file="following.jpg" alt="Following" caption="Following a user." %}

### Results

| Task | Tweetbot | Twitter
|-|:-:|:-:|
| Total | 71 | 68 |

The relatively awkward, albeit native, method of keying hashtags and @ mentions in Tweetbot skews the results in favor of Twitter for iPhone. If it wasn't for this detail, the third party client would have come out ahead.

That being said, it would be short-sighted to declare a winner based on the total score alone. In order to gauge the relevance of these tests, we need to take a closer look at the way we use Twitter in reality. [Studies] suggest that a big majority of users on the social platform are silent; unless you are a news agency, a celebrity, or a spam bot, you are more likely to be reading tweets than tweeting or sending DM's. As a result, the overall experience is deeply affected by our passive use, a point that the tests above completely eschewed in favor of purely active use scenarios.

{% include figure.html file="notifications.jpg" alt="Notifications" caption="In-app notifications in Tweetbot." %}

Notably, Tweetbot shines in some areas that would be hard to assess using the HIP model above. Save for the occasional tweet, reply, or DM, we spend most of the time on Twitter wading through hundreds of tweets and swapping accounts and lists. Few Twitter clients address these areas as elegantly as Tweetbot does:

* The number of new tweets (since the last refresh) is displayed in a unobtrusive blue bar in the time-line. This may seem gimmicky at first, but it turns out to be a huge time saver for time-line completionists.

* Single swiping a tweet displays related tweets in a dedicated conversation view, even if the user is not taking part in them. There seems to be no way to do that in the official client.

* Even though the visual style may not appeal to everyone, it provides a good balance of contrast between content and controls.

For a 1.0 release, Tweetbot is doing a remarkable job, especially when considering the saturated and volatile market of Twitter third party clients. Even though there is still room for improvement in certain areas, Tweetbot for iPhone has got what it takes to dethrone the official client, and then some.

[HIP]: http://en.wikipedia.org/wiki/Human*information*processor*model
[studies]: http://labs.yahoo.com/publication/who-says-what-to-whom-on-twitter/
[tweetbot]: http://tapbots.com/software/tweetbot/

*[DM]: Direct Message
*[GOMS]: Goals, Operators, Methods, and Selection rules
*[HIP]: Human Information Processing
*[MMT]: Multi-Mention Tweet
*[MOP]: Multi-Option Prompt