# Chris Walker Weekly episode 4, Optimizing CRM Data Architecture

**Author:** Chris Walker
**Video URL:** https://www.youtube.com/watch?v=wR20w3DGEjQ
**Date Published:** 28 February 2024
**Duration:** 54:40

companies over and over reinvent the wheel in bi and they make a lot of mistakes along the way and that they're
rarely if ever up to a best practice of how you're supposed to look at the data so I think that overtime um first we need to have the
foundational pipeline architecture I.E a custom object that looks across the entire customer life cycle that's
collecting all that data then we have purpose-built analytics that are then pulling out the data exactly what we
need exactly how we're expecting it and then manipulating it in the stand standardized way and then delivering
that back to the customer with other parts of value like Ben realtime benchmarks Market updates based on all
the whole database that exists etc etc um I think that that's where the market
will [Music]
go what is up everyone welcome back good to have you here got to see some new
faces give everyone a second to uh to join in here you also notice I got a laptop here we're going to try something
new with a couple visuals and Screen shares I'm trying to illustrate a couple of Core Concepts that I've been thinking
about um so what I want to do is I was Rel listening to the podcast episode that just got released today um a
podcast that I did with Chrissy and Charlie Saunders who are the co-founders of CS2 marketing a marketing Ops and rev
Ops consultancy and I've been advising them we made that partnership more formal just uh just recently um and I
think what they're doing is highly interesting and highly complimentary to a lot of the things that we discuss on
this podcast so for those of you that haven't feel free to reference that episode it's a little bit technical but
it's very focused on having the right architecture the underlying Foundation
inside of your CRM data so that all of the systems that then have to then use that data like when you're doing
pipeline modeling um conversion rate type of optimization not just in marketing but all the way through the
sales funnel um there's a lot of different applications of why why it's very useful and so I'm going to go through it in a more practical sort of
way with a couple of visuals to talk through it um before we go there I've uh
I've noticed that many marketing leaders almost every marketing leader is doing this thing that they refer to as
pipeline modeling where they have an Excel or Google spreadsheet and they're putting in like manually every week or
every month they're pulling data from Salesforce and then they're putting this in this in Excel sheet to try and track
the cost per opportunity to try and cohort conversion rates by having like
mql volume and meeting volume and opportunity volume um and then trying to use that to then forecast out and make
bets and say okay like how do we increase pipeline or Revenue by this much we can increase conversion rates we
can try and lower our cost per opportunity and they're doing a lot of the work in Excel so first off they
won't be needing to do it in Excel for that much longer because that's a core part of what we're building at poetto to
give go to market leaders one the right underlying data foundation and then tools to then analyze diagnose forecast
and model in the future which is we discussed it a lot on the podcast I encourage you to check it out pipeline
modeling and pipeline Diagnostics is entirely different than at multi-touch
attribution and they should be looked at as two independent things where you're using them for different purposes and so
reference that episode if you want so now I want to get into a little bit of the details here because a lot of people are asking and the clients that we that
we work with at petto are asking the same thing like okay we're down we want to solve this so like how do we think
about solving it and the reality is there's a lot of different ways to solve it some that have certain specific cons
some that cost a lot or you need tech to do it and then other ones uh so we'll go through some of those details right now
so this is a super super highle graph TR of basically the way that you look at
the customer life cycle all the way from has never heard of your company all the way to expanding them and having them be
your number one customer and promoter and things like that a couple of the core points that I want to make here
number one you have your entire total uh total addressable Market or what you have decided are your is your target
market at the top until a Target account and the people inside of those accounts
are showing intent and signals that account is not in Market to buy which the estimates now are somewhere between
95 and 99% of your Market are not in Market to buy at any specific time and
so in that instance the strategy for that set of accounts which is most of your Market is to create demand or try
to accelerate demand when I say accelerate demand I mean that company might buy from you in two and a half
years if you do nothing but if you're able to do things and market and educate them maybe they'll buy in 6 months or
maybe they'll buy in 9 months and therefore you're accelerating pulling in that market demand for your business and
accelerating growth the next part is the signals and so instead of looking at this as leads or mqls or something like
that we have all of these different available signals that are happening inside of our go to market they request
a buyer requests a demo intent data from an account Zoom info cold list pole
attended a webinar an event something like that and a critical part of this is
that in my view that's where pipeline starts pipeline starts at the signal
where your your account the account that you're going after is in Market or the people inside of those accounts are
showing some level of intent that could be tracked intent it could be hey I want
a demo it could be anonymous intent like they're on G2 and they G2 feeds you back the account that that uh is on that page
regardless that's where pipeline starts the problem is that companies aren't really tracking the part from signal all
the way to opportunity and they have not a very good data structure to track that part so then they just look at
Opportunity down and they miss a ton of these early signals about the quality of the pipeline and how to optimize the
overall system then you get into pipeline sources which is very well documented but basically you're breaking
it out and looking at distinct go to market motions and then the accounts and the tiers of accounts that are flowing
through those motions you have hero pipeline as a key ba uh a key metric to be able to normalize the definition of
pipeline across the pipeline sources so that you have a clear way to optimize and understand and then you have close
one and then expansion and upsell what I mentioned on the data side is that all this stuff that's happening pre-
opportunity creation is generally lost or very difficult to connect to what's actually happening and all that loss is
a ton of wasted time from tens to hundreds of sdrs a lot of marketing
dollars that are spent to create signals that don't drive Revenue um and a
variety of other like sort of unseen waste that's happening in the beginning of the process I want to talk through
and this is a little small U so hopefully people can consume it oh most uh B2B companies are tracking their data
like this what people are viewing as the fractured funnel approach where you have all these different objects that are
tracking parts of the process so you have a leader a contact at the top and then they become a campaign member when
they engage and then there's some type of like stamping for mql or sales ready
if you're that sophisticated and then you have Downstream activities and opportunities and then you actually have
your close one data and then trying to stitch all of that together with all these multiple objects creates tons of
different challenges to understand the conversion rates between stages the velocity that's happening the source and
where people actually came from all the marketing data all like looking down all
that stuff is then having to be stitched together in an Excel spread sheet and then the CMO is working on that Excel
spreadsheet and doing her manipulations and you have a marketing manager doing their own manipulations then you have the CFO doing their own stuff in bi and
all of a sudden everyone is looking at different data and everyone's tracking filtering doing everything differently
makes it really hard to get aligned as a company and make some bold strategic decisions the best practice is to use a
custom object that sits alongside all these different objects and pulls the data off of them into one object and you
can look all the way and basically the the tracking starts at the signal that
happens at the account or person and then all the way down you have the tracking it's copying data from the lead
and then the contact tracking sales activities tracking all the campaign data all the opportunity data all in one
place so that anyone in the company can then take that data and then go and be
able to visualize analyze and do anything with it and you have a clear path to understand conversion rate from
one to one and a ton of other benefits this is an example of all of the data
that should that theoretically should be tracked by a company every single time that there's a signal there is tons of
data on one object and the reality is that most companies across all their objects do not track anywhere near this
level of granularity to make decisions and so I'm just going to run through a couple of the examples of the core buckets for the listeners afterwards you
have all of the lead and contact data that's coming through you have what we what we call a
Tipping Point or some people call a Tipping Point I'm now referring to as the core signal and you have all of that
data you have engagement data that's coming from marketing like UTM and campaigns you would be amazed how many
companies can't track the outcomes of their Google ads campaigns when just putting it on an object and tracking the
signal all the way to revenue would solve the whole thing cost a couple thousand maybe $10,000 and it would be
solved meanwhile they spend 500,000 300,000 a million dollars a month on
Google ads and don't set up don't take the time and the small amount of investment to be able to just set this data up to track it appropriately you
have all the account data the account tier what segment they're in all that stuff so then future and Reporting you
can slice by segment and things like that and get clear conversion rates all the way from signal to
cash um you're stamping at all the progressions when the SDR reached out
when the meeting was held when it became qualified when it changed stages you're tracking all that stuff so you can then
look at the velocity between stages where people are dropping off figure out the clear places where you're not up to
Benchmark where there's an opportunity to optimize the process you have all the opportunity data the AR any other key
data that's actually on the opportunity record that then is getting pulled in as well who's owning it so who are the
people that are actually doing the work at the different stages that you can do process optimization you can do cohorts
you can look at high performers and low performers this is just just an example of all the data that you could be
collecting in one place and then be able to basically analyze and optimize everything and so as you look at this
you can clearly see that this what we're doing here in terms of having an architecture to be able to analyze
diagnose optimize and report on our pipeline is very different than trying to connect a channel like LinkedIn ads
or something like that to create a touch Point these are very different things they should be looked at not as
competitive that actually that you need to do you need to be able to do both but in my humble opinion the foundational
data to optimize your entire your marketing Investments how you capture intent sdrs the sales process has to be
a foundational part of your data set before we start looking at things like marketing mix modeling and
incrementality and all these other Advanced complex things which have some promise in the future and maybe have
some promise today but we can't lose sight of the fundamentals and the things that help us make make easy decisions
and when people look at this the the core difference is that fixing your Salesforce data like in this and having
a pipeline architecture is generally harder to implement and fix but once you
fix it it provides very easy to analyze data to make good decisions and
conversely attribution tools are easy to implement but then once you have the
data it's very very hard to analyze the data and make good decisions and so
that's the reason that I believe a lot of companies jump to an attribution software when really they need to fix their core CRM foundation and
infrastructure of data and then if you had all of this
data then you'd be able to run all of your go to market Motions like a machine
you would have all the data you'd have all the changes in the process you'd know where you're on or off track you could track every single thing it
fundamentally changes the kpi set and how you optimize and run your entire go go to market not just the marketing
department um and so I feel very strongly about helping companies see the
opportunity here helping them see the cons of what they're trying to do right now which is push data from the leader
contact onto the opportunity and then do cross object reporting and have campaign touch points and campaign members it's
just really difficult to have everyone looking at the same data when you have it all across all these different objects and filters so a little bit of a
stop a stop sharing I just kind of wanted to throw like throw that out there for people to consume maybe there's some questions on that we're
basically getting um questions from every single one of the customers that we work with about like hey we believe
in this how are we going to implement it um and so I shared some of the details about what the future looks like to try
and help illustrate to people the gap between what they're doing right now and the data they have available versus the
data that they could have available if they took the time and small amount of money to be able to solve these things
and so uh if we can get technical would love to S Sydney's is also working on this and is a great technical Ops
thinker and so we'll have uh multiple angles to answer any questions like that
and so with that said thanks you all for being here let's get into some questions question is if I look at this custom
object there's some sort of hidden relationships uh embedded in there so how do you deal in reporting and
tracking stuff across the funnel between contacts so you have multiple contacts on one account you have maybe multiple
opportunities on the same account how do you deal with those so when it comes to
actual like the humans that are doing the work it's the workflows are not changing for an SDR or how marketing
inputs their campaigns or how sales manages their process or their qualification or how they do a proposal
all the workflows remain the same there might be opportunities for business process optimization and you can capitalize on those if you choose but
the real the what's actually happening is the object is running on the background and just grabbing data from
all the existing objects and workflows once it's filled and when it's needed and then collecting it all in one place
throughout the journey that it it allows if a person comes through gets to a
meeting like reschedules the meeting and then drops out and then they come back six months later and they come back in
in a normal process all the original data gets overwritten and so it REM mqls a new mql date your historical data is
off and then they're back in with an object solution the object is what's actually tracking the journey not the
leader contact object so when somebody re-enters a new custom object record is created and then all the data for the
new journey is collected again um and so and then there's a you're you can use
this to look at both a person level journey and an account level Journey um
because you're taking the account data so then you could filter onto just things that are in tier a tier 2 account
you could look at it as in both an account or a person level view cool thanks great question have you uh
considered trying this or what are you doing right now yeah so uh one of the challenges we re run into is moving from
a lead or contact based motion towards an account based motion and one of the
big hurdles is to get all the to get reliable or decent decently reliable
data on account level and track that across the funnel so for instance starting with lead scoring or rating in
the beginning look at it at an account level rather than at a uh at a contact level totally contact might
be a low uh an intern reaching out from a hugely attractive company in our ICP
and then we'd still like to track and follow up and and treat them accordingly yeah and so what this gives you the
granularity to do is track the process of individual people in the accounts
while also having the way to look at the accounts overall because the reality is that when an account moves to like
Market or something like that it's very possible for the account to move backwards as well um and there's not a
lot of there's it's when companies do account tracking it's typically a linear process where it's difficult for them to
go backwards when in reality it happens all the time um and so I think this
gives the way to track the progression of people in accounts while also giving like the the roll up of the the overall
accounts or account tiers as well yeah yeah sounds cool wish I had that six months ago
we're working on a uh a in you know inexpensive solution that companies could implement it rather quickly so
we're hoping to have that live soon yeah one of the key ways to think about it is you're tracking you know unique
conversions unique starting points which we call signals um across leads and
contacts and accounts and you're going to have multiple in the accounts over periods of different times and you'd be
able to see that and correlate okay we had all these signals at this time which one of those signals resulted
in Opportunity Revenue expansion so forth so it's uh gives you a different
dimension to look at the data and you're not stuck in the lead to account like
mapping view hey Chris what's going on man Tori good to have you back interested to hear
your perspective on this I imagine you're doing some Excel modeling yourself so interested in your question then we
can a lot of this stuff manually and uh HubSpot in Salesforce and so um love
what uh what y'all are working on here really cool to to actually start to see it um you know in in demo form but um so
here's my question right like I guess what it kind of comes down to is uh how you're how you're interpreting and
analyzing like the the data that comes from all these different goto Market functions so for instance right like
with with inbound um it's easy for us to identify when somebody comes in the
length of the cycle between you know the time they came in Bound and raised their hand versus when they actually became a
closed one deal um but like one of the things I'm I'm working on with a client right now who uh is still getting a lot
of their pipeline from sea level relationships um in that instance it's
less clear when like the actual maybe we'll call it lead originated from uh
and so if I were to compare like a deal that came from a sea level intro um it
might look like the sales cycle is really short and you know if I compare that to inbound I'll say well it looks
like our our average deal size and our sales cycle is really short for the SE level intros and so that's where we should be placing more of our bets um so
like how how do you actually kind of interpret some of this data when looking at all the different go to market
motions alongside one another is this really like a comparison between all the different uh all the different sources
or um are you trying to kind of isolate them and look at all of them on their own yeah so one uh critical point that I
want to make here is that the this type of tool in automation is built for scale
um and so that's one key point if you are a artist that is like hand making a
table then may you may not need this but if you're running a manufacturing facility trying to make 10,000 tables a
day and do it effectively and make a margin then you're going to need some type of tool and analytics and so it's
really the difference between th th those two dichotomies um so that's the first point
is that it's really for scale um if you're less than a million AR would it be nice to have the foundation set up so
as you scale you have it 100% but the perceived value at that stage is lower
and then the other the other question was related to tracking like differences between hand raisers and maybe like
sales Outreach or other things like that when people are like marketing is used to tracking these things because they're
trying to they were trying to have like a first touch or they're trying to have last touch or they say they marketing influence so marketing's very used to
having this type of track track trackable data when it comes to a web form submission a third-party like lead
uh contact that came from a LinkedIn lead gen form or contents indication or review site form or something like that
um marketing is used to having those types of things the the thing to consider is when you open it up and look
at it in the entire go to market that basically anytime A salesperson takes action it should be driven by a signal
your ta your sales team should not just be aimlessly deciding what to do in some de that should all be architected in the
strategy and the technology and then you have all the data of okay signal action
you collect it over a long period of time then you have all these signals and you say okay let's just cut these signals out these signals we win one out
of a th000 leads or one out of 10,000 signals let's get rid of these and let's put these new ones in and let's track
the effectiveness of these new ones and basically like the reason that sales is
or sdrs are engaging all that expensive human capital that that that stuff has been prior prioritized and decided
already based on the strategy and the technology used um and so that's really how you're thinking about it in the
scale level if there's a person in a manufacturing facility working on it they know what they need to do every day
they have a very clear metric of what they're how many parts they're supposed to push through the line those types of
things and so having that level of granularity and prescription on what we're doing and why I think would be
really useful and then Downstream to that then you have all of the perfect analytics about how to make a decision
at a SDR leader a cro or even a marketing leader so it's a little bit different way of thinking than how
companies uh think right now and do you think that like um you know for some of your your clients that adopt the uh you
know your uh your new product here um do you expect that they would be analyzing
and and utilizing those insights on like a like a week to week basis like your typical Salesforce dashboard or is this
something that you you you know you would recommend that they look at in more of a zoomed out view like a monthly or even quarterly it'd be curious how
often are you updating the sheets that you're using um yeah I think kind of it depends on uh the volume of the client
um but uh yeah I mean I I try to stay on top of it like I'm in Salesforce daily
um and then updating kpi trackers maybe on a on a weekly basis and doing more of the analysis on like a a monthly and
quarterly basis yeah exactly most people I talk to are updating their spreadsheet somewhere between weekly and monthly
somewhere in that vicinity and then that'll help you understand how you're progressing to plan identify risks allow
you to update your future forward models and things like that and then having a quarterly view where we look at much
larger chunks of time and that you get out of the ups and downs that can happen in a month and you have more time that
that is the data that we recommend sort of analyzing in a different way and using it to make like big bigger
decisions I just don't think that big decisions should be made on daily or weekly or even monthly type of
data um and so it's just about knowing what frequency of of the data you're looking at and why you would use that
frequency so at lower frequencies it's really understanding hey are there like anything major it's almost like monitoring is there anything major going
wrong or right that I need to know about now but then we even if we knew it was
going right or wrong it's not necessarily that we would blow up our whole strategy and change something based on that one week of up or down
because you're likely to make a bad decision based on just looking at too short of a Time window um so I think the
I think the real answer is both just using the right time periods for the right purposes got it thanks all right
we've got another question from Tracy bring her on um my question was I I saw
some terminology in the architecture that I hadn't really seen from you before and it seems intuitive but I
wasn't sure about the distinction distinction between Tipping Point and non- Tipping Point Source data and
Milestones and how that um ties into the customer journey and triggers action
either inbound or outbound or like what insights you're gaining from those distinctions and how they're defined
yeah our terminology is evolving at one point we used conversions as the main term it's very confusing there's so many
different conversion actions in like a marketing or go to market engine so we've moved away from
conversion um Tipping Point was something that other people have used that seems to work the point where the
the the last thing that happens before someone becomes sales ready um but
lately we've been just looking at it as signals so it would just be the signal that happened that triggered sales to
have some type of action um and that would be the the terminology that's used
you're going to have it looking at the campaign or the visible data all that data is there it's just we're using
we're using that data in a different way um and so it's really having the distinction of like when you look the
signal that happens has a massive indicator of everything else that happens after that but most companies
don't track the signal well all the way to the end so they don't get the very easy easy to see and obvious insights
and changes that they could make if they had the data so does a Tipping Point uh trigger a sales action and a non-
Tipping Point not or is it not that black and white uh I would I just wouldn't look at it in that way anymore
I would just think about it as the the signal that's driving the action which could be viewed as a Tipping Point but I
just wouldn't look at the non- Tipping Point data yeah I should have updated the slide a little bit I put it together
in a short order before coming on here and just looking at it as the signal and then having all of the other available
stuff that like an attribution tool is either dropping into Salesforce or pulling Salesforce out and manipulating
in their own tool and we have all that stuff and it's useful but we use it for a different reason got some good uh
technical questions here love it all right thanks um yeah so I was wondering
uh Chris um this is Maybe coming from a different angle but I find it a very interesting question myself
also because you yourself are a Service Company by definition not a SAS company
um so my main question is how do you think this is different when it comes to
being a Service Company where you're more dependent on uh quality hours of
people experts that work on your clients versus being a SAS company which is more
scalable so to say is there like a certain cut off point in ARR where you can say okay look
we really need to implement these kinds of systems that is part one and then
part two is how important is it to pick the right CRM because I see uh that you
like maretto HubSpot and Salesforce but is this also implementable with for
example uh pipe Drive got it so just so I understand the question clearly you're coming from the perspective of trying to
understand if this is applicable for a Services business do I understand that right yeah
for example a business like yourself you're actually helping out other product or SAS companies that are
scalable more scalable than just having people do project management work
basically yeah so just to be clear so I own a company called refine Labs so I appointed my CEO uh the CEO Megan Bowen
um just a couple of months ago that company is a pure services company and then I started a company called etto
which is a software company but we're using services to be able to fund the company so that we can bootstrap it and
not have to raise VC so that's just a clarification but now as it relates to as it relates to like using this in a
Services business the differences in a service business versus a SAS company from a business model standpoint and the
Dynamics that drive all the stuff Downstream you have much uh lower gross margin profiles you have much different
u m Revenue multiple like valuation profiles you have Lex less access to VC
and other forms of financial Capital um and so what do all those things do it
drives down the amount of money that you can spend to acquire a customer your lifetime gross profit of a customer is
usually some usually different than Dynamics on a SAS company um and so the ability to track
the data is still incredibly useful um the difference in a service business is
that typically it's scales with people so you can't just get a 100 customers and onboard all 100 customers right out
the gate you have to get two and then two in a couple weeks and two in a couple weeks you need to build it because you need to hire and train and
onboard customers which is a little bit different um so I think from an analytics perspective you could track
all the same stuff Salesforce is like the easiest to track because of the
ecosystem and the technical details inside of it hubspot's making some good progress on that I think that other
lightweight crms just don't invest enough time in this part which is like the data architecture and the
infrastructure and the ecosystem to be able to fully support like a full-blown
model um and so like we in interact with like big Enterprise companies that are
using like sap as a CRM and then they have all their marketing data in HubSpot
or maretto and they're not connected together at all so they have their marketing data coming from one place the
sales data coming from another place can't Stitch it together um and creates
like a some a big problem that needs to get fixed in an Enterprise um and so I think it's more
about the difference between services and uh a product business is really
about how much you can spend to acquire a customer and how many customers that you can get at a period of time and then
typically the business model and the LTV of a custo or the lifetime of a customer
um and so those differences Drive how you run your go to market strategy and it changes how you invest in sales and
marketing as an overall percentage of Revenue um but from an analytic standpoint I think that both it would apply to both given if you're at a
certain stage or maturity where you have five or 10 reps or you have outbound sdrs you're spending millions or tens of
millions of dollars in marketing at some point you need to be able to look at that data and be able to make decisions
against it that's what this infrastructure allows you to do regardless of what you're selling so if I understand correctly basically not the
CAC but the whole service part of acquiring a customer is much more expensive when you're doing a service by
definition and therefore you really need to approach it in a different way and um
to follow up do you also think that uh starting out in pipe Drive is is a big
mistake when you want to reach a certain skill at some point like do you feel
have you experienced that it's easy to then switch for example to hop spot later on or is that really a decision
you need to make up front uh from a tech standpoint I don't think you need to make that decision up front early stage
like you build a lot of tech debt that's going to have to be rebuilt anyway whether you rebuild it in pipe drive or you rebuild it again in a different
system so um I wouldn't I like I don't think that it matters use what you use
what you is working for you right now don't get so lost in like what tool am I going to use or spending 3 months to
implement a tool versus spending three months trying to go and get more customers um and then at some point you'll start to feel some friction then
you'll say we need to optimize these things and then you'll make a decision either optimize them in the current platform or move platforms depending on
the needs of the business at that stage and then um just to sort of H like talk
a little bit more between services and product so like let's look at a $10 million Revenue company right okay
you're Services Company you're doing 10 million in Revenue if you're doing good you're doing 20% net uh net income you
have 2 million in eida that company's going to be valued off of ibaa 2 million ibaa Forex Revenue valuation $8 million
business less than 1X Revenue that exact same company that's a software company
at 10 million ARR could get valued at 10 to 20x revenue and be valued at1 to $200
million rather than an $8 million services company and so and that core
difference allows you to invest in growth a lot more aggressively because you're able to raise fund
at a much higher like Revenue multiple than you would in a Services business so while a Services business is trying to
have a two-month customer acquisition cost payback period due to eida and valuation constraints a SAS company
might say we're good with a three-year CAC payback because we'll be able to get to the next funding round and be able to continue to fund growth as the revenue
multiple expands expon almost exponentially so it's really about the allowable CAC and that's why you see
Services businesses that typically don't have invest almost anything in like a dedicated marketing department and have
a very lean sales team um for typically not always but typically due to that
phenomena exactly all right that was get back and forth we have a question from Adam I'm
gonna bring you on he also asked if uh the slides that you shared would be in
shared out they will be on YouTube later on Chris Walker's Channel drop the Link
in the chat for everybody cool yeah the exclusive for the the
listeners uh he can't come on so I'll read this from Adam for you do you recommend moving reporting to a BBI tool
like looker or do you and most of your clients use maintain the reporting
inside of Salesforce this is a good question it is a good question there's a ton of details
in the podcast that I just released today so you can feel free to reference that as well the difference is not where
you're looking at the data it's whether the data has integrity at the place that you're looking at it in and so the core
belief is that all of the data that you need and the way that you look at it should be set inside of the CRM not
pulled out of the CRM and then manipulated in Excel or postprocessing before it goes into bi so then the
people that are looking at it in bi and Excel are seeing a much different story than the individual people that are trying to build a report in Salesforce
and then you just have this place where because the Salesforce data isn't great and all this manipulation has to happen
that most people in the company aren't reporting on the same stuff and it just doesn't match up and so the thing that
we need to think about is if we're going to look at the data in bi that the data in bi is the data that we're not doing
all of this fixing and manipulation and filtering of the data from the CRM into
bi um so I think that's really the core distinction here so that if someone's
looking at it in bi or looking at trying to replicate a report in Salesforce that they can actually do it because the data
is the same so uh and it's just having a it's having a a a level of commitment to
having the operational tool the CRM which is basically the brain of your go
to market um having the brain have all the right data that you need to be able to operationalize create signals for
sales correct the right collect the right information report properly optimize and just having a commitment to
being able to do that in the core CRM he left a comment here I'll just read for listeners listening to the podcast later
this is where he's been having issues uh he's been trying to build this and looker we've been running into issues trying to combine all the data sources
building a custom object in Salesforce to create a source of Truth is a huge unlock today and then you have the
source of Truth and then you can take that object directly out of Salesforce into bi and make all of the reports a
hundred times better and more consistently than trying to have all the the objects connect together outside of
bi great unlock love that yeah I 100% agree we've worked with a couple of
clients that exclusively are primarily use bi tools to run their reporting and
the custom calculations and the workflows and the chaos that goes on behind the scenes to manipulate the data
uh breaks and then no one knows how to fix it either so it's uh it's definitely
not recommended okay great question I have another one that I got DM and this is a little bit off topic so we're going
to shift gears a little bit here let's do it all right this is on account and contact targeting so says we're shifting
our targeting approach specifically on LinkedIn to be account-based purely to improve delivery and focus our targeting
since their industry targeting is subpar they make a lot of assumptions with
industries that don't really align to our Target markets how would you use data enrichment providers to to get a
list and even potentially Source contacts as well for context we don't
have a dedicated account list or tiering so I was just thinking of going through
and seeing what accounts are in our CRM that fit our ICP and then going to a data tool to Source similar accounts how
would you approach this this the answer on this one is kind of like take a step backwards to go like 20 steps forwards I
think is the way that I would look at this that like sure like some to either
tools will help you or some marketers will go and just say let's just look at our close one accounts over the past 6
months and then just try to figure out what's the same about them or upload them into a tool and try to have the tool spit out a bunch of other lookalike
companies um but then you gener you basically have marketing running advertising to accounts and sales
doesn't even really know those same accounts they're not working them it's not tracked in the right way so there's
just like a lot of issues here so to step backwards is to if you're going to
have a like a quote unquote ABM strategy to have every single account the details
of that account the tier or the segment that that account falls into falls into all in the CRM there are companies that
I know that have 700,000 tier three accounts and every single account the
company name the website the details are inside of the CRM some ABM tools are data providers to that are able to sync
data otherwise you can go out and be able to get it and get everybody aligned
that these are the tier ones the exact accounts these are the tier tws and these are the tier 3s um and then have a
specific go to market motion or motions that are focused on those accounts based
on how much you can spend or acquire on that customer the real solution is taking a step back really having the
data and then when you go into LinkedIn you when you put tier one account list in the campaign or in the C in the
audience upload and you literally do a raw upload of actual accounts that you
know that those tier one accounts everyone in the business has agreed that that's a tier one account that it really matters to our sales team and things
like that and you clearly have a acknowledgement across the whole company about tier 3es or companies that aren't
on that list that you just wouldn't end up putting in advertising at all um and
so that's the uh the recommended approach even though it might quote unquote take a little bit longer it
really sets you and your you know advertising your program s up for more success love it I think the theme of the
episode today is source of Truth put it in the CR good point yeah okay this uh
person has a followup they can't come on live so they keep uh asking followup they are ahead of demand gen
and they agree with the approach should they work with their head of sales to
kind of Kick this off work with their peers first do a plan submit to leadership how do you would you suggest
they go internally to find a sales counterpart to work with to kick off the
account uh like selection process that we just talked about uh I would start
with getting connected with your the marketing leader and saying hey I think
I'm thinking about like just picking out these accounts or finding lookalikes over here what I think would be a much better idea is to like take a step back
and really be thoughtful and decide as a go to market team what accounts matter
the exact accounts having those details in Salesforce so that when we go out and spend $50,000 a month in advertising
that we have a much better way to understand whether that advertising is working or not because we've selected the accounts up front and we've decided
that they're valuable to our business and that sales is also going to be running motions when we start to get
signals and like those types of accounts are on our website that we're going to be able to get those signals and then go
and try and Outreach and get meetings with those companies and so in order for this to really be successful we need to have alignment because they are
integrated go to market motions that multiple departments need to all be aligned on who the accounts are that
they're valuable and then have the setup so that when marketing create signals or other signals that are created that then
sales and sdrs are able to take action on them um and so I would start with having the conversation if you're ahead
of demand gen having the conversation with your CMO um and then have the C start to work
with the CMO and then the CMO is most likely going to have a strategy for if when they involve the C Foo and the cro
and things like that I would look at that type of approach when you're trying to uh to make this implementation love
it we're going back to the custom object now for a question how does self report
attribution and software-based attribution UTM and touch points uh work
with the custom object so at the time of the
signal all the signal data that's available is stamped onto the record and
so if the customer had filled out a demo form or another place where you collect self-reported attribution that would be
part of it and it would be put on the record but if you look at all of the available go to market signal
self-reported attribution will only be on 51% of all the signals and so that's
one key thing to know UTM data will not be on all signals but you when UTM data
is available then we should stamp that data on inside of it we should know the actual offer we should know the pipeline
Source all that stuff can happen at the time of the signal um having all that data on the record then allows us to be
able to you know filter and slice that data to be able to answer certain questions in our business very easily it
could answer what is the ROI of this Google ads campaign or even this Google ads keyword or any other type of motion
where you're having spending money on advertising and driving to a direct response type of conversion like in a
Google ad and you'd be able to answer that question incredibly simply you'd be able to see where are people falling off
where are the lowquality keywords where all the places where we create conversions where the people never
convert through what campaigns and keywords they're coming from can we eliminate those you can make much more simple Roi calculations in terms of
dollars in to Hero pipeline dollars out or dollars in to actual Revenue out
against anything at the at the total Google ads level or even down to campaigns and
keywords um so it gives you all of that data on the record and then for some
signals you're going to have certain data and for other signals you're going to have certain data and then being able to use that data in a certain way to
optimize or answer a more micro question right so this the architecture really
allows us to answer macro questions um and then have the details
to be able to know where and how to look into into the micro um and so when you're trying to go
and optimize a Google ads campaign having this data helps it helps you flag hey we have low Roi on these campaigns
or hey we have low Roi on these keywords but then after that you have to go and make micro optimizations you have to go
and change the copy you have to change the landing page you have to do all these micro strategies but the the fact
that you focus there gets identified by these top level analytics um and so it's really about
being able to B understand and balance the macro to micro anything that we're doing in the micro should be driven by
the macro business story and the go to market performance that's why we should focus on things that's why when we
identify hey our demo to Hero opportunity rate is
7% The Benchmark from poetto and all that data is
31% if we just got it from 7% even halfway there to 15% we would double our
pipeline what would be the impact on that in the in the next year and you can go and run through those calculations but if you don't have the
custom object and you can't look at cohort conver verion rates you wouldn't you'd often times not even see that there's an opportunity there um it's
really about having the macro data to identify macro strategy adjustments or
big really big areas of opportunity or risk followup from the same
person how would you then use attribution touch points or campaign
members is that more for micro or adjustments like you just talked about
we're still working on our position so right now we ingest all B visible touch Point data and we're actually running
through a variety of different ways to analyze it that we think is different than like using just a blanket W shape
or u- shape but having it uh in concert with having this type of pipeline architecture in that data to be able to
look at the touch points in a different way um we don't have a full position on if those touch points are valuable and
if they are how they should be used so stay tuned uh for more details on that one and then basically like if I'll pull
this up for a second it's basically about acknowledging that the way we
measure signals to closed one needs to be different than how we measure how we
get Target accounts in market and that most of the things that happen inside of
multi-touch attribution are signals they are signals some that are
incredibly low quality and some that are higher quality that we' be able to tease out with data if we had it but there's
all of these things that happen while our target market is has not decided to
purchase something or has not been interested or prioritized it or don't even know that it exists there are
things that are happening there that we need to be able to better understand so that we can allocate Investments to get
more of our Target customers to create the signals I.E be in Market to buy and then just thinking about those as two
independent Concepts is the the direction that we're going here um and the way that we solve the target
market measurement my belief one person's belief is that everyone in the
industry is trying to solve it in One Way by trying to get a digital touch point or try to create some level of you
know marketing mix modeling to like justify LinkedIn ads so they're going all in that direction at poetto we're
going to go in an entirely different direction and I think it's going to uh lead to much better decisions for that
specific part of the Investments that happen in Market machine which honestly right now are not that high companies
aren't investing as a top part of it we just finished an analysis with a company I think it's a $13 million a year
marketing program budget and 6% of it is spent on demand creation or demand acceleration is a different way to look
at it 6% of the the overall budget that's on a $13 million budget we're
talking $500,000 or something and so and the reason that money doesn't get spent
there is because multi-touch attribution doesn't pick it up and so we just need I my belief is that we need a different
solution that multi-touch attribution has value from intent capture down um
but we most likely need to be looking at different solutions different entirely different dimensions of how we like
collect and look at the data for understanding demand creation great love it think we have time for one more and
we've got Russ coming on to ask his question yes yeah hi Chris and team um
we actually we actually have a a pre-sales platform for B2B and so we're a little more in the opportunity
Management Area um one of the things that we've been kind of working through
is a single source of Truth possible um from the standpoint of when you're in
that early Market development phase you can bring a lot of this information together we've actually built the custom
object as part of our solution and what we found is that um you know when you
start thinking about the entire customer life cycle not just from lead gen into opportunity
management or even in the pre-sale stage where it's less sales oriented more sales engineering oriented where you're
doing project management and you know slack channels and all these kind of ancillary feeds are happening that never
find their way into CRM um and then there's the handoff you know from the cell to the transition to the delivery
teams and then from delivery into expansion um where all of those are
different systems and so you've got a technical challenge of just unifying all this information um so we're kind of
leaning into this idea that uh uh single source of Truth is not it's distributed
um but I wanted to get your your thoughts on that yeah it's it feels a little nuanced because like distributed
source of Truth sort of means that there are multiple things that are all the source of Truth meaning that the CRM
still is the source of truth right um but I I'm on board with the distributed
nature which means that we have a commitment to having all of the systems have all of the right data which still means that there's no data manipulation
out of Salesforce into bi or a different other tool so I uh I see a ton of value
in that I think that um at some point companies will
transition from building custom bi dashboards to using purpose-built
software to look at data in the consistent way that everyone trusts um I
think that companies over and over reinvent the wheel in bi and they make a lot of mistakes along the way and that
they're rarely if ever up to a best practice of how you're supposed to look at the data which is a perfect use case
for building a purpose-built software tool for those purposes um so I think that
overtime um first we need to have the foundational pipeline architecture I.E a
custom object that looks across the entire customer life cycle that's collecting all that data then we have purpose-built analytics
that are then pulling out the data exactly what we need exactly how we're expecting it and then manipulating it in
a standardized way and then delivering that back to the customer with other parts of value like B real-time
benchmarks Market updates based on all the whole database that exists etc etc
um I think that that's where the market will go yeah one of the big challenges that we're working through that right
now on how much is how much further we build out our manage package with this
Universal kind of object idea um the object itself is getting complex and
extensible and you if I'm bringing all that lead gen marketing data demand gen data account information related stuff
that you've got the pre-sales U insights um it's getting into a very large kind
of custom object um so that's we're working through how to optimize that and
then along those same lines I think where where you're going is we're going to start investing in presets that are
part of our manage package for the visualizations to go along with that set because we turn over our system to many
of these companies and then then it goes into an itq an itq to get the visualizations in place that might take
three or four months and then the customer is not really getting the value for the data that we're deriving I feel
like what we're talking about is two different objects with two different like overall end goals like you have
this object that's built for pre-sales which is basically a different form of an opportunity object for a specific
part of the process that's collecting all that data and you have our object that's really trying to track all the stuff so what in in the case of this
like I would have two objects and then the object that we're talking about on the show would just be pulling off a
couple of key pieces of information from your object that is needed for the Analytics and so yours is actually just
another object that's feeding it with data just like an opportunity or an account record would that's what I'm
thinking yeah um thanks thank you all for being here another great Tuesday
love the engagement love that we've gotten this area of like technical I feel like more actionable uh shoot some
thumbs up in the chat if you feel like this level of detail like in Practical implementation was useful we'll take
that feedback um so thanks thank you all for being here we'll see you again next Tuesday bye
[Music]
everyone