# 📰 Daily News Bot - 48+ Commits Daily

**Last Update:** 2026-08-17 20:20:47

**Total News:** 12

**Sources:** Al Jazeera, NASA, BBC, Hacker News

---

## 📰 Latest News

### 1. Universal Health Coverage Could Save $1T and 114k Lives a Year, Yale Study

**Source:** Hacker News

**Category:** technology

**Description:**
<p>Article URL: <a href="https://ysph.yale.edu/news-article/universal-health-coverage-could-save-one-trillion-dollars-and-114000-lives-every-year/">https://ysph.yale.edu/news-article/universal-health-coverage-could-save-one-trillion-dollars-and-114000-lives-every-year/</a></p>
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=49332981">https://news.ycombinator.com/item?id=49332981</a></p>
<p>Points: 200</p>
<p># Comments: 253</p>

🔗 **Read more:** [https://ysph.yale.edu/news-article/universal-health-coverage-could-save-one-trillion-dollars-and-114000-lives-every-year/](https://ysph.yale.edu/news-article/universal-health-coverage-could-save-one-trillion-dollars-and-114000-lives-every-year/)

---

### 2. Launch HN: Speko (YC S26) – OpenRouter for Voice AI

**Source:** Hacker News

**Category:** technology

**Description:**
<p>Hi HN! I'm Bek, founder of Speko, a platform that finds an optimal combination of speech-to-text, LLM, and text-to-speech models, given your constraints, among all our public benchmarked options, and tells you why.<p>Demo: <a href="https://www.youtube.com/watch?v=no2LY2gRh-c" rel="nofollow">https://www.youtube.com/watch?v=no2LY2gRh-c</a><p>Typical production voice agent is an ensemble of three models: STT, an LLM, and TTS.<p>Each of those layers offers a dozen credible vendors, and each month there are new models on the market. Almost everyone evaluates once, picks a stack of their choice, and never rechecks because switching from a vendor to another involves yet another integration and arguments about the numbers.<p>The result is that you use voice agents running last quarter's models while better and cheaper options are available.<p>Before founding Speko, I spent four years as cofounder and CTO building voice agents for enterprises across Asia in 10+ languages. Each time a new speech model would arrive, we repeated the same ritual: hire native-speaking raters, benchmark it against our existing stack, and update production if it improved. Speko turns this process into an API. A team running thousands of calls a day told us: "we can literally go to this dashboard, switch the model, and it will do it for us."<p>How it works: you send a request with your optimization criteria (accuracy, latency, cost or balanced), language and region. The router filters to models which we measured for the given combination of constraints, benchmarks them, selects the winner, and returns a response with headers containing provider, model names, and the scores. The gateway prefetches signed session plans, so a new session dials the provider straight from memory; no control-plane round trip while a caller waits.<p>Failover happens only during connection setup stage: if the provider refuses the connection attempt, we start connecting to the runners-up.<p>Some of the customer stories: one founder came to us not knowing what to pick at all: he gave us his use case and now routes everything through the platform. A property management AI runs LiveKit in Python and had not updated STT or TTS since launch: they did not know their STT had high error rates on their calls, better options existed, and swapping always looked like an R&amp;D project. One team did not know which models to pick for Spanish. A medical team did not know which STT handles medical vocabulary best. In every case we helped find the right stack from the benchmarks, and now they route through us.<p>The measuring part is public: we pass the same inputs to every model in one region in different dated runs and we publish the boards, including those where our selections perform worse than alternatives. A launch demo answers which 30-second clip sounds better; production asks which model survives minute eight, so we test spontaneous speech, money and dates, ten-minute takes, and the rankings change. We trained an automatic scorer for TTS naturalness on our blind head-to-head listening votes; on providers it has never seen a vote for, it picks the same winner our raters do about as often as raters agree with each other.<p>We don't train or sell models ourselves, that's precisely how we keep our rankings impartial.<p>We also open sourced the gateway for teams who want to avoid an extra network hop on the audio path and don't want to share keys with our cloud (<a href="https://github.com/SpekoAI/gateway" rel="nofollow">https://github.com/SpekoAI/gateway</a>, MIT): one Go binary, which is running as a sidecar in your agent's container, speaks one local protocol over Unix socket, pins provider hosts and attaches your keys. In BYOK mode it doesn't communicate with us at all.<p>Notice that the anonymous, content-free telemetry is enabled by default, and one env var disables it.<p>Cost: the gateway and BYOK setup will be free forever, we charge for the hosted router and managed keys with consolidated billing. Since we started the batch in late June, external usage has grown about 25 percent per week on average, front-loaded toward the launch weeks.<p>I would love feedback from the community: how do you pick speech models now, and what makes you trust the third-party benchmark?<p><a href="https://speko.ai/">https://speko.ai/</a></p>
<hr />
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=49332751">https://news.ycombinator.com/item?id=49332751</a></p>
<p>Points: 30</p>
<p># Comments: 9</p>

🔗 **Read more:** [https://speko.ai/](https://speko.ai/)

---

### 3. Judge relying wholly on AI in order is covered by judicial immunity, court rules

**Source:** Hacker News

**Category:** technology

**Description:**
<p>Article URL: <a href="https://reason.com/volokh/2026/08/17/judges-allegedly-relying-wholly-on-ai-in-order-is-covered-by-judicial-immunity-court-rules/">https://reason.com/volokh/2026/08/17/judges-allegedly-relying-wholly-on-ai-in-order-is-covered-by-judicial-immunity-court-rules/</a></p>
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=49331625">https://news.ycombinator.com/item?id=49331625</a></p>
<p>Points: 27</p>
<p># Comments: 26</p>

🔗 **Read more:** [https://reason.com/volokh/2026/08/17/judges-allegedly-relying-wholly-on-ai-in-order-is-covered-by-judicial-immunity-court-rules/](https://reason.com/volokh/2026/08/17/judges-allegedly-relying-wholly-on-ai-in-order-is-covered-by-judicial-immunity-court-rules/)

---

### 4. Trump threatens to bomb US ally Oman if it 'gets in the way' over Iran deal

**Source:** BBC

**Category:** world

**Description:**
The US and Oman have been working separately to reopen the Strait of Hormuz, one of the world's busiest oil shipping routes.

🔗 **Read more:** [https://www.bbc.co.uk/news/articles/cy5dzk0ryzdo?at_medium=RSS&at_campaign=rss](https://www.bbc.co.uk/news/articles/cy5dzk0ryzdo?at_medium=RSS&at_campaign=rss)

---

### 5. Burnham exchanged messages with person posing as Trump's chief of staff

**Source:** BBC

**Category:** world

**Description:**
Downing Street has declined to comment on the security breach, first reported by Politico.

🔗 **Read more:** [https://www.bbc.co.uk/news/articles/clyvj5zdjj2o?at_medium=RSS&at_campaign=rss](https://www.bbc.co.uk/news/articles/clyvj5zdjj2o?at_medium=RSS&at_campaign=rss)

---

### 6. Parents pushed to breaking point by Child Maintenance Service, BBC told

**Source:** BBC

**Category:** world

**Description:**
Mothers describe battles to make ex-partners pay, while fathers say they have been wrongly charged thousands.

🔗 **Read more:** [https://www.bbc.co.uk/news/articles/c4g3re5ew8do?at_medium=RSS&at_campaign=rss](https://www.bbc.co.uk/news/articles/c4g3re5ew8do?at_medium=RSS&at_campaign=rss)

---

### 7. War on Iran: Phase II, Day 37

**Source:** Al Jazeera

**Category:** world

**Description:**
Iran is offering $30,000 for captured or killed US soldiers. Trump cuts back South Korea drills.

🔗 **Read more:** [https://www.aljazeera.com/video/newsfeed/2026/8/17/war-on-iran-phase-ii-day-37?traffic_source=rss](https://www.aljazeera.com/video/newsfeed/2026/8/17/war-on-iran-phase-ii-day-37?traffic_source=rss)

---

### 8. Somali army clashes with rebel forces for control of key city Baidoa

**Source:** Al Jazeera

**Category:** world

**Description:**
Somali forces repel rebel fighters in Baidoa after intense fighting involving explosives and dozens of casualties.

🔗 **Read more:** [https://www.aljazeera.com/news/2026/8/17/somali-army-clashes-with-rebel-forces-for-control-of-key-city-baidoa?traffic_source=rss](https://www.aljazeera.com/news/2026/8/17/somali-army-clashes-with-rebel-forces-for-control-of-key-city-baidoa?traffic_source=rss)

---

### 9. Democrats rebuke Trump over scaling back military drills with South Korea

**Source:** Al Jazeera

**Category:** world

**Description:**
Republican Senator Thom Tillis says the decision allows North Korea to provide more support to Russia in Ukraine.

🔗 **Read more:** [https://www.aljazeera.com/news/2026/8/17/democrats-rebuke-trump-over-scaling-back-military-drills-with-south-korea?traffic_source=rss](https://www.aljazeera.com/news/2026/8/17/democrats-rebuke-trump-over-scaling-back-military-drills-with-south-korea?traffic_source=rss)

---

### 10. Cyclone Hernan

**Source:** NASA

**Category:** nature

**Description:**
Natural event: Severe Storms

🔗 **Read more:** [https://eonet.gsfc.nasa.gov/api/v3/events/EONET_22562](https://eonet.gsfc.nasa.gov/api/v3/events/EONET_22562)

---

### 11. Tropical Storm Nangka

**Source:** NASA

**Category:** nature

**Description:**
Natural event: Severe Storms

🔗 **Read more:** [https://eonet.gsfc.nasa.gov/api/v3/events/EONET_22561](https://eonet.gsfc.nasa.gov/api/v3/events/EONET_22561)

---

### 12. Tropical Storm Lala

**Source:** NASA

**Category:** nature

**Description:**
Natural event: Severe Storms

🔗 **Read more:** [https://eonet.gsfc.nasa.gov/api/v3/events/EONET_22563](https://eonet.gsfc.nasa.gov/api/v3/events/EONET_22563)

---


**Built with ❤️ by GitHub Actions**