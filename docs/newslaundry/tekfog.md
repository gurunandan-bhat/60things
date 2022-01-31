# Lifting the Fog over Tek

[The Wire](https://thewire.in/) recently published an exhaustive
three-part[^1] investigation on the use of technology, called
*TekFog*, by a political party to:

> ...artificially inflate the popularity of the party, harass its
> critics and manipulate public perceptions at scale across major social
> media platforms

While this investigation has, as usually happens these days, brought
forth a polarized public response, many responders on both sides of
the spectrum have, privately and publicly, admitted that the details
and sub-plots of the investigation required a familiarity with
technology, beyond what is usually afforded to the lay. There has been
one [brave
effort](https://www.samarthbansal.com/the-wires-tek-fog-investigation-futile-search-for-evidence/)
at looking the investigation in the eye by [Samarth
Bansal](https://www.samarthbansal.com/), a formally trained
technologist turned data journalist. While his review is certainly
more accessible than The Wire's original set, its main premise (in my
opinion) is that the investigation and its conclusions have fallen
short of standards of due diligence and journalistic
exactitude. Sadly, why and where exactly have standards slipped,
according to Samarth, also requires a familiarity with technology. 

The purpose of this article is, then, to lift the fog as it were by
making the technology behind both views more accessible. The purpose
is not to support one view or the other, but to merely provide a
technology context for both views in the form of questions and answers
and hope that the questions answered here reflect those that you, the
reader, might have.

[^1]: [Part 1](https://thewire.in/tekfog/en/1.html), [Part
    2](https://thewire.in/tekfog/en/2.html) and [Part
    3](https://thewire.in/tekfog/en/3.html).


**Social media has been used for artificially inflating popularity,
harassing and manipulating perceptions ever since it was deployed. So
what is new about TekFog?**

You are right! The use of Social Media (Twitter, YouTube, Instagram,
Facebook and WhatsApp Group Chats and their clones) for dubious and
nefarious ends has been widespread ever since these platforms have
becaame popular. Obama in 2008 and 2012 and Trump 2016 (or people
acting on his behalf for their own ends) would count their Social
Media "campaigns" as critical to their victory. What distiniguishes
TekFog, according to *The Wire* investigators is their term "*... at
scale ...*". It is conceivable that a commercial enterprise or a
political organization hires 500,000 young unemployed keyboard
monkeys, each armed with 500,000 individual social media accounts to
spew whatever message pushes their product or their agenda. Of course,
someone would need to craft that message and its timing, but that
could be tasked to a very small group of communication experts. On the
other hand, if you hire 50 keyboard monkeys to send out targetted
messages from 500,000 fake accounts, then you are talking
"*scale*". And to operate at that scale you need technology that will
front 500,000 fake people, using just 50 real people. It is the
investigator's claim that TekFog is such a technology.
   
**The articles often refer to "trend" - What exactly is a trend?**

It is all about grabbing your attention. Social media platforms carry
a humungous morass of messages. By a rough estimate, in 2020, it was
estimated that 6,000 tweets were sent out every second - roughly 500
million tweets every day. By a similar estimate 400 million photos are
uploaded everyday on Facebook (requires attribution). Even if you
"follow" a small number of people, the number of messages, counting
likes, shares and re-tweets in your "feed" would be huge. Given that,
each of these platforms have to choose what to show you first - not
unlike the "ranking" of Google's search results. Each of these
platforms use their own algorithm to decide which message floats on
top of your feed. The "subjects" (derived from hashtags, photo
captions, story titles, poster's bio etc.) of the top tweets and
stories is essentially an indicator of "... what people are talking
about ...". Subjects that float to the top of this mess is loosely
referred to as tending subjects.
   
**Is it possible to artifically cause a subject to trend?**

It is generally believed that around two years ago, the (half)-life of
a tweet is between 18-24 minutes (requires attribution). If a tweet
about a subject does not get traction in that time, newer posts with
new trends will quickly bury the older message at the bottom of your
feed losing visibility and importance.  It is believed that you can
artificially influence the ranking algorithms of these platforms by
pushing a huge number of tweets or strories on a single subject in a
short interval of time from a large number of fake accounts.  And
critically, to weight it these posts correctly, these fake accounts
have to re-tweet each others messages to manipulate and influence the
subject. It is The Wire's contention (among others) that automating
this at scale is the goal of the TekFog technology tool set.
  
**If this were true how could it all work? Or in other words - What the
hell is an API?**

As explained above, operating 500 fake accounts with 500 keyboard
monkeys is easy and sadly, not uncommon in the PR world. To operate
500,000 fake accounts with just 500 people requires technology. And
that brings us to thing technologists call an API (Application
Programming Interface). When real people use (in other words, speak
to) Social Media and post their messages, photographs and videos, they
use a *User Interface* (UI) that requires them to type, upload, click
or tap a *form*. Obviously, this takes time and for even a well
trained keyboard monkey, posting into a thousand fake accounts
operated by him, would take him well past the 24 minute limit and thus
cause his message to loose traction. Almost all Social Media platforms
make it possible for *computer programs* rather than humans to
"fill-in" the equivalent information (your text, your images etc.) in
a *virtual form* and "submit" it to the platform. This set of *virtual
forms* that programs can use to add posts to platforms is called an
API. So just as humans use a UI (User Interface) to interact with a
program, a compter program can use an API (Application Program
Interface) to talk to other programs at extremely high speeds. Each
platform has their own version of the API and if tomorrow, a new
platform becomes available (or an existing platform changes its
virtual interface: its API), the posting platform would have to be
(re-)written to use the new API. A single human can conceivably feed a
single message and a list of fake accounts to a program which could
then, conceivably, assume the identity of each fake account in turn
and post the supplied message. If you can write such a program, then
you have *scale*. It is The Wire's contention that a part of the
TekFog toolset does this.
  
**If an API is liable to be misused, why do Social Media platforms make
it available? Or how do these APIs prevent misinformation from
spreading?** 

Its all about the platform's ability to increase the *engagement*
between producers of messages (ordinary people, but also product and
brand owners and their PR and Advertsing agencies, groups with an
agenda etc.) and consumers (other people). And an API like this opens
up a secondary market for products that use it for Bulk
communication. It is not disimilar to the ability to add a CC-list to
an email for bulk delivery (remember SPAM?). In a way, the platform is
saying, "Here is a shotgun for you to reach more people quickly and
increase engagement, but please don't use it in crowded places". Also
they claim that, like a safety lock on a shotgun, they have controls
that will make the use of bulk fake messaging difficult. Different
platforms provide different levels of control and they range from
reasonably strict to laughably ineffective. These range from Captchas,
One-time passwords, throttles etc. But most good programmers know how
to get around this. And both the providers and users of a platform's
API usually go "Wink! Wink!!" between them. It is The Wire's
contention that TekFog routinely bypasses controls (Captchas, OTPs
etc.) on a platform's API.

**OK. So I need something that will allow a small group of people to
send out a massive number of messages from fake accounts promoting up
each other's messages in a short time to be able to come up on top and
therefore grab a readers attention. Is this all there is to it? What
else is required?** 

While there are many public and underground tools to do this, the
critical component that distinguishes an ordinary tool from a truly
effective (but nefarious) one is the audience profiling that each one
uses. There is clearly no point in sending a message to someone or a
group who will ignore it. So to get traction, you need to match the
spirit of the message with the profile of the person or group. Since
you expose your biases (your profile) every time you browse, visit and
engage with Twitter, or Facebook, these platforms have a very good
idea about your likes, dislikes and preferences. And there are several
ways in which these platforms can reveal these profiles (money and
payment is an obvious path). Fake Games are another (this was how
Cambridge Analytica created a database of profiles of persons and
groups). So matching a message to a profiled recipient can amplify
your message.
   
**What evidence does The Wire provide to back their conclusions?**

Several, spread over all three parts and of varying depth and
detail. Here is a list I made of specific technology related evidences
(there are others, but those dont concern us since they are
understandable by the lay person). 

1. Screenshots of the TekFog toolset/application showing purpotedly,
   menu items of functionality that the set was capable of.
2. Screenshot of the TekFog toolset/application showing a task in
   progress. of artificially pushing a particular hashtag (subject) to
   trend. The application screen shows that this subject is being
   pushed through a little over one thousand accounts. The
   investigators then use a publicly available tool to ascertain
   whether that hashtag received a bump, and to obtain the number of
   accounts involved in pushing that hashtag. The bump and the number
   of user accounts pushing the hashtag matches with the numbers shown
   in the application screenshot. However the investigators leave out
   two interesting indicators (one admittedly) - First we dont know
   whether that topic did actually trend (meaning the hashtag appeared
   as a trending one in the twitter application) and second whether
   the one thousand accounts belonged to real political party workers
   who had turned over their credentials to the TekFog administrators
   to tweet from or these were fake accounts with imagined names that
   the TekFog had created using the TekFog platform. Tweeting from
   party worker accounts is deplorable too but not uncommon. Tweeting
   from bulk fake accounts is downright nefarious and almost certainly
   violates Twitter's terms of service and opens them up to
   prosecution. But we have no hint of what happened here.
3. Screenshot that indicates that TekFog includes a highly
   stratified/profiled database of individuals (possibly journalists
   and other "influencers"). We are shown how detailed the profile
   grid is (gender, age group, location, profession and political
   inclination) is, but not the database entries
   themselves. Interestingly, the investigators then analyze replies
   to tweets of 280 female journalists spread over a period of 6
   months and parse the messages for words of abuse listed on the
   TekFog application. And they find that 18% of these abusive
   messages were sent from "...*accounts linked to TekFog*...". It
   would be interesting to know how the investigators identified an
   account as managed by TekFog. They do not share that detail. What
   is scary though and significantly more so is this: That 88% of
   abusive replies with demeaning and disgusting words came from real
   people? 
   
   **In progress**

