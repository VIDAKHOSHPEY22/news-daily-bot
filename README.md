# 📰 Daily News Bot - 48+ Commits Daily

**Last Update:** 2026-09-30 21:52:04

**Total News:** 12

**Sources:** Hacker News, BBC, Al Jazeera, NASA

---

## 📰 Latest News

### 1. Launch HN: Magnitude (YC S25) – Self-optimizing inference engine for agents

**Source:** Hacker News

**Category:** technology

**Description:**
<p>Hey HN, Anders and Tom here. We're building Magnitude, an inference engine for agents that optimizes itself to run as fast as possible on your hardware. It works on Mac, Linux, and Windows on any hardware and is up to 2x faster than llama.cpp.<p>We're both software engineers and previously built an open source browser agent to 4k+ GH stars and 100k+ downloads. We increasingly wanted to run it on local models, but found that no inference engine worked for our use case.<p>Inference engines today all make a performance tradeoff. They are either:<p>- Built for batched inference on datacenter hardware at the cost of single-session performance (vLLM, SGLang)
- Designed for broad compatibility instead of optimizing for specific hardware (llama.cpp, Ollama)
- Specialized for specific hardware or models but lacking engine completeness (oMLX, ds4)<p>Plus none of them are designed for running agents locally. Sessions are long, several often run at once, and you still want to use your computer for other things.<p>Magnitude is built for maximum performance on your hardware and running local agents:<p>- On-device compilation and tuning: Kernels are written with flexible parameters that are tuned on your actual device before the model runs. This gives you broad hardware compatibility with the same performance ceiling as hardware-specific kernels.
- Focus on best architectures: We write our tunable, highly efficient kernels for the most popular open-weights families. This allows us to achieve and surpass the performance of hardware or model specialized engines, without forcing ourselves to over-generalize at the cost of performance.
- Dynamic memory allocation: Magnitude reserves only enough memory up front to hold model weights. As your agent sessions grow, the memory heap dynamically increases, and frees itself when agents stop. Your hardware can still be used for other stuff while agents run.
- Hybrid paged attention: We borrow the best ideas from engines like SGLang to allow concurrent sessions to share prefix caches, but optimize placement for memory-adjacency so single-session performance doesn't suffer.<p>Magnitude is fully open source (Apache 2.0). We built it in Rust, including a custom GPU kernel runtime and autotuner. We take inspiration from the best innovations in inference from academics (e.g. FlashAttention, FlashInfer, TurboQuant) as well as other engines (e.g. SGLang radix attention) to reach the performance ceiling.<p>Benchmarked against llama.cpp with Qwen 3.6 35B A3B (4 bit), 64k context, no speculative decoding:<p>Metal (Mac M4 Pro 48 GB)
- 92% faster decode (30 tok/s → 57 tok/s)
- 9% faster prefill (466 tok/s → 507 tok/s)
- 28% less per-agent memory usage<p>CUDA (DGX Spark)
- 19% faster decode (49 tok/s → 58 tok/s)
- 23% faster prefill (2,033 tok/s → 2,507 tok/s)
- 27% less per-agent memory usage<p>Magnitude ships as a desktop app that you can easily connect with whatever agents you already use (Pi, OpenCode, Hermes, Codex, and more). It automatically runs models on demand when these agents actually need them, and shuts them down after inactivity.
Here's what it looks like: <a href="https://www.youtube.com/watch?v=0qE8BWEZu7o" rel="nofollow">https://www.youtube.com/watch?v=0qE8BWEZu7o</a><p>We're excited to push Magnitude further to let you run bigger models on the same hardware while continuing to improve performance. Our plans include:<p>- Expert streaming: store experts on RAM or disk and load them just-in-time. This lets you run models bigger than what otherwise would fit on your GPU.
- Kernel compiler: our current kernels tune a few parameters to fit your hardware. We can take this further with a fully custom compiler that automatically chooses how to fuse kernels and which implementations to use, to make it fit to your hardware even better.
- Multi-device utilization: Make the best possible use of all hardware on a system (CPU, GPUs, RAM, disk) by detecting these and automatically solving for the best model layout.<p>We'd love for more people to try it out and give us feedback. Feel free to comment here, we'll be around all day!</p>
<hr />
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=49911995">https://news.ycombinator.com/item?id=49911995</a></p>
<p>Points: 35</p>
<p># Comments: 13</p>

