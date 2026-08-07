# 📰 Daily News Bot - 48+ Commits Daily

**Last Update:** 2026-08-07 03:40:36

**Total News:** 12

**Sources:** BBC, NASA, Hacker News, Al Jazeera

---

## 📰 Latest News

### 1. Spin audit of SQD/QSCI quantum-chemistry benchmarks on iron–sulfur clusters

**Source:** Hacker News

**Category:** technology

**Description:**
<p>Author here.<p>Background, for anyone who hasn't followed this fight: IBM's iron–sulfur SQD results (Sci. Adv. 2025) are one of the flagship "quantum computers are useful for chemistry now" claims, and a published critique (arXiv:2501.07231) argues the quantum samples never beat classical selected-CI at matched cost. That argument is still live.<p>Both sides have been arguing about energies. Neither measured which electronic state these calculations actually converge to.<p>So I measured it. ⟨S²⟩ comes out between 4.7 and 7.0 depending on the system and the subspace size, where the target these papers name is a singlet at ⟨S²⟩ = 0. Every starting guess I tried lands in the same place, and the error at convergence is about the size of the spin-state ladder itself, which <i>is</i> the physics under dispute.<p>IBM ships a mitigation for this. Run exactly as shipped, using their driver, their recovery loop and their own spin_square() diagnostic, it moves the ground energy by under a nanohartree while making the subspace 4.00x bigger: 194,481 determinants against 48,600. It makes a singlet representable. It never produces one. Their solver also takes a spin_sq argument that would target the singlet directly, and the default pipeline never sets it.<p>I filed that narrow part on their tracker yesterday, before posting this: <a href="https://github.com/Qiskit/qiskit-addon-sqd/issues/337" rel="nofollow">https://github.com/Qiskit/qiskit-addon-sqd/issues/337</a>. A maintainer answered and closed it the same day, and his answer is the useful part. The flag, in his words, augments the sampled subspace by using alpha CI strings as beta strings and vice versa. That is a statement about which determinants span the space, not about what spin the returned state comes out in, which is exactly what the measurement says. He did not contest the numbers. The second question, whether the default path is meant to reach spin_sq at all, is still unanswered.<p>The obvious objection is that this is all my own reimplementation, so here's the part that isn't. IBM's data-availability archive for the flagship paper contains the raw hardware measurement records: 2,457,600 shots on [2Fe-2S] from December 2023, 3,163,742 outcomes on [4Fe-4S] from April 2024, plus the integrals and the optimized circuit's parameters. Running their shots through their own pipeline, [2Fe-2S] reaches low ⟨S²⟩ but sits 248 mHa off their own reference, and [4Fe-4S] converges to a spin-pure triplet, Var(S²) = 3e-6, a genuine S=1 eigenstate: a clean state, and the wrong one, 1,438 mHa from their reference.<p>Two things in that archive need no analysis from me at all. Their uniform-random null control matches or beats the hardware samples in every published [2Fe-2S] comparison. And their largest [4Fe-4S] runs, at subspace dimension 10⁸, trail their own classical HCI file by 149 mHa.<p>On the AI angle, since that's half of why this is on HN: Claude did the initial audit end to end in about 72 hours under my direction, and it's been through many rounds of adversarial review since. The part I'd defend as actually interesting isn't the speed. It caught five defects in its own work through pre-registered validation gates, one of them by cross-checking against IBM's own published energy tables, and it retracted its own strongest pro-quantum finding when the new instrument showed that result was a spin-sector artifact. AUDIT_TRAIL.md has the timeline. REPRO_MAP.md maps every claim to a file and a command that regenerates it.<p>If you want to kill this, and I mean that, here's how. Exhibit any state in a spin-completed ground manifold of these benchmarks with ⟨S²⟩ < 1. Or show me a quantum-sampled subspace at matched determinant count whose spin-identified energy beats HCI or CIPSI. Or get any shipped-pipeline run on IBM's archived samples to land ⟨S²⟩ < 1 and error under 50 mHa at once, with no spin penalty. The harness is in the archive and I'll publish whatever comes back, including if it's me who's wrong.<p>Preprint: <a href="https://doi.org/10.26434/chemrxiv.15006382/v1" rel="nofollow">https://doi.org/10.26434/chemrxiv.15006382/v1</a><p>The limitations section is real: comparison dimensions are fixed, the [4Fe-4S] reference is approximate, and the 58.6M "samples" file is deduplicated, so the shot-level distribution of their optimal-circuit numerics isn't publicly auditable. It's short. Worth reading before the hot take.</p>
<hr />
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=49203707">https://news.ycombinator.com/item?id=49203707</a></p>
<p>Points: 3</p>
<p># Comments: 0</p>

