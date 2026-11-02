# 📰 Daily News Bot - 48+ Commits Daily

**Last Update:** 2026-11-02 22:04:21

**Total News:** 12

**Sources:** Al Jazeera, NASA, BBC, Hacker News

---

## 📰 Latest News

### 1. Show HN: Subvocal – Talk to your computer without making noise

**Source:** Hacker News

**Category:** technology

**Description:**
<p>Hi HN, we're Aarush and Arnav from The Subvocal Company (YC F26). We’re building smart glasses that let you talk to your computer without talking out loud. You can mouth words silently and discreetly and the glasses decode them to text at the speed of speech.<p>Here's a video of Dave from YC trying it out: <a href="https://www.youtube.com/watch?v=9QdX1eObVYI" rel="nofollow">https://www.youtube.com/watch?v=9QdX1eObVYI</a><p>(Edit: you don't actually have to move your lips or even open your mouth for this to work! Since the RF can see inside your mouth the system can be fine tuned on "internal speech". This isn't the automatic tongue movements that occur when "thinking" words to yourself, but more like mouthing with your lips closed. We don't often lead with this since it's weird for many people to do, but with a bit of practice, we have been able to get it down pretty well.)<p>Arnav and I were studying CS at Georgia Tech at the beginning of the year, with no experience in silent speech or sensing. We were both AI-native builders and power users of Wispr Flow. What bugged us was not being able to use these tools in the library (or an office) or in public. At Stanford’s TreeHacks in February, we decided to build the most technically ridiculous thing we could think of. We’d read about AlterEgo, a silent speech system out of MIT’s Media Lab, and wanted to recreate it in 36 hours. We built a crude prototype, sticking EMG electrodes onto my face:<p><a href="https://drive.google.com/file/d/1mwhv5HZMz3UTevdrgwS5O7g2jWV0K9r2/view?usp=sharing" rel="nofollow">https://drive.google.com/file/d/1mwhv5HZMz3UTevdrgwS5O7g2jWV...</a><p>We got it to kind of work at a letter level in a very janky way. It wasn’t good enough to win the hackathon, but convinced us to go all in. The first time I typed a sentence without anyone noticing, I felt the magic of the technology.<p>We quickly realized EMG (reading muscle electrical signals) wouldn’t work:<p>- Signal changes due to sweat<p>- Electrical interference<p>- Placement variability<p>- Most importantly, no one wants to stick electrodes onto their face!!<p>So we switched to RF and built the glasses you see now. They emit radio waves, similar to Bluetooth, that pass through your face. As they cross the tongue, lips and soft palate, they’re modulated by silent mouthing. We train foundation models on this data to decode these perturbations to text.<p>Despite prior academic research, getting this to work was a huge engineering challenge. First we built an extremely low noise RF sensing stack. Then we had to place antennas so their fields overlapped maximally with the articulators. Our first attempt on glasses failed completely, so we reverted to old habits and taped antennas on our face:<p><a href="https://drive.google.com/file/d/1ks0dS0eZiTV9EqSFsyB_w5BBjpcBAfX-/view?usp=sharing" rel="nofollow">https://drive.google.com/file/d/1ks0dS0eZiTV9EqSFsyB_w5BBjpc...</a><p>Since taping antennas consistently in the same spot and angle was hard, we created this weird but effective head rig to hold them in place:<p><a href="https://drive.google.com/file/d/1rhzNFpdDzr7oHk0isFY70dkoV4CAF1pT/view?usp=sharing" rel="nofollow">https://drive.google.com/file/d/1rhzNFpdDzr7oHk0isFY70dkoV4C...</a><p>This worked, but obviously wasn’t a product yet. So we worked deep in simulations to design glasses that could hold the antennas.<p>That evolved into our design now, with antennas embedded within the frames. Once we established there was a signal, the next hurdle was cross-user generalization. Everyone’s facial anatomy, and hence RF signal patterns, are vastly different. We tried algorithmic workarounds but realized the only lever was to massively scale pretraining data.<p>So that’s what we did. We set up booths in our office and paid people to read prompts wearing our glasses, to pretrain our models on. This produced a beautiful scaling curve, with errors falling quickly as we scaled our dataset and cross-user performance becoming genuinely compelling (as you see in the video above; Dave only had a short 20-sentence calibration).<p>We always heard about building things from first principles but never understood it before this. We tried tackling it top down but completely failed. Only when we broke each component (the antenna, electronics, ML) down to its fundamentals to understand and optimize it did we get it to work really well.<p>Over the next few months we’re continuing R&amp;D to turn our prototype glasses into the slick product on our website and ship in Q1 2027. We’re also scaling up our dataset to improve performance on edge cases.<p>For anyone who loves voice dictation but hates using it around people, we’ve opened preorders for our first batch of 500 units, with a $200 discount off the final price. Allocation is running out quickly, so get yours at <a href="https://subvocal.co/preorder" rel="nofollow">https://subvocal.co/preorder</a>!</p>
<hr />
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=50340088">https://news.ycombinator.com/item?id=50340088</a></p>
<p>Points: 125</p>
<p># Comments: 96</p>

