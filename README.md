# 📰 Daily News Bot - 48+ Commits Daily

**Last Update:** 2026-10-19 21:05:31

**Total News:** 12

**Sources:** Hacker News, NASA, Al Jazeera, BBC

---

## 📰 Latest News

### 1. Evidence (YC S21) Is Hiring Software Engineers

**Source:** Hacker News

**Category:** technology

**Description:**
<p>Article URL: <a href="https://evidence.dev/jobs">https://evidence.dev/jobs</a></p>
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=50155172">https://news.ycombinator.com/item?id=50155172</a></p>
<p>Points: 0</p>
<p># Comments: 0</p>

🔗 **Read more:** [https://evidence.dev/jobs](https://evidence.dev/jobs)

---

### 2. Launch HN: Laminar (YC S24) – We trained a model to catch silent agent failures

**Source:** Hacker News

**Category:** technology

**Description:**
<p>Hi HN, we’re Robert and Din from Laminar (<a href="https://laminar.sh">https://laminar.sh</a>). We’ve been building open-source observability for AI agents since 2024. Recently, we released flow-1, a model trained with RL to find errors in agent traces. On our benchmark (<a href="https://laminar.sh/blog/flow-1">https://laminar.sh/blog/flow-1</a>), it matches GPT-6-sol in detection quality while being 23x cheaper. This makes it affordable to analyze every production agent trace, without sampling.<p>Here’s a one-minute walkthrough: <a href="https://youtu.be/KJa3h6ZJNLQ" rel="nofollow">https://youtu.be/KJa3h6ZJNLQ</a><p>We also put together a post with example traces and analyses from flow-1 and other models: <a href="https://laminar.sh/blog/flow-1-in-action">https://laminar.sh/blog/flow-1-in-action</a><p>Agent observability is crowded, so instead of a bullet list of how Laminar differs from X, we’ll explain how we’re solving agent observability from first principles.<p>Agents now run for many steps and fail implicitly. An agent can click the wrong button or cite the wrong document while every call completes successfully. These errors are the most useful ones to catch and understand. To find them, you need to understand what the agent was trying to do and inspect its LLM calls and tool results. Simply looking at the final agent output is not enough.<p>Collecting traces alone doesn’t solve this. A lot of agent observability platforms are still data collectors at their core. You can end up paying to store traces that nobody has time to read or extract value from.<p>Using another LLM to inspect traces is THE solution, but capable models are expensive at scale and cheaper ones often miss errors or flag unrelated things.<p>So we built our model to solve exactly this problem. We finetuned a small OSS model and then post trained it with RL on thousands of synthetic investigations of realistic agent workflows in software, legal, customer support, etc. We got a model that is both good at agent trace analysis and very cheap to run.<p>flow-1 runs inside a harness we call Signals. It acts as a coding agent, treating an agent trace like a repo, with each span (an LLM call, tool call, etc.) as a file. It starts from a compressed string representation of a full agent trace and a user prompt, then greps across spans and reads the relevant ones in full.<p>The beauty of Signals is that it can respond to a general prompt. You can ask it to identify user frustration, check whether your browser agent completed a checkout, and so on. It’s not limited to raw error detection. It returns findings as JSON in a schema users can freely define. We call these signal events.<p>Once you’re analyzing every trace, you also have too many individual events to read. That’s why we automatically group similar signal events into clusters. You can see recurring problems and how often they happen, then drill into individual events and the traces behind them.<p>You can use traces from a cluster to build an eval dataset for that type of failure. You can then use your favourite coding agent to hillclimb on those evals and check that the fix works across these cases before shipping it to prod.<p>Trace → analyze → catch errors and form clusters → fix → release. Making this loop easy is why we built Laminar.<p>We’ve put the same thought into the rest of Laminar. Our blog (<a href="https://laminar.sh/blog">https://laminar.sh/blog</a>) explains how looking closely at how agents actually work led us to build 20x trace compression, a custom SQL query engine and automatic task extraction.<p>Laminar is Apache 2.0 and self-hostable (<a href="https://github.com/lmnr-ai/lmnr" rel="nofollow">https://github.com/lmnr-ai/lmnr</a>). We make money from the managed cloud.<p>We’d love to hear how you track your agents’ performance today. How much do you learn from user feedback versus your own monitoring? And when you fix something, how do you check that it hasn’t introduced a different failure?</p>
<hr />
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=50154029">https://news.ycombinator.com/item?id=50154029</a></p>
<p>Points: 18</p>
<p># Comments: 4</p>

🔗 **Read more:** [https://news.ycombinator.com/item?id=50154029](https://news.ycombinator.com/item?id=50154029)

---

### 3. Degraded availability for GitHub Actions, GitHub Pages and Webhooks

**Source:** Hacker News

**Category:** technology

**Description:**
<p>Article URL: <a href="https://www.githubstatus.com/incidents/8tzbpcnl75jp">https://www.githubstatus.com/incidents/8tzbpcnl75jp</a></p>
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=50153934">https://news.ycombinator.com/item?id=50153934</a></p>
<p>Points: 106</p>
<p># Comments: 74</p>

🔗 **Read more:** [https://www.githubstatus.com/incidents/8tzbpcnl75jp](https://www.githubstatus.com/incidents/8tzbpcnl75jp)

---

### 4. Watch: Are the French riots a warning of an intense election to come?

**Source:** BBC

**Category:** world

**Description:**
Rioting, looting and vandalism has gripped France over the weekend after protests spiralled out of control across the country.

🔗 **Read more:** [https://www.bbc.co.uk/news/videos/ckzd60dy746qo?at_medium=RSS&at_campaign=rss](https://www.bbc.co.uk/news/videos/ckzd60dy746qo?at_medium=RSS&at_campaign=rss)

---

### 5. Australian MP critically injured after being hit by car in apparent attack

**Source:** BBC

**Category:** world

**Description:**
The independent politician is in hospital after what the prime minister says may have been a deliberate attack.

🔗 **Read more:** [https://www.bbc.co.uk/news/articles/cwp9g43g2p07o?at_medium=RSS&at_campaign=rss](https://www.bbc.co.uk/news/articles/cwp9g43g2p07o?at_medium=RSS&at_campaign=rss)

---

### 6. Woman says she 'closed eyes and tried not to be there' during alleged Russell Brand rape

**Source:** BBC

**Category:** world

**Description:**
The 51-year-old faces three counts of rape, three charges of sexual assault and one of indecent assault.

🔗 **Read more:** [https://www.bbc.co.uk/news/articles/cvj6jylk3456o?at_medium=RSS&at_campaign=rss](https://www.bbc.co.uk/news/articles/cvj6jylk3456o?at_medium=RSS&at_campaign=rss)

---

### 7. Brazilian court orders Meta to prove Lula and Bolsonaro get equal treatment

**Source:** Al Jazeera

**Category:** world

**Description:**
A judge also doubled the daily fine for noncompliance with a previous court order governing political content.

🔗 **Read more:** [https://www.aljazeera.com/news/2026/10/19/brazilian-court-orders-meta-to-prove-lula-and-bolsonaro-get-equal-treatment?traffic_source=rss](https://www.aljazeera.com/news/2026/10/19/brazilian-court-orders-meta-to-prove-lula-and-bolsonaro-get-equal-treatment?traffic_source=rss)

---

### 8. 12 migrants, including an infant, drown in two incidents off Greece

**Source:** Al Jazeera

**Category:** world

**Description:**
Two separate boat incidents off the Greek islands of Lesbos and Samos left 12 migrants dead.

🔗 **Read more:** [https://www.aljazeera.com/video/newsfeed/2026/10/19/12-migrants-including-an-infant-drown-in-two-incidents-off-greece?traffic_source=rss](https://www.aljazeera.com/video/newsfeed/2026/10/19/12-migrants-including-an-infant-drown-in-two-incidents-off-greece?traffic_source=rss)

---

### 9. Trump backs Netanyahu: Is the US planning a new Iran attack with Israel?

**Source:** Al Jazeera

**Category:** world

**Description:**
Trump’s endorsement comes after he previously shied away from fully backing Netanyahu’s election campaign.

🔗 **Read more:** [https://www.aljazeera.com/news/2026/10/19/trump-backs-netanyahu-is-the-us-planning-a-new-iran-attack-with-israel?traffic_source=rss](https://www.aljazeera.com/news/2026/10/19/trump-backs-netanyahu-is-the-us-planning-a-new-iran-attack-with-israel?traffic_source=rss)

---

### 10. Tropical Cyclone Wati

**Source:** NASA

**Category:** nature

**Description:**
Natural event: Severe Storms

🔗 **Read more:** [https://eonet.gsfc.nasa.gov/api/v3/events/EONET_25340](https://eonet.gsfc.nasa.gov/api/v3/events/EONET_25340)

---

### 11. Super Typhoon Champi

**Source:** NASA

**Category:** nature

**Description:**
Natural event: Severe Storms

🔗 **Read more:** [https://eonet.gsfc.nasa.gov/api/v3/events/EONET_25339](https://eonet.gsfc.nasa.gov/api/v3/events/EONET_25339)

---

### 12. Prescribed Fire Newman Piles RX, Coconino, Arizona

**Source:** NASA

**Category:** nature

**Description:**
Natural event: Wildfires

🔗 **Read more:** [https://eonet.gsfc.nasa.gov/api/v3/events/EONET_25310](https://eonet.gsfc.nasa.gov/api/v3/events/EONET_25310)

---


**Built with ❤️ by GitHub Actions**