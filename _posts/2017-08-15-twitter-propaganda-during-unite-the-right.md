---
layout: post
title: "Twitter propaganda during 'Unite the Right'"
modified: 2017-08-15 18:56:55 -0000
image:
  feature: sheep.jpg
  teaser: sheep-teaser.jpg
  credit: photographername
  creditlink: linktosource
share: true
categories: [data science, propagandalytics]
short_description: "This isn't just disinformation. It's also censorship. And it's terrorism. It's time to fight back."
---

As more and more people take to Twitter to keep up on fast-developing events, it's more important than ever important to understand how their platform facilitates the spread of misinformation, disinformation, and hate, as well as up-to-the-minute accounts of fact. While news and live video content was indeed shared widely and rapidly on Twitter during this weekend's #unitetheright rally, high-volume accounts highjacked the trending hashtags to push a pro-white-nationalist agenda and share disparaging disinformation about antifa, Black Lives Matter, other activists, and the mainstream media, with the intent (and effect) of flooding out the good information with propaganda.

## Background

High-volume Twitter accounts ― such as bots ― play <a href="https://medium.com/data-for-democracy/spot-a-bot-identifying-automation-and-disinformation-on-social-media-2966ad93a203" target="blank_">a significant role in the spread of disinformation online</a>. We have seen the same pattern in a number of disinformation campaigns: *catalyst* accounts seed a kernel of disinformation, and a large network of *signal boosters* amplify the signal, in the hopes that it will reach a wide audience that spills over into mainstream consciousness.

This was certainly the case in the <a href="https://medium.com/data-for-democracy/democracy-hacked-a46c04d9e6d1" target="blank_">lead-up to the French presidential election</a> this spring, and <a href="https://medium.com/data-for-democracy" target="blank_">my Data for Democracy colleagues and I</a> have found Twitter bots, sockpuppets, and other high-volume accounts played a significant role in a number of (mostly far-right) disinformation campaigns in the past couple years.

But this weekend's #unitetheright protests and terrorist attack presented a new problem. **Misinformation thrives during terror attacks and other breaking stories.** Many witnesses are sharing their perspective from their own up-close, but limited, vantage point; others are trying to spin (and omit) details into a narrative that favors their preconceived ideology; and no one ― not even the most seasoned journalists ― has the time to fact-check every claim at the pace of media consumption.

Given how easy it is for incorrect and incomplete information to spread, breaking stories like Friday's rally and Saturday's terror attack seem like the ideal environment in which to seed disinformation, misinformation, and heavily biased narratives. But it's not simple to manage such a campaign when the story develops rapidly, and the usual catalysts (and even many of the bot/sockpuppet operators) are *physically present at the event*. While bots and sockpuppets are at work during events like #unitetheright, their role is different than in traditional disinformation campaigns, and it's not always obvious from looking at an account which side they are on.

## The tweets

I collected just under 700,000 tweets from 6:24 UTC (2:24am Charlottesville local time) on Saturday, August 12, to 22:29 UTC (6:29pm Charlottesville local time) on Sunday, August 13. As far as I could tell, this collection included the vast majority of (if not all of) the public tweets from that time period containing the hashtag #unitetheright.
The bulk of these tweets were posted in the immediate aftermath of the car crash that killed one civil rights activist and injured at least 19 other individuals.

<i>(For all images, click to view full-size.)</i>

<a href="/assets/images/frequency_all.png" target="blank_"><img src="/assets/images/frequency_all.png" alt="#unitetheright tweets per hour" /></a>

