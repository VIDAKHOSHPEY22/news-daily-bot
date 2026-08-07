# 📰 Daily News Bot - 48+ Commits Daily

**Last Update:** 2026-08-07 04:15:17

**Total News:** 12

**Sources:** BBC, Hacker News, Al Jazeera, NASA

---

## 📰 Latest News

### 1. Show HN: Whisper transcribes 70-year-olds more accurately than 20-year-olds

**Source:** Hacker News

**Category:** technology

**Description:**
<p>Article URL: <a href="https://github.com/Kayvan-Zahiri/asr-age-gap">https://github.com/Kayvan-Zahiri/asr-age-gap</a></p>
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=49204388">https://news.ycombinator.com/item?id=49204388</a></p>
<p>Points: 6</p>
<p># Comments: 1</p>

🔗 **Read more:** [https://github.com/Kayvan-Zahiri/asr-age-gap](https://github.com/Kayvan-Zahiri/asr-age-gap)

---

### 2. Meta Ordered to Pay $942M to Address Harm to Kids from Social Media

**Source:** Hacker News

**Category:** technology

**Description:**
<p>Article URL: <a href="https://www.wsj.com/tech/meta-ordered-to-pay-942-million-to-address-harm-to-kids-from-social-media-8ba5aab7">https://www.wsj.com/tech/meta-ordered-to-pay-942-million-to-address-harm-to-kids-from-social-media-8ba5aab7</a></p>
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=49204352">https://news.ycombinator.com/item?id=49204352</a></p>
<p>Points: 19</p>
<p># Comments: 3</p>

🔗 **Read more:** [https://www.wsj.com/tech/meta-ordered-to-pay-942-million-to-address-harm-to-kids-from-social-media-8ba5aab7](https://www.wsj.com/tech/meta-ordered-to-pay-942-million-to-address-harm-to-kids-from-social-media-8ba5aab7)

---

### 3. Spin audit of SQD/QSCI quantum-chemistry benchmarks on iron–sulfur clusters

**Source:** Hacker News

**Category:** technology

**Description:**
<p>Author here.<p>Background, for anyone who hasn't followed this fight: IBM's iron–sulfur SQD results (Sci. Adv. 2025) are one of the flagship "quantum computers are useful for chemistry now" claims, and a published critique (arXiv:2501.07231) argues the quantum samples never beat classical selected-CI at matched cost. That argument is still live.<p>Both sides have been arguing about energies. Neither measured which electronic state these calculations actually converge to.<p>So I measured it. ⟨S²⟩ comes out between 4.7 and 7.0 depending on the system and the subspace size, where the target these papers name is a singlet at ⟨S²⟩ = 0. Every starting guess I tried lands in the same place, and the error at convergence is about the size of the spin-state ladder itself, which <i>is</i> the physics under dispute.<p>IBM ships a mitigation for this. Run exactly as shipped, using their driver, their recovery loop and their own spin_square() diagnostic, it moves the ground energy by under a nanohartree while making the subspace 4.00x bigger: 194,481 determinants against 48,600. It makes a singlet representable. It never produces one. Their solver also takes a spin_sq argument that would target the singlet directly, and the default pipeline never sets it.<p>I filed that narrow part on their tracker yesterday, before posting this: <a href="https://github.com/Qiskit/qiskit-addon-sqd/issues/337" rel="nofollow">https://github.com/Qiskit/qiskit-addon-sqd/issues/337</a>. A maintainer answered and closed it the same day, and his answer is the useful part. The flag, in his words, augments the sampled subspace by using alpha CI strings as beta strings and vice versa. That is a statement about which determinants span the space, not about what spin the returned state comes out in, which is exactly what the measurement says. He did not contest the numbers. The second question, whether the default path is meant to reach spin_sq at all, is still unanswered.<p>The obvious objection is that this is all my own reimplementation, so here's the part that isn't. IBM's data-availability archive for the flagship paper contains the raw hardware measurement records: 2,457,600 shots on [2Fe-2S] from December 2023, 3,163,742 outcomes on [4Fe-4S] from April 2024, plus the integrals and the optimized circuit's parameters. Running their shots through their own pipeline, [2Fe-2S] reaches low ⟨S²⟩ but sits 248 mHa off their own reference, and [4Fe-4S] converges to a spin-pure triplet, Var(S²) = 3e-6, a genuine S=1 eigenstate: a clean state, and the wrong one, 1,438 mHa from their reference.<p>Two things in that archive need no analysis from me at all. Their uniform-random null control matches or beats the hardware samples in every published [2Fe-2S] comparison. And their largest [4Fe-4S] runs, at subspace dimension 10⁸, trail their own classical HCI file by 149 mHa.<p>On the AI angle, since that's half of why this is on HN: Claude did the initial audit end to end in about 72 hours under my direction, and it's been through many rounds of adversarial review since. The part I'd defend as actually interesting isn't the speed. It caught five defects in its own work through pre-registered validation gates, one of them by cross-checking against IBM's own published energy tables, and it retracted its own strongest pro-quantum finding when the new instrument showed that result was a spin-sector artifact. AUDIT_TRAIL.md has the timeline. REPRO_MAP.md maps every claim to a file and a command that regenerates it.<p>If you want to kill this, and I mean that, here's how. Exhibit any state in a spin-completed ground manifold of these benchmarks with ⟨S²⟩ < 1. Or show me a quantum-sampled subspace at matched determinant count whose spin-identified energy beats HCI or CIPSI. Or get any shipped-pipeline run on IBM's archived samples to land ⟨S²⟩ < 1 and error under 50 mHa at once, with no spin penalty. The harness is in the archive and I'll publish whatever comes back, including if it's me who's wrong.<p>Preprint: <a href="https://doi.org/10.26434/chemrxiv.15006382/v1" rel="nofollow">https://doi.org/10.26434/chemrxiv.15006382/v1</a><p>The limitations section is real: comparison dimensions are fixed, the [4Fe-4S] reference is approximate, and the 58.6M "samples" file is deduplicated, so the shot-level distribution of their optimal-circuit numerics isn't publicly auditable. It's short. Worth reading before the hot take.</p>
<hr />
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=49203707">https://news.ycombinator.com/item?id=49203707</a></p>
<p>Points: 5</p>
<p># Comments: 1</p>

🔗 **Read more:** [https://zenodo.org/records/21359923](https://zenodo.org/records/21359923)

---

### 4. Thousands of rail passengers hit by power failure disruption

**Source:** BBC

**Category:** world

**Description:**
An outage in Manchester caused delays and cancellations, with services expected to be affected throughout the evening.

🔗 **Read more:** [https://www.bbc.co.uk/news/articles/cn5nlvdxpwpo?at_medium=RSS&at_campaign=rss](https://www.bbc.co.uk/news/articles/cn5nlvdxpwpo?at_medium=RSS&at_campaign=rss)

---

### 5. Uefa says boycott may still go ahead as FA withdraws Infantino support

**Source:** BBC

**Category:** world

**Description:**
Fifa's backing of president Gianni Infantino at a meeting on Wednesday "changes nothing", says European governing body Uefa.

🔗 **Read more:** [https://www.bbc.co.uk/sport/football/articles/c2k74yevgzwo?at_medium=RSS&at_campaign=rss](https://www.bbc.co.uk/sport/football/articles/c2k74yevgzwo?at_medium=RSS&at_campaign=rss)

---

### 6. Meta fined $567m in largest child safety ruling against social media giant

**Source:** BBC

**Category:** world

**Description:**
A New Mexico judge ordered the Instagram, Facebook and Whatsapp parent company to pay another $567m for the way it has harmed children.

🔗 **Read more:** [https://www.bbc.co.uk/news/articles/cd7lz3wr2rlo?at_medium=RSS&at_campaign=rss](https://www.bbc.co.uk/news/articles/cd7lz3wr2rlo?at_medium=RSS&at_campaign=rss)

---

### 7. After the floods, hunger: Mozambique’s second disaster

**Source:** Al Jazeera

**Category:** world

**Description:**
Lost harvests and disrupted supply routes have pushed many families deeper into food insecurity.

🔗 **Read more:** [https://www.aljazeera.com/news/2026/8/7/after-the-floods-hunger-mozambiques-second-disaster?traffic_source=rss](https://www.aljazeera.com/news/2026/8/7/after-the-floods-hunger-mozambiques-second-disaster?traffic_source=rss)

---

### 8. Trump says war can’t ‘go much longer’, Hormuz deal close

**Source:** Al Jazeera

**Category:** world

**Description:**
The US, Iran, and Oman are close to a temporary deal to reopen the Strait of Hormuz

🔗 **Read more:** [https://www.aljazeera.com/news/liveblog/2026/8/7/trump-says-war-cant-go-much-longer-hormuz-deal-close?traffic_source=rss](https://www.aljazeera.com/news/liveblog/2026/8/7/trump-says-war-cant-go-much-longer-hormuz-deal-close?traffic_source=rss)

---

### 9. Travel restrictions – from Israel and Europe – trap students in Gaza

**Source:** Al Jazeera

**Category:** world

**Description:**
Blockades and bureaucracy turn education into an uphill journey for talented Gaza students seeking a brighter future.

🔗 **Read more:** [https://www.aljazeera.com/features/2026/8/6/travel-restrictions-from-israel-and-europe-trap-students-in-gaza?traffic_source=rss](https://www.aljazeera.com/features/2026/8/6/travel-restrictions-from-israel-and-europe-trap-students-in-gaza?traffic_source=rss)

---

### 10. Wildfire Wrights Spring, Klamath, Oregon

**Source:** NASA

**Category:** nature

**Description:**
Natural event: Wildfires

🔗 **Read more:** [https://eonet.gsfc.nasa.gov/api/v3/events/EONET_22196](https://eonet.gsfc.nasa.gov/api/v3/events/EONET_22196)

---

### 11. Wildfire BUZZARD, Kern, California

**Source:** NASA

**Category:** nature

**Description:**
Natural event: Wildfires

🔗 **Read more:** [https://eonet.gsfc.nasa.gov/api/v3/events/EONET_22195](https://eonet.gsfc.nasa.gov/api/v3/events/EONET_22195)

---

### 12. Wildfire Bare, Sublette, Wyoming

**Source:** NASA

**Category:** nature

**Description:**
Natural event: Wildfires

🔗 **Read more:** [https://eonet.gsfc.nasa.gov/api/v3/events/EONET_22197](https://eonet.gsfc.nasa.gov/api/v3/events/EONET_22197)

---


**Built with ❤️ by GitHub Actions**