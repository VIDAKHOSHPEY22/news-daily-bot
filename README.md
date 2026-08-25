# 📰 Daily News Bot - 48+ Commits Daily

**Last Update:** 2026-08-26 03:01:13

**Total News:** 12

**Sources:** NASA, Al Jazeera, BBC, Hacker News

---

## 📰 Latest News

### 1. Show HN: TeXbrain, a LaTeX editor that runs pdfTeX in the browser via WASM

**Source:** Hacker News

**Category:** technology

**Description:**
<p>I'm a master's engineering student and a big fan of LaTeX, which I used for my thesis and research articles. I have used Overleaf and that was fine until I wanted to git sync, which unfortunately sits behind a paywall. Since I didn't want to pay subscriptions for things that should simply just work, I built the editor I wanted in my free time, where you open a tab, write LaTeX, get your PDF and the files stay all in one folder on my disk.<p>TeXbrain is a static site with no backend. pdfTeX is compiled to WebAssembly (SwiftLaTeX) and runs in your browser. The editor can read and write your project folder through the File System Access API, so you can use git, any local TeX install, local AI Agents, or any other editor on the same files. Git is built in through isomorphic-git for anyone who would rather not touch a terminal and clone, branch, commit, push or pull via commands. No account is needed, no analytics, and everything works offline after the first load.<p>Try it out: <a href="https://tex.swimmingbrain.dev/" rel="nofollow">https://tex.swimmingbrain.dev/</a> (Chromium browsers get direct folder access, while Firefox or Safari fall back to a virtual filesystem)<p>Or for self-hosting/contributing: <a href="https://github.com/swimmingbrain/texbrain" rel="nofollow">https://github.com/swimmingbrain/texbrain</a> (MIT, the pdfTeX engine is EPL 2.0 / GPL 2.0 and is listed in the THIRD_PARTY_LICENSES file).<p>The part I'm most proud of getting to work is the package loading. The engine itself is only 1.8 MB. When it asks for a file it doesn't have, then a service worker intercepts the request and resolves it through Cache Storage first, then a small bundled subset, then a TeX Live tree mirrored on jsDelivr, then a SwiftLaTeX style server as a last resort. Every file is fetched once at most and after the first successful compilation, the core subset is prefetched in the background so that the offline story actually holds. Only file names go over the network, never any document content.<p>So far, it only supports pdfTeX (no XeTeX or LuaTeX), so fontspec or polyglossia won't work, packages are pinned to the TeX Live 2020 era to stay coherent with the engine's format file and there is no bibtex or biber in the engine yet, which is maybe the roughest edge.<p>This is should be a good solution for people on a work laptop, a Chromebook, or a university lab PC where installing TeX Live isn't always an option, and people who don't want to maintain a TeX install at all. If you already have a local setup you like, keep it. This isn't necessarily thought as a replacement for that.<p>Some people have already used it for their thesis in the past months and their bug reports (which I would never have hit on my own) were then most of the summer's work. The first outside PR also landed recently, so if something doesn't compile for you, an issue with the package name or the bug itself is the most useful thing you can send me!</p>
<hr />
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=49441375">https://news.ycombinator.com/item?id=49441375</a></p>
<p>Points: 16</p>
<p># Comments: 2</p>