However, as is typically the case in a dataset like this, the majority of the tweets are generated by a much smaller minority of high-volume accounts. The top 10% of accounts by tweet volume account for approximately 50% of the tweets, and the top 5% of accounts generated approximately 37% of the tweets. To figure out how a "typical" user tweeted, I divided the corpus in two according to a number of different thresholds and compared. Here are the lowest-volume accounts (10 tweets or less using the #unitetheright hashtag ― the 78% of the users in the dataset who produced roughly 31% of the tweets):

<a href="/assets/images/frequency_10_tweets_less.png" target="blank_"><img src="/assets/images/frequency_10_tweets_less.png" alt="#unitetheright tweets per hour, accounts with 10 or less tweets" /></a>

The spike immediately following the car crash and the subsequent drop off in tweet volume are far sharper for these accounts. And as we raise the threshold, the drop off becomes less precipitous. Here are the accounts with 20 #unitetheright tweets or less (92% of users, 54% of tweets):

<a href="/assets/images/frequency_20_tweets_less.png" target="blank_"><img src="/assets/images/frequency_20_tweets_less.png" alt="#unitetheright tweets per hour, accounts with 20 or less tweets" /></a>

And 50 tweets or less (98% of users, 76% of tweets):

<a href="/assets/images/frequency_50_tweets_less.png" target="blank_"><img src="/assets/images/frequency_50_tweets_less.png" alt="#unitetheright tweets per hour, accounts with 50 or less tweets" /></a>

And 100 tweets or less (99% of users, 88% of tweets):

<a href="/assets/images/frequency_100_tweets_less.png" target="blank_"><img src="/assets/images/frequency_100_tweets_less.png" alt="#unitetheright tweets per hour, accounts with 100 or less tweets" /></a>

Compare these to the top tweeters. Here are the accounts with 100 #unitetheright tweets or more (0.6% of users, 12% of tweets):

<a href="/assets/images/frequency_100_tweets_more.png" target="blank_"><img src="/assets/images/frequency_100_tweets_more.png" alt="#unitetheright tweets per hour, accounts with 100 or more tweets" /></a>

And accounts with 2oo tweets or more (up to 681 tweets for the highest-volume account: 0.1% of users, 5% of tweets):

<a href="/assets/images/frequency_200_tweets_more.png" target="blank_"><img src="/assets/images/frequency_200_tweets_more.png" alt="#unitetheright tweets per hour, accounts with 200 or more tweets" /></a>

It's clear from this sequence of plots that the highest-volume accounts tweeted on a very different schedule. Most users dropped off in their tweeting with the #unitetheright hashtag after the car crash (though many of them kept tweeting *about* Charlottesville, but without that hashtag). But most high-volume accounts *kept tweeting with the hashtag for several hours after the crash*. I don't know exactly why, and from spot-checking the tweets, it's hard to find a single narrative emerging. But I have seen situations before where after a hashtag begins to trend, the disinformation bot-nets and sock-nets latch onto it in order to keep it trending long enough for their narrative to spill over into more mainstream channels. It's hard to know for sure, but that seems to be at least part of what is going on here.

## The information landscape

In an age of information glut, there's no shortage of sources for news and opinion content, and it's not surprising to see that people on the political right and left get much of their information <a href="http://pushpullfork.com/2017/03/fake-news-adtech-misinformation/" target="blank_">from different places</a>. In disinformation campaigns, we've also seen differences in the kinds of information sources being pushed by the high-volume accounts when compared with "regular" users, and this has <a href="http://pushpullfork.com/2017/05/macronleaks-timeline/" target="blank_">an impact on the sources being cited in the mainstream</a>. #unitetheright is no exception.
I extracted all of the web pages linked from #unitetheright tweets and compared high-volume accounts to low-volume accounts. (It's difficult to parse left-leaning and right-leaning accounts without a pre-made list, especially when they are collected because of a single shared hashtag.) To start, here are the websites (domains and subdomains) shared most frequently by #unitetheright tweets overall:

<a href="/assets/images/domains.png" target="blank_"><img src="/assets/images/domains.png" alt="Top domains shared on #unitetheright" /></a>

The emphasis on video content is striking, if not surprising. The most tweeted domain is Periscope (livestreamed video), followed by YouTube. @RVAwonk's account of the weekend's events accounted for almost all of the Medium links (third place), followed by a number of other partisan or extremist sites and social media platforms, with a few URL shorteners thrown in. Interestingly, mainstream news media is nowhere to be seen on this list at all. (Huffington Post is the closest to mainstream news on the list.) The lack of expert, edited journalism on this list should be a caution to all of us when we participate in the mass quick-fire retweeting of updates during a breaking event.
But not all of these sites were equally distributed among #unitetheright tweeters. Using a simple statistical measure called odds ratio, we can find the *most distinctive* domains shared by high-volume and low-volume accounts. (I used a threshold of 10 or more tweets for high-volume accounts, separating the tweets into the 25% most active accounts and their 72% of the tweets, and the 75% least active accounts and their 28% of the total tweet count.)

<a href="/assets/images/domains_logodds_with_retweets.png" target="blank_"><img src="/assets/images/domains_logodds_with_retweets.png" alt="Most distinctive domains shared on #unitetheright by low- and high-volume accounts" /></a>

Here we do see a few mainstream news media sites (among the low-volume accounts), but also many more extremist sites among those most characteristic of the high-volume accounts: not only Breitbart and InfoWars, but also 4chan and Order15. So like we've seen in studies of disinformation campaigns, **the highest-volume accounts are disproportionately pushing sites known for spreading disinformation, misinformation, and propaganda.**
However, some of the "most distinctive" sites are not particularly widely shared overall. So here is a two-dimensional map of the 50 most shared sites, according to how distinctive they are of high- or low-volume accounts. (Domains to the bottom right are more distinctive of low-volume, "regular" users, while domains to the upper left are more distinctive of high-volume accounts. Domains near the dashed line are shared with similar frequency by low- and high-volume accounts.

<a href="/assets/images/domains_2d_with_retweets.png" target="blank_"><img src="/assets/images/domains_2d_with_retweets.png" alt="Most distinctive domains shared on #unitetheright by low- and high-volume accounts" /></a>

It's interesting to see here how the typical perception of these sites' politics maps almost perfectly onto the high-/low-volume account distinction. Of the mainstream news sites, the New York Times is most distinctive of low-volume (left-leaning?), Fox News of high-volume (right-leaning?), and Washington Post near the center. Left-leaning Think Progress also sits on the low-volume side, while far-right extremist sites like Order 15, White Genocide Project, and Daily Stormer can be found on the high-volume side. There are anomalies, of course ― never mind the fact that partisans tweet links to their opponents while disparaging or critiquing them. However, in this context, it makes perfect sense that **the high-volume accounts are generally pushing the narrative of the alt-right, white nationalist agenda of the #unitetheright organizers.**

## The content of the tweets

Applying the same analysis to the text of the #unitetheright tweets, we can see the same kinds of patterns emerge. Here are the bigrams (two-word phrases) most distinctive of high- and low-volume accounts, as well as a two-dimensional map of the 50 most common bigrams.

<a href="/assets/images/bigrams_logodds_10.png" target="blank_"><img src="/assets/images/bigrams_logodds_10.png" alt="Most distinctive bigrams shared on #unitetheright by low- and high-volume accounts" /></a>

<a href="/assets/images/bigrams_2d_no_rt.png" target="blank_"><img src="/assets/images/bigrams_2d_no_rt.png" alt="Most distinctive bigrams shared on #unitetheright by low- and high-volume accounts" /></a>

The phrases most distinctive of high-volume accounts are those talking about the identity of the attacker, and those pushing a narrative that sees the media, the antifa (anti-fascist) movement, and Black Lives Matter as the enemies. The phrases appearing in similar proportion across all accounts are those that describe the details of the incident ("car attack", "counter protest", "Richard Spencer", etc.). And the phrases most distinctive of low-volume accounts are those that describe (usually in less than flattering terms) the far-right marchers: "white supremacist", "white nationalist", "neo nazis", and (poking fun at the very non-white-American choice of light source on Friday night) "tiki torches".
It's heartening to see that the bulk of Twitter users are in opposition to the white nationalist extremists who marched on Saturday, one of whom killed an activist. But you wouldn't know that from looking at the tweets overall. Three-fourths of the *users* are in the low-volume, largely anti-white-nationalist category here, but roughly three-fourths of the *tweets* are in the high-volume, largely pro-white-nationalist category. And while Twitter does make meager attempts to keep botnets from gaming their "trending" algorithm, it was impossible to follow the weekend's events without being flooded with pro-white-nationalist content, on both the hashtags and Twitter Moments.
As my colleagues and I have written before, these disinformation campaigns are attempts to control the mainstream narrative. In this case, the high-volume, pro-white-nationalist accounts made the movement seem larger and louder than they really are, and that in turn emboldens isolated extremists to speak out and to act out. Further, when the voices of a movement of *violence* is amplified *during and immediately following an act of terror*, that messaging in itself is terrorism. And Twitter's platform makes that terrorism both more possible and more effective than it might otherwise be.

## Takeaways

It turns out that while things look very different than in the #macronleaks campaign, high-volume accounts played an important part in the spread of (mis/dis)information during and after the #unitetheright rally. The high-volume accounts using the #unitetheright hashtag tended to share far-right propaganda more than the low-volume accounts, and the high-volume accounts maintained peak activity far longer after the terrorist attack than average accounts. In general, these high-volume accounts did not serve as signal boosters for specific catalysts like we've seen in the past. Instead, they capitalized on the media attention brought by the terror attack and used it to push several standard far-right propaganda narratives. While few of these narratives made it into the mainstream news media, they were echoed by Donald Trump's initial response to the events in Charlottesville, and any Twitter user who clicked on the #unitetheright trending moment would have seen a significant number of tweets pushing that narrative mixed in with actual news and eyewitness reporting.

In her recent book <a href="https://www.twitterandteargas.org/" target="blank_"><i>Twitter and Tear Gas</i></a>, Zeynep Tufekci redefines censorship for the digital age. Censorship is no longer a silencing of a voice by force, but a flooding of the information landscape with so much disinformation that the truth is covered. It seems that the extremists of #unitetheright are not only trying to push a false narrative about the media and identity groups other than young, white, straight men, but they are also trying to flood our news feeds with so much filth that the truth becomes harder to find ― and so stained by the filth around it that we don't believe it when we do find it.

This isn't just disinformation. It's also censorship. And it's terrorism.
It's time <a href="http://www.digitalpedagogylab.com/hybridped/truthy-lies-surreal-truths/" target="blank_">to fight back</a>.

<i>Note: the Twitter scrape and analysis were conducted with an extension of my <a href="https://github.com/kshaffer/tweetmineR" target="blank_">tweetmineR</a> utility for Python and R.</i>

<i>Featured image by <a href="https://www.flickr.com/photos/ginz/6816885427/" target="blank_">Gwendolen Tee</a>.</i>
