# 📰 Daily News Bot - 48+ Commits Daily

**Last Update:** 2026-11-05 22:20:55

**Total News:** 12

**Sources:** BBC, Al Jazeera, Hacker News, NASA

---

## 📰 Latest News

### 1. How to Lie With Statistics (1954) [pdf]

**Source:** Hacker News

**Category:** technology

**Description:**
<p>Article URL: <a href="https://www.horace.org/blog/wp-content/uploads/2012/05/How-to-Lie-With-Statistics-1954-Huff.pdf">https://www.horace.org/blog/wp-content/uploads/2012/05/How-to-Lie-With-Statistics-1954-Huff.pdf</a></p>
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=50382594">https://news.ycombinator.com/item?id=50382594</a></p>
<p>Points: 4</p>
<p># Comments: 0</p>

🔗 **Read more:** [https://www.horace.org/blog/wp-content/uploads/2012/05/How-to-Lie-With-Statistics-1954-Huff.pdf](https://www.horace.org/blog/wp-content/uploads/2012/05/How-to-Lie-With-Statistics-1954-Huff.pdf)

---

### 2. Nasdaq Sinks 5% as Investors Retreat from AI Trade After Election

**Source:** Hacker News

**Category:** technology

**Description:**
<p>Article URL: <a href="https://www.wsj.com/livecoverage/stock-market-today-dow-sp-500-nasdaq-11-05-2026">https://www.wsj.com/livecoverage/stock-market-today-dow-sp-500-nasdaq-11-05-2026</a></p>
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=50382179">https://news.ycombinator.com/item?id=50382179</a></p>
<p>Points: 54</p>
<p># Comments: 35</p>

🔗 **Read more:** [https://www.wsj.com/livecoverage/stock-market-today-dow-sp-500-nasdaq-11-05-2026](https://www.wsj.com/livecoverage/stock-market-today-dow-sp-500-nasdaq-11-05-2026)

---

### 3. Launch HN: Rivet (YC W23) – Scale and Orchestrate Agents on S3

**Source:** Hacker News

**Category:** technology

**Description:**
<p>Hey HN, this is Nathan and Nicholas from Rivet (<a href="https://rivet.dev">https://rivet.dev</a>) – a fast, high-density, and scalable orchestrator for agentic workloads using the actor model. Rather than running a heavyweight sandbox per agent, each agent gets a lightweight actor backed by S3.<p>Actors provide a long-lived process for long agent turns, in-memory state for context, a WebSocket server for multiplayer, durable SQLite storage backed by S3, and hibernation when idle.<p>It's a similar model to Cloudflare Durable Objects, but it’s open source and self-hostable.<p>Here’s a video walkthrough: <a href="https://www.youtube.com/watch?v=3Ev6I7DOV9c" rel="nofollow">https://www.youtube.com/watch?v=3Ev6I7DOV9c</a><p>When we went through YC in 2023, we were building infrastructure for multiplayer games like Diep and Krunker. This involved heavily optimizing high-throughput matchmaking, real-time player messages, and blitz scaling. Through that process, we spent a lot of time on workloads where Postgres couldn't keep up with our throughput. We started out by hacking together Lua scripts on top of Redis, but this became too cumbersome to maintain and upgrade. This led us to extend our game server orchestrator to support what we call Rivet Actors today: many lightweight workers with in-memory state and durable storage. By using actors, we were able to serve tens of millions of monthly active users.<p>As agents grew in popularity, it became clear that running agents in sandboxes is inefficient. Sandboxes are expensive, mostly idle, and slow to start. Developers started using actors because they are far more memory efficient (72 KB baseline for actors vs 512 MB for a minimal sandbox) and fast to start (4.9 ms p99 for actors vs 1.7 s p99 for sandboxes).<p>For example, Amp is using Rivet to orchestrate multiplayer agents. They originally tried to build on Cloudflare Durable Objects, but couldn’t launch because of the platform’s limitations and unresponsive support. They migrated to Rivet Actors in a weekend and deploy on-prem. Rivet’s flexible architecture lets them adapt it to their own use cases without being constrained by a framework or the memory, storage, and runtime limits of Cloudflare Durable Objects.<p>Under the hood, Rivet is backed by S3 while maintaining SSD speeds.<p>Why S3? Previously, Rivet ran on FoundationDB. However, we were surprised to find that companies are storing orders of magnitude more data on Rivet Actors than in Postgres, such as large session transcripts, agent artifacts, and full POSIX filesystems. As their data grew, they had to start paying for SSDs that sat mostly idle with old transcripts. This led us to double down on S3 as our primary storage medium without sacrificing performance. This choice means that data stored on Rivet is 10× cheaper than on EBS gp3 while maintaining SSD speeds.<p>It’s not as simple as writing data straight to S3. Lots of PUTs for tiny blobs of data are slow and expensive. Instead, we use an SSD tier to optimize speed and cost:<p>When you write data to an actor’s SQLite database, the write is acknowledged once SSDs in 2 of 3 availability zones have it. Then, the data is batched to S3 in the background. This means that S3 is never on the write path, which lowers latency and cost. When reading data or waking an actor, Rivet reads from SSDs if already cached and falls back to S3 if not. SSD caches can be tuned to meet your needs, giving you configurable tiered storage for your actors.<p>This architecture lets Rivet provide 1.07 ms durable writes (3 AZ, p99), 1.36 ms reads (p99), and 138 ms reads from object storage (p99).<p>We’ve spent a lot of time making sure that Rivet can run wherever you need it. Self-hosting requires deploying a single Rust binary with S3 as the only dependency, Rivet Cloud lets you deploy dedicated clusters on AWS or GCP in any region, and BYOC lets us deploy Rivet to your VPC without having to operate it yourself. Rivet also runs identically in local dev as in production, since Rivet is a lightweight binary that runs anywhere<p>Rivet Actors can be written in TypeScript or Rust. Out of the box, they support agents (Pi Durable), workflows, real-time, multiplayer, running AI-generated code, Durable Streams, and integrations with tools like Vercel’s Eve and Turso. See all of our available guides, or point your agent at them: <a href="https://rivet.dev/docs/#guides">https://rivet.dev/docs/#guides</a><p>Try it out now, by reading our quickstart guides (<a href="https://rivet.dev/docs/">https://rivet.dev/docs/</a>) or ask your agent: “Run npx skills add rivet-dev/skills, then build a multiplayer chat agent and run it locally.”<p>We’d love to get feedback on your experience with Rivet! We’re deeply invested in making Rivet an easy-to-self-host, flexible, and efficient way to run agentic workloads.<p>GitHub: <a href="https://github.com/rivet-dev/rivet" rel="nofollow">https://github.com/rivet-dev/rivet</a><p>Architecture: <a href="https://rivet.dev/docs/architecture/">https://rivet.dev/docs/architecture/</a><p>Benchmarks: <a href="https://rivet.dev/docs/benchmarking/">https://rivet.dev/docs/benchmarking/</a><p>Self-hosting: <a href="https://rivet.dev/docs/deploy/self-host/">https://rivet.dev/docs/deploy/self-host/</a></p>
<hr />
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=50381687">https://news.ycombinator.com/item?id=50381687</a></p>
<p>Points: 24</p>
<p># Comments: 16</p>

🔗 **Read more:** [https://github.com/rivet-dev/rivet](https://github.com/rivet-dev/rivet)

---

### 4. Russell Brand found guilty of rape and sexual assault

**Source:** BBC

**Category:** world

**Description:**
Brand is told to expect a prison sentence "of some length" and faces more rape allegations, it can now be reported.

🔗 **Read more:** [https://www.bbc.co.uk/news/articles/ckyvrze96y70o?at_medium=RSS&at_campaign=rss](https://www.bbc.co.uk/news/articles/ckyvrze96y70o?at_medium=RSS&at_campaign=rss)

---

### 5. Watch: Met Police release Brand interview footage

**Source:** BBC

**Category:** world

**Description:**
Brand was found guilty of one count of rape and three sexual assaults at Southwark Crown Court.

🔗 **Read more:** [https://www.bbc.co.uk/news/videos/c693ze38vywxo?at_medium=RSS&at_campaign=rss](https://www.bbc.co.uk/news/videos/c693ze38vywxo?at_medium=RSS&at_campaign=rss)

---

### 6. Russell Brand is being investigated over two new rape complaints, police say

**Source:** BBC

**Category:** world

**Description:**
Det Supt Andy Furphy said he hoped other potential victims would gain "courage" and "confidence" from the guilty verdicts.

🔗 **Read more:** [https://www.bbc.co.uk/news/articles/c6vgx8q09gg4o?at_medium=RSS&at_campaign=rss](https://www.bbc.co.uk/news/articles/c6vgx8q09gg4o?at_medium=RSS&at_campaign=rss)

---

### 7. Could Football Change After Jesus de Miguel’s Death?

**Source:** Al Jazeera

**Category:** world

**Description:**
Could football change after the death of Jesus de Miguel?

🔗 **Read more:** [https://www.aljazeera.com/video/newsfeed/2026/11/5/could-football-change-after-jesus-de-miguels-death?traffic_source=rss](https://www.aljazeera.com/video/newsfeed/2026/11/5/could-football-change-after-jesus-de-miguels-death?traffic_source=rss)

---

### 8. AI stocks plunge after US election, driving down markets

**Source:** Al Jazeera

**Category:** world

**Description:**
Tech stocks lead US market slide as investors weigh impact of midterm election results on AI industry.

🔗 **Read more:** [https://www.aljazeera.com/economy/2026/11/5/ai-stocks-plunge-after-election-driving-down-us-markets?traffic_source=rss](https://www.aljazeera.com/economy/2026/11/5/ai-stocks-plunge-after-election-driving-down-us-markets?traffic_source=rss)

---

### 9. Jordanian officer killed in stabbing attack in Amman

**Source:** Al Jazeera

**Category:** world

**Description:**
A Jordanian security officer has been killed and another one wounded near the Sri Lankan embassy in Amman.

🔗 **Read more:** [https://www.aljazeera.com/video/newsfeed/2026/11/5/jordanian-officer-killed-in-stabbing-attack-in-amman?traffic_source=rss](https://www.aljazeera.com/video/newsfeed/2026/11/5/jordanian-officer-killed-in-stabbing-attack-in-amman?traffic_source=rss)

---

### 10. Wildfire Wild River, Coos, New Hampshire

**Source:** NASA

**Category:** nature

**Description:**
Natural event: Wildfires

🔗 **Read more:** [https://eonet.gsfc.nasa.gov/api/v3/events/EONET_26057](https://eonet.gsfc.nasa.gov/api/v3/events/EONET_26057)

---

### 11. Tropical Cyclone Murasu

**Source:** NASA

**Category:** nature

**Description:**
Natural event: Severe Storms

🔗 **Read more:** [https://eonet.gsfc.nasa.gov/api/v3/events/EONET_25964](https://eonet.gsfc.nasa.gov/api/v3/events/EONET_25964)

---

### 12. Prescribed Fire Dry Lake Hills Piles RX, Coconino, Arizona

**Source:** NASA

**Category:** nature

**Description:**
Natural event: Wildfires

🔗 **Read more:** [https://eonet.gsfc.nasa.gov/api/v3/events/EONET_25984](https://eonet.gsfc.nasa.gov/api/v3/events/EONET_25984)

---


**Built with ❤️ by GitHub Actions**