🔗 **Read more:** [https://github.com/magnitudedev/magnitude](https://github.com/magnitudedev/magnitude)

---

### 2. Commit Description as a Thinking Tool

**Source:** Hacker News

**Category:** technology

**Description:**
<p>Article URL: <a href="https://yedhu.me/posts/commit-description-as-a-thinking-tool/">https://yedhu.me/posts/commit-description-as-a-thinking-tool/</a></p>
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=49911757">https://news.ycombinator.com/item?id=49911757</a></p>
<p>Points: 37</p>
<p># Comments: 5</p>

🔗 **Read more:** [https://yedhu.me/posts/commit-description-as-a-thinking-tool/](https://yedhu.me/posts/commit-description-as-a-thinking-tool/)

---

### 3. Bild AI (YC W25) Is Hiring a Founding Product Engineer

**Source:** Hacker News

**Category:** technology

**Description:**
<p>Article URL: <a href="https://www.ycombinator.com/companies/bild-ai/jobs/dAbC3Gd-founding-product-engineer">https://www.ycombinator.com/companies/bild-ai/jobs/dAbC3Gd-founding-product-engineer</a></p>
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=49911531">https://news.ycombinator.com/item?id=49911531</a></p>
<p>Points: 0</p>
<p># Comments: 0</p>

🔗 **Read more:** [https://www.ycombinator.com/companies/bild-ai/jobs/dAbC3Gd-founding-product-engineer](https://www.ycombinator.com/companies/bild-ai/jobs/dAbC3Gd-founding-product-engineer)

---

### 4. 'We removed him from the cockpit': People speak about what happened

**Source:** BBC

**Category:** world

**Description:**
Passengers on the Flydubai flight bound for Israel filmed the moments following the stabbing.

🔗 **Read more:** [https://www.bbc.co.uk/news/videos/cv70d22kd34do?at_medium=RSS&at_campaign=rss](https://www.bbc.co.uk/news/videos/cv70d22kd34do?at_medium=RSS&at_campaign=rss)

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

### 7. Trump set to announce $200bn in energy investments from South Korea

**Source:** Al Jazeera

**Category:** world

**Description:**
The investments come as Trump seeks to tout the Republican Party&#039;s economic record ahead of the US midterm races.

🔗 **Read more:** [https://www.aljazeera.com/economy/2026/9/30/trump-set-to-announce-200bn-in-energy-investments-from-south-korea?traffic_source=rss](https://www.aljazeera.com/economy/2026/9/30/trump-set-to-announce-200bn-in-energy-investments-from-south-korea?traffic_source=rss)

---

### 8. Why is Malaysia sending back Rohingya refugees to Myanmar?

**Source:** Al Jazeera

**Category:** world

**Description:**
Kuala Lumpur calls it a voluntary process, but many are raising safety concerns.

🔗 **Read more:** [https://www.aljazeera.com/video/inside-story/2026/9/30/why-is-malaysia-sending-back-rohingya-refugees-to-myanmar?traffic_source=rss](https://www.aljazeera.com/video/inside-story/2026/9/30/why-is-malaysia-sending-back-rohingya-refugees-to-myanmar?traffic_source=rss)

---

### 9. Syria removed from US arms export ban list

**Source:** Al Jazeera

**Category:** world

**Description:**
US has gradually loosened restrictions placed on Syria during the Assad era to aid country&#039;s recovery from conflict.

🔗 **Read more:** [https://www.aljazeera.com/news/2026/9/30/syria-removed-from-us-arms-export-ban-list?traffic_source=rss](https://www.aljazeera.com/news/2026/9/30/syria-removed-from-us-arms-export-ban-list?traffic_source=rss)

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