🔗 **Read more:** [https://zenodo.org/records/21359923](https://zenodo.org/records/21359923)

---

### 2. Welcoming the Nepalese Government to Have I Been Pwned

**Source:** Hacker News

**Category:** technology

**Description:**
<p>Article URL: <a href="https://www.troyhunt.com/welcoming-the-nepalese-government-to-have-i-been-pwned/">https://www.troyhunt.com/welcoming-the-nepalese-government-to-have-i-been-pwned/</a></p>
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=49203105">https://news.ycombinator.com/item?id=49203105</a></p>
<p>Points: 52</p>
<p># Comments: 12</p>

🔗 **Read more:** [https://www.troyhunt.com/welcoming-the-nepalese-government-to-have-i-been-pwned/](https://www.troyhunt.com/welcoming-the-nepalese-government-to-have-i-been-pwned/)

---

### 3. Show HN: Pokémon Emerald Ported to Raspberry Pi Pico 2

**Source:** Hacker News

**Category:** technology

**Description:**
<p>Pokémon Emerald ported to the RP2350 microcontroller. No emulator, 60 fps HDMI output. Recompiled from ARMv4T to Cortex-M33 and the Game Boy Advance's video hardware is reimplemented in software on the second core.</p>
<hr />
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=49203059">https://news.ycombinator.com/item?id=49203059</a></p>
<p>Points: 34</p>
<p># Comments: 15</p>

🔗 **Read more:** [https://github.com/mattdeeds/pokeemerald-rp2350](https://github.com/mattdeeds/pokeemerald-rp2350)

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

### 7. Trump signs executive orders banning so-called ‘birth tourism’

**Source:** Al Jazeera

**Category:** world

**Description:**
US President Donald Trump signed two executive orders to further limit who is eligible for birthright citizenship.

🔗 **Read more:** [https://www.aljazeera.com/video/newsfeed/2026/8/6/trump-signs-executive-orders-banning-so-called-birth?traffic_source=rss](https://www.aljazeera.com/video/newsfeed/2026/8/6/trump-signs-executive-orders-banning-so-called-birth?traffic_source=rss)

---

### 8. Iran’s Ghalibaf accuses Trump of conducting show diplomacy ‘on loop’

**Source:** Al Jazeera

**Category:** world

**Description:**
US president says he is involved in talks and war will end &#039;pretty soon&#039;, claiming that Iran cannot &#039;go much longer&#039;.

🔗 **Read more:** [https://www.aljazeera.com/news/2026/8/6/irans-ghalibaf-accuses-trump-of-conducting-show-diplomacy-on-loop?traffic_source=rss](https://www.aljazeera.com/news/2026/8/6/irans-ghalibaf-accuses-trump-of-conducting-show-diplomacy-on-loop?traffic_source=rss)

---

### 9. How Abdul El-Sayed’s ‘extraordinary’ win stunned pro-Israel establishment

**Source:** Al Jazeera

**Category:** world

**Description:**
Michigan progressive fended off AIPAC as well as Democratic establishment in US Senate race, supporters say.

🔗 **Read more:** [https://www.aljazeera.com/news/2026/8/6/how-abdul-el-sayeds-extraordinary-win-stunned-pro-israel-establishment?traffic_source=rss](https://www.aljazeera.com/news/2026/8/6/how-abdul-el-sayeds-extraordinary-win-stunned-pro-israel-establishment?traffic_source=rss)

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