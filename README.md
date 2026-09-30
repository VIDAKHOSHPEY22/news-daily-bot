# 📰 Daily News Bot - 48+ Commits Daily

**Last Update:** 2026-09-30 23:00:23

**Total News:** 12

**Sources:** BBC, Al Jazeera, Hacker News, NASA

---

## 📰 Latest News

### 1. 5x faster Edge Functions: V8 isolates to Firecracker MicroVMs

**Source:** Hacker News

**Category:** technology

**Description:**
<p>Article URL: <a href="https://www.netlify.com/blog/edge-functions-firecracker-microvms/">https://www.netlify.com/blog/edge-functions-firecracker-microvms/</a></p>
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=49912444">https://news.ycombinator.com/item?id=49912444</a></p>
<p>Points: 13</p>
<p># Comments: 3</p>

🔗 **Read more:** [https://www.netlify.com/blog/edge-functions-firecracker-microvms/](https://www.netlify.com/blog/edge-functions-firecracker-microvms/)

---

### 2. Launch HN: Magnitude (YC S25) – Self-optimizing inference engine for agents

**Source:** Hacker News

**Category:** technology

**Description:**
<p>Hey HN, Anders and Tom here. We're building Magnitude, an inference engine for agents that optimizes itself to run as fast as possible on your hardware. It works on Mac, Linux, and Windows on any hardware and is up to 2x faster than llama.cpp.<p>We're both software engineers and previously built an open source browser agent to 4k+ GH stars and 100k+ downloads. We increasingly wanted to run it on local models, but found that no inference engine worked for our use case.<p>Inference engines today all make a performance tradeoff. They are either:<p>- Built for batched inference on datacenter hardware at the cost of single-session performance (vLLM, SGLang)
- Designed for broad compatibility instead of optimizing for specific hardware (llama.cpp, Ollama)
- Specialized for specific hardware or models but lacking engine completeness (oMLX, ds4)<p>Plus none of them are designed for running agents locally. Sessions are long, several often run at once, and you still want to use your computer for other things.<p>Magnitude is built for maximum performance on your hardware and running local agents:<p>- On-device compilation and tuning: Kernels are written with flexible parameters that are tuned on your actual device before the model runs. This gives you broad hardware compatibility with the same performance ceiling as hardware-specific kernels.<p>- Focus on best architectures: We write our tunable, highly efficient kernels for the most popular open-weights families. This allows us to achieve and surpass the performance of hardware or model specialized engines, without forcing ourselves to over-generalize at the cost of performance.<p>- Dynamic memory allocation: Magnitude reserves only enough memory up front to hold model weights. As your agent sessions grow, the memory heap dynamically increases, and frees itself when agents stop. Your hardware can still be used for other stuff while agents run.<p>- Hybrid paged attention: We borrow the best ideas from engines like SGLang to allow concurrent sessions to share prefix caches, but optimize placement for memory-adjacency so single-session performance doesn't suffer.<p>Magnitude is fully open source (Apache 2.0). We built it in Rust, including a custom GPU kernel runtime and autotuner. We take inspiration from the best innovations in inference from academics (e.g. FlashAttention, FlashInfer, TurboQuant) as well as other engines (e.g. SGLang radix attention) to reach the performance ceiling.<p>Benchmarked against llama.cpp with Qwen 3.6 35B A3B (4 bit), 64k context, no speculative decoding:<p>Metal (Mac M4 Pro 48 GB)
- 92% faster decode (30 tok/s → 57 tok/s)
- 9% faster prefill (466 tok/s → 507 tok/s)
- 28% less per-agent memory usage<p>CUDA (DGX Spark)
- 19% faster decode (49 tok/s → 58 tok/s)
- 23% faster prefill (2,033 tok/s → 2,507 tok/s)
- 27% less per-agent memory usage<p>Magnitude ships as a desktop app that you can easily connect with whatever agents you already use (Pi, OpenCode, Hermes, Codex, and more). It automatically runs models on demand when these agents actually need them, and shuts them down after inactivity.
Here's what it looks like: <a href="https://www.youtube.com/watch?v=0qE8BWEZu7o" rel="nofollow">https://www.youtube.com/watch?v=0qE8BWEZu7o</a><p>We're excited to push Magnitude further to let you run bigger models on the same hardware while continuing to improve performance. Our plans include:<p>- Expert streaming: store experts on RAM or disk and load them just-in-time. This lets you run models bigger than what otherwise would fit on your GPU.<p>- Kernel compiler: our current kernels tune a few parameters to fit your hardware. We can take this further with a fully custom compiler that automatically chooses how to fuse kernels and which implementations to use, to make it fit to your hardware even better.<p>- Multi-device utilization: Make the best possible use of all hardware on a system (CPU, GPUs, RAM, disk) by detecting these and automatically solving for the best model layout.<p>We'd love for more people to try it out and give us feedback. Feel free to comment here, we'll be around all day!</p>
<hr />
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=49911995">https://news.ycombinator.com/item?id=49911995</a></p>
<p>Points: 58</p>
<p># Comments: 33</p>

🔗 **Read more:** [https://github.com/magnitudedev/magnitude](https://github.com/magnitudedev/magnitude)

---

### 3. Commit Description as a Thinking Tool

**Source:** Hacker News

**Category:** technology

**Description:**
<p>Article URL: <a href="https://yedhu.me/posts/commit-description-as-a-thinking-tool/">https://yedhu.me/posts/commit-description-as-a-thinking-tool/</a></p>
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=49911757">https://news.ycombinator.com/item?id=49911757</a></p>
<p>Points: 65</p>
<p># Comments: 28</p>

🔗 **Read more:** [https://yedhu.me/posts/commit-description-as-a-thinking-tool/](https://yedhu.me/posts/commit-description-as-a-thinking-tool/)

---

### 4. 'I pulled the controls': Passenger tells Israeli PM how he helped stop attacker

**Source:** BBC

**Category:** world

**Description:**
The man says he "pulled the controls" of the plane after it plummeted during the attack.

🔗 **Read more:** [https://www.bbc.co.uk/news/videos/c6rered722j5o?at_medium=RSS&at_campaign=rss](https://www.bbc.co.uk/news/videos/c6rered722j5o?at_medium=RSS&at_campaign=rss)

---

### 5. UK believes Iran involved in RAF Fairford incident, PM says

**Source:** BBC

**Category:** world

**Description:**
The prime minister's comments come days after the suspects were released on the 'strictest possible bail conditions'.

🔗 **Read more:** [https://www.bbc.co.uk/news/articles/cjwyz59k5y75o?at_medium=RSS&at_campaign=rss](https://www.bbc.co.uk/news/articles/cjwyz59k5y75o?at_medium=RSS&at_campaign=rss)

---

### 6. UK-France 'one in, one out' migrant scheme scrapped

**Source:** BBC

**Category:** world

**Description:**
Some 1,500 people have been removed to France since the scheme began just over a year ago.

🔗 **Read more:** [https://www.bbc.co.uk/news/articles/c64gvnv4eqylo?at_medium=RSS&at_campaign=rss](https://www.bbc.co.uk/news/articles/c64gvnv4eqylo?at_medium=RSS&at_campaign=rss)

---

### 7. A political dynasty? Why the Bolsonaro family dominates Brazil’s right wing

**Source:** Al Jazeera

**Category:** world

**Description:**
For a third election in a row, a Bolsonaro family member is the leading right-wing contender for Brazil&#039;s presidency.

🔗 **Read more:** [https://www.aljazeera.com/news/longform/2026/9/30/a-political-dynasty-why-the-bolsonaro-family-dominates-brazils-right-wing?traffic_source=rss](https://www.aljazeera.com/news/longform/2026/9/30/a-political-dynasty-why-the-bolsonaro-family-dominates-brazils-right-wing?traffic_source=rss)

---

### 8. Cristiano Ronaldo misses Portugal training as coach Jorge Jesus denies rift

**Source:** Al Jazeera

**Category:** world

**Description:**
Ronaldo did not play in Portugal’s 2-1 win over Norway ‌on Sunday and is now in doubt for the game against Denmark.

🔗 **Read more:** [https://www.aljazeera.com/sports/2026/9/30/cristiano-ronaldo-misses-portugal-training-as-coach-jorge-jesus-denies-rift?traffic_source=rss](https://www.aljazeera.com/sports/2026/9/30/cristiano-ronaldo-misses-portugal-training-as-coach-jorge-jesus-denies-rift?traffic_source=rss)

---

### 9. Video: Bangladesh Dengue deaths surpass 233 in deadly outbreak

**Source:** Al Jazeera

**Category:** world

**Description:**
Bangladesh’s health authorities report that at least 233 people have died from dengue fever.

🔗 **Read more:** [https://www.aljazeera.com/video/newsfeed/2026/9/30/video-bangladesh-dengue-deaths-surpass-233-in-deadly-outbreak?traffic_source=rss](https://www.aljazeera.com/video/newsfeed/2026/9/30/video-bangladesh-dengue-deaths-surpass-233-in-deadly-outbreak?traffic_source=rss)

---

### 10. Tropical Storm Hanna

**Source:** NASA

**Category:** nature

**Description:**
Natural event: Severe Storms

🔗 **Read more:** [https://eonet.gsfc.nasa.gov/api/v3/events/EONET_24909](https://eonet.gsfc.nasa.gov/api/v3/events/EONET_24909)

---

### 11. Hurricane Rachel

**Source:** NASA

**Category:** nature

**Description:**
Natural event: Severe Storms

🔗 **Read more:** [https://eonet.gsfc.nasa.gov/api/v3/events/EONET_24875](https://eonet.gsfc.nasa.gov/api/v3/events/EONET_24875)

---

### 12. Wildfire Rafter 4B, Schleicher, Texas

**Source:** NASA

**Category:** nature

**Description:**
Natural event: Wildfires

🔗 **Read more:** [https://eonet.gsfc.nasa.gov/api/v3/events/EONET_24904](https://eonet.gsfc.nasa.gov/api/v3/events/EONET_24904)

---


**Built with ❤️ by GitHub Actions**