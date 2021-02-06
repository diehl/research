---
title: Social Signaling and Language Use
date: 2010-04-29T12:12:43-07:00
tags: [Social Signaling, Social Relationship Identification]
---
Consider the following email from Tim Belden to John Lavorato and Louise Kitchen. Recall that Tim Belden was indicted for his role in conceiving and executing various financial schemes that allowed Enron to profit significantly from energy markets. Through the analysis of the Enron email collection, we would like to understand who Belden was reporting to and who he was supervising during the time period of the California energy crisis.

> _Date: August 2, 2001_
>
> _From: Tim Belden_
>
> _To: John Lavorato, Louise Kitchen_
>
> _Subject: Off-Site Travel Question_
>
> _The e-mail that was sent out many weeks ago about the off-site indicated that it would run from Wednesday night to Saturday AM. It is now running Thursday until Sunday. Calger has found a leased plane that costs roughly \$13k for one roundtrip and a total of $20k for two round trips. I had already made arraingements to attend a wedding in Oregon on Saturday night. It is a good friend of mine and my wife's. It's in eastern Oregon and is about a four hour drive away. I see the following choices before me:_
>
> 1.  _Don't go to Colorado. Tell you guys that I'm a family man and not a company man._
> 2.  _Go to Colorado and fly home commercial on Friday night, leaving at about 4 PM. Incremental cost of flight would be $500._
> 3.  _Go to Colorado and fly home on the rented plane on early Saturday afternoon. Incremental cost of flight would be $7,000._
> 4.  _Don't go to wedding. Tell my wife that I'm a company man and that it is critical that I ride mountain bikes with a bunch of 30-something Enron folks all weekend._
>
> _<span style="color: #000000;">While I have authority to place millions of dollars of the company's money at risk, I don't feel comfortable signing up for a $7,000 extra flight without talking to you guys.</span> #3, the jet set answer costs quite a bit more, but it dramatically increases the amount of time that I spend in Colorado. #2 is cost-effective but gives me less than 24 hours in Colorado. #4, while perhaps appealing to you, doesn't work for me. #2 is probably preferable to #1, just requires a lot of travel time to me._
>
> _Any thoughts would be greatly appreciated._

This email was one of the top ranked messages identified by our prototype system SocialRank as evidence in support of the rank scores for both Lavorato and Kitchen. Lavorato and Kitchen were identified as the top two most likely candidates to be Belden's superior. In fact, Belden routinely reported to both of them.

This message provides the type of evidence we seek to confirm the existence of a manager-subordinate relationship. Examples such as this nominated by SocialRank make clear the difficulty of composing explicit search queries to identify such evidence. Yet once such examples are revealed, we have no difficulty in recognizing the social relationship of interest.

A natural question at this point is: what features of the message are compelling to the machine? Each message was characterized simply by a vector of word unigram frequencies. No stop words were removed from the text. Here is the message content once again with significant terms highlighted.

> _The e-mail that was sent out many weeks ago about the off-site indicated that it would run from Wednesday night **<span style="color: #c00000;">to</span>** Saturday AM. It is now running Thursday until Sunday. Calger has found a leased plane that costs roughly \$13k for one roundtrip and a total of $20k for two round trips. I had already made arraingements **<span style="color: #c00000;">to</span>** attend a wedding in Oregon **<span style="color: #c00000;">on</span>** Saturday night. It is a good friend of mine and **<span style="color: #c00000;">my</span>** wife's. It's in eastern Oregon and is about a four hour drive away. I see the following choices before me:_
>
> 1.  _Don't go **<span style="color: #c00000;">to</span>** Colorado. Tell you guys that I'm a family man and not a company man._
> 2.  _Go **<span style="color: #c00000;">to</span>** Colorado and fly home commercial **<span style="color: #c00000;">on</span>** Friday night, leaving at about 4 PM. Incremental cost of flight would **<span style="color: #c00000;">be</span>** $500\._
> 3.  _Go **<span style="color: #c00000;">to</span>** Colorado and fly home **<span style="color: #c00000;">on</span>** the rented plane **<span style="color: #c00000;">on</span>** early Saturday afternoon. Incremental cost of flight would **<span style="color: #c00000;">be</span>** $7,000\._
> 4.  _Don't go **<span style="color: #c00000;">to</span>** wedding. Tell **<span style="color: #c00000;">my</span>** wife that I'm a company man and that it is critical that I ride mountain bikes with a bunch of 30-something Enron folks all weekend._
>
> _While I have authority **<span style="color: #c00000;">to</span>** place millions of dollars of the company's money at risk, I don't feel comfortable signing up for a $7,000 extra flight without talking **<span style="color: #c00000;">to</span>** you guys. #3, the jet set answer costs quite a bit more, but it dramatically increases the amount of time that I spend in Colorado. #2 is cost-effective but gives me less than 24 hours in Colorado. #4, while perhaps appealing **<span style="color: #c00000;">to</span>** you, doesn't work for me. #2 is probably preferable **<span style="color: #c00000;">to</span>** #1, just requires a lot of travel time **<span style="color: #c00000;">to</span>** me._
>
> _Any thoughts would **<span style="color: #c00000;">be</span>** greatly appreciated._

Surprisingly enough, the terms that matter in this message are function words (stop words), not content words. If one examines the weights in the linear ranker used by SocialRank, it becomes clear that function words make up a significant fraction of the most discriminative terms. For anyone coming from an information retrieval background, this feels unnatural. For IR tasks, we are accustomed to first removing function words from text prior to performing any processing because function words are seen as terms that carry little information. For social relationship identification tasks, this is precisely the wrong intuition.

Some time after discovering this result, I had the opportunity to meet [Kate Niederhoffer](http://socialabacus.blogspot.com/), a social psychologist who has studied social signaling in language extensively. I explained to Kate what we had learned from the Enron email data in the context of manager-subordinate relationship identification. She was not surprised at all. In the social psychology literature, there are a number of studies of function word use in different social contexts. It is well understood that function words play a significant role in social signaling. Kate's graduate work along with that of her colleagues from [Jamie Pennebaker's group at UT-Austin](https://www.words.live) provides a rich body of work to garner more perspective on the issue. Two review papers I would highlight are [here](AnnualReview.pdf) and [here](Chung&JWP.pdf).

As my colleagues at JHU/APL and I have [argued](SocialCom09-Final.pdf), we must take a fresh look at a number of issues when thinking about building systems that support social query tasks such as social relationship identification. The example above points out one issue regarding features to support machine learning. There are many others to consider. This space will definitely keep us busy for some time to come with intriguing challenges and fascinating questions!