🔗 **Read more:** [https://github.com/swimmingbrain/texbrain](https://github.com/swimmingbrain/texbrain)

---

### 2. Python's pre-declared constants are kinda weird

**Source:** Hacker News

**Category:** technology

**Description:**
<p>Article URL: <a href="https://sebsite.pw/w/20260801-pythonconstants.html">https://sebsite.pw/w/20260801-pythonconstants.html</a></p>
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=49441033">https://news.ycombinator.com/item?id=49441033</a></p>
<p>Points: 80</p>
<p># Comments: 26</p>

🔗 **Read more:** [https://sebsite.pw/w/20260801-pythonconstants.html](https://sebsite.pw/w/20260801-pythonconstants.html)

---

### 3. XCancel also down, at least for time being

**Source:** Hacker News

**Category:** technology

**Description:**
<p>Message on xcancel website:<p>"On Monday 24th August at 8PM EST, we received at letter from X Corp. asking to cease and desist the service XCancel.
The service XCancel is stopped until further notice.
We are seeking legal advice and won't share more details for now.
Thank you for the trust you have put in these two years of XCancel."<p>https://xcancel.com/</p>
<hr />
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=49440786">https://news.ycombinator.com/item?id=49440786</a></p>
<p>Points: 113</p>
<p># Comments: 22</p>

🔗 **Read more:** [https://news.ycombinator.com/item?id=49440786](https://news.ycombinator.com/item?id=49440786)

---

### 4. Dolly Parton: The life of an iconic country singer

**Source:** BBC

**Category:** world

**Description:**
Iconic country musician Dolly Parton has died at the age of 80, the singer's team announced on social media.

🔗 **Read more:** [https://www.bbc.co.uk/news/videos/c7831ld8e73o?at_medium=RSS&at_campaign=rss](https://www.bbc.co.uk/news/videos/c7831ld8e73o?at_medium=RSS&at_campaign=rss)

---

### 5. Father's house rammed before son died in A66 crash

**Source:** BBC

**Category:** world

**Description:**
The house belonging to Cole Worthy's father is significantly damaged and its windows are smashed.

🔗 **Read more:** [https://www.bbc.co.uk/news/articles/cevwjww8p08o?at_medium=RSS&at_campaign=rss](https://www.bbc.co.uk/news/articles/cevwjww8p08o?at_medium=RSS&at_campaign=rss)

---

### 6. CIA chief travels to Moscow for unannounced talks, US media reports

**Source:** BBC

**Category:** world

**Description:**
Flight tracking data confirms an American military aircraft travelled to Russia from the US via Latvia on Tuesday.

🔗 **Read more:** [https://www.bbc.co.uk/news/articles/c87vg9x5d7do?at_medium=RSS&at_campaign=rss](https://www.bbc.co.uk/news/articles/c87vg9x5d7do?at_medium=RSS&at_campaign=rss)

---

### 7. Brazil fines TikTok $30m for child data privacy violations

**Source:** Al Jazeera

**Category:** world

**Description:**
Owner ByteDance ordered to erase illegally obtained child data in Brazil as crackdown on tech giants intensifies.

🔗 **Read more:** [https://www.aljazeera.com/news/2026/8/25/brazil-fines-tiktok-30m-for-child-data-privacy-violations?traffic_source=rss](https://www.aljazeera.com/news/2026/8/25/brazil-fines-tiktok-30m-for-child-data-privacy-violations?traffic_source=rss)

---

### 8. Why can’t America agree on what time it is?

**Source:** Al Jazeera

**Category:** world

**Description:**
Why can’t America agree on what time it is?

🔗 **Read more:** [https://www.aljazeera.com/video/newsfeed/2026/8/25/why-cant-america-agree-on-what-time-it-is?traffic_source=rss](https://www.aljazeera.com/video/newsfeed/2026/8/25/why-cant-america-agree-on-what-time-it-is?traffic_source=rss)

---

### 9. US judge blocks Ohio law requiring proof of citizenship to register to vote

**Source:** Al Jazeera

**Category:** world

**Description:**
The amended law was an attempt by state Republicans to crack down on unproven claims of voting by noncitizens.

🔗 **Read more:** [https://www.aljazeera.com/news/2026/8/25/us-judge-blocks-ohio-law-requiring-proof-of-citizenship-to-register-to-vote?traffic_source=rss](https://www.aljazeera.com/news/2026/8/25/us-judge-blocks-ohio-law-requiring-proof-of-citizenship-to-register-to-vote?traffic_source=rss)

---

### 10. Tropical Storm Julio

**Source:** NASA

**Category:** nature

**Description:**
Natural event: Severe Storms

🔗 **Read more:** [https://eonet.gsfc.nasa.gov/api/v3/events/EONET_23286](https://eonet.gsfc.nasa.gov/api/v3/events/EONET_23286)

---

### 11. Wildfire Old Deer, Carson, Texas

**Source:** NASA

**Category:** nature

**Description:**
Natural event: Wildfires

🔗 **Read more:** [https://eonet.gsfc.nasa.gov/api/v3/events/EONET_23209](https://eonet.gsfc.nasa.gov/api/v3/events/EONET_23209)

---

### 12. Wildfire 22, Miami-Dade, Florida

**Source:** NASA

**Category:** nature

**Description:**
Natural event: Wildfires

🔗 **Read more:** [https://eonet.gsfc.nasa.gov/api/v3/events/EONET_23225](https://eonet.gsfc.nasa.gov/api/v3/events/EONET_23225)

---


**Built with ❤️ by GitHub Actions**