# 📰 Daily News Bot - 48+ Commits Daily

**Last Update:** 2026-08-20 19:24:20

**Total News:** 12

**Sources:** Al Jazeera, NASA, BBC, Hacker News

---

## 📰 Latest News

### 1. How to compromise your system with a job interview

**Source:** Hacker News

**Category:** technology

**Description:**
<p>Article URL: <a href="https://www.codedge.de/posts/how-to-compromise-your-system-with-a-job-interview">https://www.codedge.de/posts/how-to-compromise-your-system-with-a-job-interview</a></p>
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=49376332">https://news.ycombinator.com/item?id=49376332</a></p>
<p>Points: 4</p>
<p># Comments: 0</p>

🔗 **Read more:** [https://www.codedge.de/posts/how-to-compromise-your-system-with-a-job-interview](https://www.codedge.de/posts/how-to-compromise-your-system-with-a-job-interview)

---

### 2. I Am Morally Opposed to Updating My Claude.md

**Source:** Hacker News

**Category:** technology

**Description:**
<p>Article URL: <a href="https://alex-jacobs.com/posts/claudemd/">https://alex-jacobs.com/posts/claudemd/</a></p>
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=49376287">https://news.ycombinator.com/item?id=49376287</a></p>
<p>Points: 5</p>
<p># Comments: 0</p>

🔗 **Read more:** [https://alex-jacobs.com/posts/claudemd/](https://alex-jacobs.com/posts/claudemd/)

---

### 3. Launch HN: Vendo (YC S26) – Let users build features on top of your product

**Source:** Hacker News

**Category:** technology

**Description:**
<p>Hi HN, we’re Yousef & Nour, founders of Vendo (<a href="https://vendo.run">https://vendo.run</a>). Vendo lets users create new features inside the software they already use. A user describes the dashboard, workflow, or small app they need, and Vendo builds it on top of the product’s existing data, API, and interface.<p>Demo: <a href="https://www.youtube.com/watch?v=VdpHehY64ls" rel="nofollow">https://www.youtube.com/watch?v=VdpHehY64ls</a><p>We built Vendo because every SaaS eventually faces the same problem: every customer needs something slightly different. One wants a new report and another needs a workflow that only makes sense for their team. These requests either sit on the roadmap, become one-off engineering work, or force the customer into spreadsheets and external tools. We wanted the user to be able to create the missing feature themselves, without leaving the product.<p>Here is how it works:<p>- npx vendo init reads the product's API surface, theme, routes, and more. These are used so that the apps Vendo creates (1) look on-brand and native and (2) have the ability to read data and perform actions directly through the company's API<p>- When a user asks for a feature, we have a custom Vendo harness that writes a React component with a bunch of Vendo add-ons and guardrails (ex. ability to make calls to the host API + our component library). Every save is compiled, type-checked, run against real API responses, and rendered before the user sees it. We just released a benchmark and write-up here with more info for anyone interested: <a href="https://vendo.run/blog/generating-product-ui-measured">https://vendo.run/blog/generating-product-ui-measured</a><p>- We use QuickJS to make sure that anything the agent creates is sandboxed and can't mess with the company's site. Vendo compiles the component and runs it with Preact inside a QuickJS VM with no access to the DOM, network, or clock. The VM returns a UI tree, which the host renders using the product’s registered components. When the user clicks something, QuickJS emits a tool call; the host executes it through Vendo’s guard and passes the result back into the same VM, preserving the screen’s local state.<p>There's a lot of generative UI right now: streaming developer-written components into a chat (Vercel AI SDK, CopilotKit, Thesys), or rendering your app inside someone else's assistant (OpenAI Apps SDK, MCP Apps). We differ on two things. Vendo lives in your product and acts through your API as the signed-in user, so what it makes is durable: real apps users keep, pin, and run on triggers while they're away, and not components that are merely confined to a chat. Plus, it's not capped at putting together a bunch of prebuilt components: the agent can build arbitrary apps, from a quick dashboard out of your own components to real custom code running in a sandbox, and either way data only ever comes from tool calls to your API.<p>Here are some things customers are using Vendo for today:<p>- Letting their users create custom dashboards and reports. These are mainly UI-based and focused on letting the user see the exact graphs and metrics they care about<p>- Letting their customers create recurring automations. A big thing as well that has been used for these automations is the fact that we connect to external connections, so users have been automating many of their inter-tool workflows (ex. an automation that sends a slack alert based off of something in the product)<p>- B2B customers letting their customers customize the product with specific business logic. Often this is simple things like an extra field on a form, or an extra permission, but it is hard for a business to keep up with them otherwise.<p>- Creating and sharing custom dashboards/apps across an organization. Since the apps Vendo creates are durable, they can be shared, reused, and forked (which can’t be done with many of the other in-chat generative UI solutions)<p>We've spent a lot of time thinking about how AI and agents will change the way people consume software. We think the answer is personal(ized) software: you see the UI you need to see, you tell an agent exactly what you need, and the product molds to how you work.<p>The key insights that have enabled the product to work are:<p>- A rule in code always beats a rule in a prompt.<p>- Invent as little syntax as possible. Generation got faster and more reliable when the output looked like what models already know (JSX-shaped markup) instead of a clever custom format.<p>- Deterministic beats model wherever you can get away with it. Theme extraction is pure static analysis, and a remix starts as a copy of your component, no model call.<p>Vendo is completely open-source (Apache-2.0) and can be self-hosted, so feel free to check out all the source code here: <a href="https://github.com/runvendo/vendo" rel="nofollow">https://github.com/runvendo/vendo</a>.<p>Would love you to try it out and give us your feedback: <a href="https://docs.vendo.run/">https://docs.vendo.run/</a>. Or if you’re a company looking to embed Vendo in your product feel free to book a call here: <a href="https://cal.com/team/vendo/intro-call" rel="nofollow">https://cal.com/team/vendo/intro-call</a></p>
<hr />
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=49376038">https://news.ycombinator.com/item?id=49376038</a></p>
<p>Points: 6</p>
<p># Comments: 0</p>

🔗 **Read more:** [https://github.com/runvendo/vendo](https://github.com/runvendo/vendo)

---

### 4. Harry and Meghan's security arrangements a private matter, PM says

**Source:** BBC

**Category:** world

**Description:**
The prime minister also wishes the Duke and Duchess well after it emerged they are returning to the UK later this month.

🔗 **Read more:** [https://www.bbc.co.uk/news/articles/cr59yg34r4mo?at_medium=RSS&at_campaign=rss](https://www.bbc.co.uk/news/articles/cr59yg34r4mo?at_medium=RSS&at_campaign=rss)

---

### 5. Why are Harry and Meghan returning to the UK?

**Source:** BBC

**Category:** world

**Description:**
BBC culture correspondent Noor Nanji looks at why the move raises questions over security detail, royal duties Harry's relationship with King Charles and Prince William.

🔗 **Read more:** [https://www.bbc.co.uk/news/videos/cp8eg084n3eo?at_medium=RSS&at_campaign=rss](https://www.bbc.co.uk/news/videos/cp8eg084n3eo?at_medium=RSS&at_campaign=rss)

---

### 6. Five key takeaways from GCSE results day 2026

**Source:** BBC

**Category:** world

**Description:**
Resits are up, the gap between boys and girls has shrunk and England's regional divide has widened.

🔗 **Read more:** [https://www.bbc.co.uk/news/articles/cx2583xew8zo?at_medium=RSS&at_campaign=rss](https://www.bbc.co.uk/news/articles/cx2583xew8zo?at_medium=RSS&at_campaign=rss)

---

### 7. Deadly Russian missile barrage hits Kyiv in hours-long overnight attack

**Source:** Al Jazeera

**Category:** world

**Description:**
Russia launched a hours-long overnight barrage of ballistic and cruise missiles and drones across Kyiv.

🔗 **Read more:** [https://www.aljazeera.com/video/newsfeed/2026/8/20/deadly-russian-missile-barrage-hits-kyiv-in-hours-long-overnight-attack?traffic_source=rss](https://www.aljazeera.com/video/newsfeed/2026/8/20/deadly-russian-missile-barrage-hits-kyiv-in-hours-long-overnight-attack?traffic_source=rss)

---

### 8. Gunmen seize tanker off Yemen amid resurgence of Somali piracy

**Source:** Al Jazeera

**Category:** world

**Description:**
UK maritime security monitor says Seamull tanker diverted towards Somalia, as wave of piracy sweeps the Gulf of Aden.

🔗 **Read more:** [https://www.aljazeera.com/news/2026/8/20/gunmen-seize-tanker-off-yemen-amid-resurgence-of-somali-piracy?traffic_source=rss](https://www.aljazeera.com/news/2026/8/20/gunmen-seize-tanker-off-yemen-amid-resurgence-of-somali-piracy?traffic_source=rss)

---

### 9. Can US, Middle Eastern powers unite Libya 15 years after Gaddafi overthrow?

**Source:** Al Jazeera

**Category:** world

**Description:**
The US government is intensifying efforts to unify the country&#039;s two rival governments.

🔗 **Read more:** [https://www.aljazeera.com/news/2026/8/20/can-us-middle-eastern-powers-unite-libya-15-years-after-gaddafi-overthrow?traffic_source=rss](https://www.aljazeera.com/news/2026/8/20/can-us-middle-eastern-powers-unite-libya-15-years-after-gaddafi-overthrow?traffic_source=rss)

---

### 10. Tropical Storm Saudel

**Source:** NASA

**Category:** nature

**Description:**
Natural event: Severe Storms

🔗 **Read more:** [https://eonet.gsfc.nasa.gov/api/v3/events/EONET_22926](https://eonet.gsfc.nasa.gov/api/v3/events/EONET_22926)

---

### 11. Wildfire Picture Rock, Lake, Oregon

**Source:** NASA

**Category:** nature

**Description:**
Natural event: Wildfires

🔗 **Read more:** [https://eonet.gsfc.nasa.gov/api/v3/events/EONET_22798](https://eonet.gsfc.nasa.gov/api/v3/events/EONET_22798)

---

### 12. Wildfire CATO 2, Chaves, New Mexico

**Source:** NASA

**Category:** nature

**Description:**
Natural event: Wildfires

🔗 **Read more:** [https://eonet.gsfc.nasa.gov/api/v3/events/EONET_22800](https://eonet.gsfc.nasa.gov/api/v3/events/EONET_22800)

---


**Built with ❤️ by GitHub Actions**