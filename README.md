# 📰 Daily News Bot - 48+ Commits Daily

**Last Update:** 2026-08-17 19:15:50

**Total News:** 12

**Sources:** Al Jazeera, NASA, BBC, Hacker News

---

## 📰 Latest News

### 1. Launch HN: Speko (YC S26) – OpenRouter for Voice AI

**Source:** Hacker News

**Category:** technology

**Description:**
<p>Hi HN! I'm Bek, founder of Speko, a platform that finds an optimal combination of speech-to-text, LLM, and text-to-speech models, given your constraints, among all our public benchmarked options, and tells you why.<p>Demo: <a href="https://youtu.be/no2LY2gRh-c" rel="nofollow">https://youtu.be/no2LY2gRh-c</a><p>Typical production voice agent is an ensemble of three models: STT, an LLM, and TTS.<p>Each of those layers offers a dozen credible vendors, and each month there are new models on the market. Almost everyone evaluates once, picks a stack of their choice, and never rechecks because switching from a vendor to another involves yet another integration and arguments about the numbers.<p>The result is that you use voice agents running last quarter's models while better and cheaper options are available.<p>Before founding Speko, I spent four years as cofounder and CTO building voice agents for enterprises across Asia in 10+ languages. Each time a new speech model would arrive, we repeated the same ritual: hire native-speaking raters, benchmark it against our existing stack, and update production if it improved. Speko turns this process into an API. A team running thousands of calls a day told us: "we can literally go to this dashboard, switch the model, and it will do it for us."<p>How it works: you send a request with your optimization criteria (accuracy, latency, cost or balanced), language and region. The router filters to models which we measured for the given combination of constraints, benchmarks them, selects the winner, and returns a response with headers containing provider, model names, and the scores. The gateway prefetches signed session plans, so a new session dials the provider straight from memory; no control-plane round trip while a caller waits.<p>Failover happens only during connection setup stage: if the provider refuses the connection attempt, we start connecting to the runners-up.<p>Some of the customer stories: one founder came to us not knowing what to pick at all: he gave us his use case and now routes everything through the platform. A property management AI runs LiveKit in Python and had not updated STT or TTS since launch: they did not know their STT had high error rates on their calls, better options existed, and swapping always looked like an R&amp;D project. One team did not know which models to pick for Spanish. A medical team did not know which STT handles medical vocabulary best. In every case we helped find the right stack from the benchmarks, and now they route through us.<p>The measuring part is public: we pass the same inputs to every model in one region in different dated runs and we publish the boards, including those where our selections perform worse than alternatives. A launch demo answers which 30-second clip sounds better; production asks which model survives minute eight, so we test spontaneous speech, money and dates, ten-minute takes, and the rankings change. We trained an automatic scorer for TTS naturalness on our blind head-to-head listening votes; on providers it has never seen a vote for, it picks the same winner our raters do about as often as raters agree with each other.<p>We don't train or sell models ourselves, that's precisely how we keep our rankings impartial.<p>We also open sourced the gateway for teams who want to avoid an extra network hop on the audio path and don't want to share keys with our cloud (<a href="https://github.com/SpekoAI/gateway" rel="nofollow">https://github.com/SpekoAI/gateway</a>, MIT): one Go binary, which is running as a sidecar in your agent's container, speaks one local protocol over Unix socket, pins provider hosts and attaches your keys. In BYOK mode it doesn't communicate with us at all.<p>Notice that the anonymous, content-free telemetry is enabled by default, and one env var disables it.<p>Cost: the gateway and BYOK setup will be free forever, we charge for the hosted router and managed keys with consolidated billing. Since we started the batch in late June, external usage has grown about 25 percent per week on average, front-loaded toward the launch weeks.<p>I would love feedback from the community: how do you pick speech models now, and what makes you trust the third-party benchmark?</p>
<hr />
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=49332751">https://news.ycombinator.com/item?id=49332751</a></p>
<p>Points: 7</p>
<p># Comments: 0</p>

🔗 **Read more:** [https://news.ycombinator.com/item?id=49332751](https://news.ycombinator.com/item?id=49332751)

---

### 2. Ask HN: GitHub employees what's going on? Why?

**Source:** Hacker News

**Category:** technology

**Description:**
<p>Pretty self explanatory. Could you folks shed some light on why these issues keep happening?<p>I’ve noticed most posts and replies are just people coming to their own conclusions based on whatever published data.<p>I think it would be helpful to get some actual, non-corporate/marketing information on the goings-on by those that actually see what’s happening on the inside.<p>Thanks<p>Can</p>
<hr />
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=49332495">https://news.ycombinator.com/item?id=49332495</a></p>
<p>Points: 30</p>
<p># Comments: 14</p>

🔗 **Read more:** [https://news.ycombinator.com/item?id=49332495](https://news.ycombinator.com/item?id=49332495)

---

### 3. Qwen3.8-27B at 256K on a 24GB RTX PRO 4000 SFF (432 GB/s): 50 tok/s with MTP

**Source:** Hacker News

**Category:** technology

**Description:**
<p>Article URL: <a href="https://piszczek.pl/blog/qwen38-27b-256k-50-tps-24gb-gpu">https://piszczek.pl/blog/qwen38-27b-256k-50-tps-24gb-gpu</a></p>
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=49331607">https://news.ycombinator.com/item?id=49331607</a></p>
<p>Points: 16</p>
<p># Comments: 4</p>

🔗 **Read more:** [https://piszczek.pl/blog/qwen38-27b-256k-50-tps-24gb-gpu](https://piszczek.pl/blog/qwen38-27b-256k-50-tps-24gb-gpu)

---

### 4. Trump threatens to bomb Oman if it 'gets in the way' over Iran issue

**Source:** BBC

**Category:** world

**Description:**
The president also told Fox News the US had a direct backchannel with the Islamic Revolutionary Guard Corps - something it denies.

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

### 7. Rights group urges FIFA to block Infantino re-election bid over term limits

**Source:** Al Jazeera

**Category:** world

**Description:**
FairSquare says the FIFA president should not be able to run again under the world football organisation&#039;s statutes.

🔗 **Read more:** [https://www.aljazeera.com/sports/2026/8/17/rights-group-urges-fifa-to-block-infantino-re-election-bid-over-term-limits?traffic_source=rss](https://www.aljazeera.com/sports/2026/8/17/rights-group-urges-fifa-to-block-infantino-re-election-bid-over-term-limits?traffic_source=rss)

---

### 8. Police execute controlled World War II–era Mine explosion

**Source:** Al Jazeera

**Category:** world

**Description:**
Video footage released by police on Sunday shows Slovak bomb disposal experts executing a mine detonation.

🔗 **Read more:** [https://www.aljazeera.com/video/newsfeed/2026/8/17/police-execute-controlled-world-war-ii-era-mine?traffic_source=rss](https://www.aljazeera.com/video/newsfeed/2026/8/17/police-execute-controlled-world-war-ii-era-mine?traffic_source=rss)

---

### 9. Trump demands Iran ‘put up the white flag of surrender’ as MoU expires

**Source:** Al Jazeera

**Category:** world

**Description:**
President also claims US is in direct contact with IRGC, denies a rush to end conflict ahead of November&#039;s US midterms.

🔗 **Read more:** [https://www.aljazeera.com/news/2026/8/17/trump-demands-iran-put-up-the-white-flag-of-surrender-as-mou-expires?traffic_source=rss](https://www.aljazeera.com/news/2026/8/17/trump-demands-iran-put-up-the-white-flag-of-surrender-as-mou-expires?traffic_source=rss)

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