🔗 **Read more:** [https://subvocal.company/](https://subvocal.company/)

---

### 2. Launch HN: Momentic (YC W24) – Agents that catch bugs by using your app

**Source:** Hacker News

**Category:** technology

**Description:**
<p>Hey HN, we’re Wei-Wei and Jeff. We’re building Momentic, QA agents that autonomously plan, explore, and bug-bash controls and user flows in your web, iOS, Android, and (soon) desktop apps to catch bugs.<p>Here’s a demo: <a href="https://youtu.be/BFsM-Se1Fh8" rel="nofollow">https://youtu.be/BFsM-Se1Fh8</a><p>We’re both software engineers that spent our careers on dev tooling and infra across companies like Robinhood, Retool, WeWork, and Qualtrics. Testing was always a pain in the ass (esp Playwright and Selenium), so we built agents to do it for us.<p>Modern day software has a ton of bugs and the change failure rate is only growing faster as coding agent adoption scales. LLMs are really good at generating code, but reinforce their own assumptions, write a ton of useless tests, and are bad at visual understanding. On DeepSWE v1.1, Sonnet 5.5 hit 66.2% pass rate when banned from writing tests, versus 65.3% when allowed.<p>OSS end-to-end testing frameworks like Playwright, Selenium, or Maestro force you to hardcode implementation details like XPath, text, or aria-* attributes in your tests. Even with agents, these take a nontrivial amount of time and tokens to build and maintain.<p>In 2023, we saw Nat Friedman drive a browser with GPT-3 via natbot. We were inspired to use this technology to automate the most painful and tedious parts of software engineering: testing. We started with using LLMs to generate and maintain Playwright, but quickly realized that those primitives were fundamentally misaligned with the agentic SDLC. We think the future of QA is agents testing themselves, not writing scripts.<p>Mo is a custom agent harness for catching bugs that builds on the past 3 years of Momentic and millions of test traces from complex, real-world applications. Mo is built for recall: it finds the most real bugs, though Codex is a bit more precise at 86% vs 84%. The tradeoff is cost: Mo costs $2.67 per bug vs $0.80 for Codex, less than Claude Code and Devin.<p>- Self-organizing agent graph. Mo builds a directed acyclic graph (DAG) as it explores. Large product areas automatically fork into parallel sub-agents, each with their own browser or device for concurrent execution.<p>- Specialized agents for domain specific tasks. Planner agents reason over screenshots and video while dedicated locator agents inspect page structure to resolve plain-English interaction targets. Others include image analysis, video understanding, audio generation, and more.<p>- Parallel agents coordinate through cooperative resource leases. Agents can announce that they’re “using” or “modifying” overlapping resources or fixtures. Multiple “using” claims can coexist, but only a single “modifying” claim can be active on any particular one.<p>- Scaled infrastructure. Mo ships with a tunnel that lets users expose private sites and local apps to our hosted agents and infra. A single bug bash can spin up 100s of concurrent browsers and devices.<p>We benchmarked Mo against coding agents on 4 popular open-source apps: Gitea (58.8k stars), Metabase, Twenty (YC), and Saleor, with 1,396 human-labeled bugs. Each agent got the same brief, a fresh E2B sandbox, and no access to source code. Codex and Claude Code used hosted Browserbase browsers, while Devin used its built-in browser. For evaluators, we implemented LLM as a judge (GPT-6.1 Sol) with a human reviewer.<p>Results from a time-boxed 60-minute run:<p>- Mo: 269 bugs, 19.3% recall, 84% precision, $2.67 per bug<p>- Codex (GPT-6.1 Sol + Playwright MCP): 86 bugs, 6.2% recall, 86% precision, $0.80 per bug<p>- Claude Code (Opus 5.5 + Playwright MCP): 59 bugs, 4.2% recall, 80% precision, $4.09 per bug<p>- Devin: 27 bugs, 1.9% recall, 84% precision, $3.89 per bug<p>Mo finds more bugs the more time it has. From 30 to 60 minutes, it went from 177 to 269 bugs (+52%), while Codex gained only 16%.<p>Results: <a href="https://momentic.ai/qa-bench">https://momentic.ai/qa-bench</a><p>Write-up: <a href="https://momentic.ai/blog/qa-bench">https://momentic.ai/blog/qa-bench</a><p>Dataset: <a href="https://huggingface.co/datasets/momentic/qa-bench" rel="nofollow">https://huggingface.co/datasets/momentic/qa-bench</a><p>Harness: <a href="https://github.com/momentic-ai/qa-bench" rel="nofollow">https://github.com/momentic-ai/qa-bench</a><p>We just shipped PR testing for Vercel and Cloudflare deploy previews and we’re giving every new signup $250 in Mo spend. Paid plans have higher infra capacity and included usage along with options to top up.<p>We’d love for you to try it out and give us feedback. Feel free to comment here, we’ll be around all day!</p>
<hr />
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=50339913">https://news.ycombinator.com/item?id=50339913</a></p>
<p>Points: 47</p>
<p># Comments: 29</p>

🔗 **Read more:** [https://momentic.ai/](https://momentic.ai/)

---

### 3. Bitmovin (YC S15) Is Hiring Technical Graduates in Denver (Engineering/CS Focus)

**Source:** Hacker News

**Category:** technology

**Description:**
<p>Article URL: <a href="https://bitmovin.com/careers/8660599002/">https://bitmovin.com/careers/8660599002/</a></p>
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=50339827">https://news.ycombinator.com/item?id=50339827</a></p>
<p>Points: 0</p>
<p># Comments: 0</p>

🔗 **Read more:** [https://bitmovin.com/careers/8660599002/](https://bitmovin.com/careers/8660599002/)

---

### 4. Shop freezers in seven European countries hit by cyber-attack

**Source:** BBC

**Category:** world

**Description:**
The temperature of freezers in several shops across Europe reportedly rose to as high as 50C.

🔗 **Read more:** [https://www.bbc.co.uk/news/articles/cq1kd1nee80eo?at_medium=RSS&at_campaign=rss](https://www.bbc.co.uk/news/articles/cq1kd1nee80eo?at_medium=RSS&at_campaign=rss)

---

### 5. 'All this food is now useless': Piles of rubbish after shop freezers hit by cyber-attack

**Source:** BBC

**Category:** world

**Description:**
Dozens of supermarkets in seven European countries dumped huge quantities of food after refrigerators and freezers were targeted in a cyber-attack.

🔗 **Read more:** [https://www.bbc.co.uk/news/videos/cmwyvrgk9p0ro?at_medium=RSS&at_campaign=rss](https://www.bbc.co.uk/news/videos/cmwyvrgk9p0ro?at_medium=RSS&at_campaign=rss)

---

### 6. Channel 4 documentary and journalists 'poisoned the well' against Russell Brand, court hears

**Source:** BBC

**Category:** world

**Description:**
Brand's defence barrister told jurors that Brand "had an immense amount of sex", but that "none of it was unlawful".

🔗 **Read more:** [https://www.bbc.co.uk/news/articles/cwkg5dnypdn4o?at_medium=RSS&at_campaign=rss](https://www.bbc.co.uk/news/articles/cwkg5dnypdn4o?at_medium=RSS&at_campaign=rss)

---

### 7. Judge dismisses charges against FBI agents involved in Hunter Biden case

**Source:** Al Jazeera

**Category:** world

**Description:**
A federal judge tossed charges accusing two former FBI officials of lying to Congress about Hunter Biden investigation.

🔗 **Read more:** [https://www.aljazeera.com/news/2026/11/2/judge-dismisses-charges-against-fbi-agents-involved-in-hunter-biden-case?traffic_source=rss](https://www.aljazeera.com/news/2026/11/2/judge-dismisses-charges-against-fbi-agents-involved-in-hunter-biden-case?traffic_source=rss)

---

### 8. British adventurer Karl Bushby returns home after 28-year walk around world

**Source:** Al Jazeera

**Category:** world

**Description:**
The 57-year-old crossed jungles and frozen seas before an emotional homecoming in Hull, northern England.

🔗 **Read more:** [https://www.aljazeera.com/news/2026/11/2/british-adventurer-karl-bushby-returns-home-after-28-year-walk-around-world?traffic_source=rss](https://www.aljazeera.com/news/2026/11/2/british-adventurer-karl-bushby-returns-home-after-28-year-walk-around-world?traffic_source=rss)

---

### 9. Drone attacks extend campaign targeting Sudan’s power system

**Source:** Al Jazeera

**Category:** world

**Description:**
Attacks the latest to disrupt electricity supplies; army reports new defections from paramilitary RSF.

🔗 **Read more:** [https://www.aljazeera.com/news/2026/11/2/drone-attacks-extend-campaign-targeting-sudans-power-system?traffic_source=rss](https://www.aljazeera.com/news/2026/11/2/drone-attacks-extend-campaign-targeting-sudans-power-system?traffic_source=rss)

---

### 10. Tropical Cyclone Murasu

**Source:** NASA

**Category:** nature

**Description:**
Natural event: Severe Storms

🔗 **Read more:** [https://eonet.gsfc.nasa.gov/api/v3/events/EONET_25964](https://eonet.gsfc.nasa.gov/api/v3/events/EONET_25964)

---

### 11. Prescribed Fire Dry Lake Hills Piles RX, Coconino, Arizona

**Source:** NASA

**Category:** nature

**Description:**
Natural event: Wildfires

🔗 **Read more:** [https://eonet.gsfc.nasa.gov/api/v3/events/EONET_25984](https://eonet.gsfc.nasa.gov/api/v3/events/EONET_25984)

---

### 12. Prescribed Fire McCarty Piles RX, Coconino, Arizona

**Source:** NASA

**Category:** nature

**Description:**
Natural event: Wildfires

🔗 **Read more:** [https://eonet.gsfc.nasa.gov/api/v3/events/EONET_25986](https://eonet.gsfc.nasa.gov/api/v3/events/EONET_25986)

---


**Built with ❤️ by GitHub Actions**