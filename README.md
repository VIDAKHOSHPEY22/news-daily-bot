# 📰 Daily News Bot - 48+ Commits Daily

**Last Update:** 2026-08-19 21:16:16

**Total News:** 12

**Sources:** BBC, NASA, Hacker News, Al Jazeera

---

## 📰 Latest News

### 1. Show HN: Frugal Tokens – explore costs and usage across coding agents

**Source:** Hacker News

**Category:** technology

**Description:**
<p>I wanted to share a project I’ve been working on called Frugal Tokens. I originally built it because I was curious to see how much all of my sessions cost and how much cache misses affected that spend. I’d noticed people had widely different spend profiles and wanted to better understand what might contribute to that.<p>As I’ve worked on this, the tool has grown to show more usage patterns across all of your sessions. It shows overall usage, estimated working time and overlapping sessions, and where your spend is coming from across models and cache misses. I also have a few session level metrics with percentile breakdowns, along with a list of your sessions and high level info.<p>Clicking into a session opens an explorer where you can see individual model calls and tool inputs and outputs. You can also jump directly to where a cache miss happened. There’s also a rough cost comparison that shows what the recorded session would have cost with another model’s pricing, or for Anthropic, with 5m vs 1h caching.<p>In the future, I’d love to collect more information to see which patterns might make people’s workflows more expensive, e.g. long sessions, high context usage, many turns, etc.<p>The tool requires deno, but is just one command to run once that is installed. The demo provided has some of the data scrubbed, but helps to show what it looks like before running it.<p>Would appreciate any thoughts or ideas<p><a href="https://github.com/dpclark4/frugal-tokens" rel="nofollow">https://github.com/dpclark4/frugal-tokens</a></p>
<hr />
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=49364223">https://news.ycombinator.com/item?id=49364223</a></p>
<p>Points: 11</p>
<p># Comments: 2</p>

🔗 **Read more:** [https://demo.frugaltokens.com/](https://demo.frugaltokens.com/)

---

### 2. Launch HN: OneCLI (YC S26) – OSS sandboxed agent harness for teams

**Source:** Hacker News

**Category:** technology

**Description:**
<p>Hi HN, Jonathan & Guy here from OneCLI, an agent harness built for teams, giving every employee a secured, sandboxed personal agent.<p>Here’s what you can do with it:<p>1. get a sandboxed agent, with all the OneCLI capabilities in place like connect your GitHub account, Gmail, Notion, or Dropbox simply from the chat.<p>2. deterministic human in the loop approval in the chat itself for things that you need 100% control like sending an email or deleting the Linear ticket.<p>3. manage team policy in one place, enforced across every agent in the workspace<p>4. enjoy global connections at the team level, like shared LLM keys or service accounts<p>Here’s a demo: <a href="https://www.youtube.com/watch?v=dlW-44ntpbE" rel="nofollow">https://www.youtube.com/watch?v=dlW-44ntpbE</a><p>We started working on this by accident, even though our careers were in the security space. We were working on a devtool called ChartDB, an open-source DB tool. When OpenClaw took off back in January, we started using it to orchestrate agents on top of ChartDB. We quickly understood there is a big issue around auth. Agents need credentials to do real work, but to give them those secrets would not be the best idea. They keep them in their memory and also write them down to local files and their sessions as plain text. And we knew that agents can easily be fooled into giving up those API keys/secrets. So we needed some way to control the agent and stop prompt injections from tricking it into using its services for an attacker's benefit.<p>We created OneCLI that started as a vault for AI Agents built in Rust.<p>We found out that most of our demand for OneCLI came from autonomous agents like Hermes, OpenClaw and NanoClaw for individuals and teams.<p>Users looked for useful agents that do things for the person who runs them with two missing parts: 1) managing secrets and permissions. 2) and for teams - multiplayer management.<p>We decided to pivot and provide the agent itself as a harness for teams, to give each employee an agent. We saw that teams had to deal with setting up their own harness again and again, and basically as we already had the vault as a gateway. We got the idea to provide the missing piece of the agent management out of the box and open source it (Apache-2.0, with a small enterprise exception).<p>We're open source first - the entire platform, not just a small portion of it like other agents, so companies can actually see the code, evaluate it, and trust it instead of taking our word for it. They run it isolated, in their own environment, fully under their control, at production quality, not a locked black box hosted somewhere else. That means the safety isn't just a promise, it's something they can verify themselves. Combined with real autonomy and least-privilege access, that's what makes it something a company can fully own and trust, not just adopt.<p>We also approach this from a company perspective rather than an individual one. Our solution manages agents on behalf of each employee, wrapped in deterministic guardrails that company admins configure through centralized policies.<p>For the agent engine itself we’re using jcode which is the core of the agent-loop. We found out that it improves the experience and makes the agent smarter and faster.<p>Here’s how it works:<p>It runs on infra you control. Fully open-source, self-host or cloud in minutes.<p>The agent never holds a real secret. It gets a placeholder. The real credential is injected at the gateway, per request, after the call is authorized. It never enters the agent's context, memory, or logs.<p>Enforcement outside the model. Prompts are suggestions. Policies defined by the org admin run at the network layer, outside the agent and the LLM. Block endpoints, rate limit per agent, require approval, scope per employee. The gateway decides. The agent can't bypass it.<p>Isolated VM per agent. Own memory, own keys, own permissions. Blast radius is one agent.<p>Speed of the Harness: Rust engine under the agent loop.<p>Full identity trail. Every agent is bound to an employee. Every call logged with who it acted for and which policy allowed it.<p>Some things people are doing with the platform include:<p>- Managing their company life cycle entirely from the sales calls, to the product side automatically open tickets to the engineering teams, that would kick the development agents to deliver and ship to production.<p>- Operational side, like automatically hygiene the CRM after calls, sourcing leads, book meetings and manage follow ups emails.<p>- Some of our customers also doing their entire grocery shopping using those agents and send them to take care of their chores like ordering things online.<p>About the team: Both founders come from cybersecurity backgrounds. Jonathan spent years at Axis Security building zero trust network access. The core idea is that you never trust the client. You decide exactly what a person can reach, and you enforce it outside of them, at the network layer, so it doesn't matter what the client tries to do. That's how every serious company gives access to humans today. Guy was the 1st employee in Argon security doing AppSec.<p>We would love to hear your thoughts on the move, happy to get issues open to improve and get your agent to be powerful and secure - designed for teams, not just individuals.</p>
<hr />
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=49363710">https://news.ycombinator.com/item?id=49363710</a></p>
<p>Points: 19</p>
<p># Comments: 4</p>

🔗 **Read more:** [https://github.com/onecli/onecli](https://github.com/onecli/onecli)

---

### 3. Extensible Software in the Age of LLMs

**Source:** Hacker News

**Category:** technology

**Description:**
<p>Article URL: <a href="https://jeremymorrell.dev/blog/extensible-software-in-the-age-of-llms/">https://jeremymorrell.dev/blog/extensible-software-in-the-age-of-llms/</a></p>
<p>Comments URL: <a href="https://news.ycombinator.com/item?id=49363668">https://news.ycombinator.com/item?id=49363668</a></p>
<p>Points: 19</p>
<p># Comments: 11</p>

🔗 **Read more:** [https://jeremymorrell.dev/blog/extensible-software-in-the-age-of-llms/](https://jeremymorrell.dev/blog/extensible-software-in-the-age-of-llms/)

---

### 4. Track defect found on approach to site of Lewes derailment, initial report says

**Source:** BBC

**Category:** world

**Description:**
Initial findings from an RAIB investigation show an "irregularity" at the site near Lewes.

🔗 **Read more:** [https://www.bbc.co.uk/news/articles/c4gx12v8z51o?at_medium=RSS&at_campaign=rss](https://www.bbc.co.uk/news/articles/c4gx12v8z51o?at_medium=RSS&at_campaign=rss)

---

### 5. Thunderstorm warnings issued for parts of UK with flash flooding expected

**Source:** BBC

**Category:** world

**Description:**
Warnings for northern England, eastern Scotland and Northern Ireland will come into force later on Wednesday.

🔗 **Read more:** [https://www.bbc.co.uk/news/articles/c0m7e9ym747o?at_medium=RSS&at_campaign=rss](https://www.bbc.co.uk/news/articles/c0m7e9ym747o?at_medium=RSS&at_campaign=rss)

---

### 6. Israel confirms soldiers fired at car in which Hind Rajab was killed and opens criminal investigation

**Source:** BBC

**Category:** world

**Description:**
The five-year old Gaza girl initially survived the attack and pleaded for help but her body was recovered later with those of six of her relatives.

🔗 **Read more:** [https://www.bbc.co.uk/news/articles/crl7yjlpx2po?at_medium=RSS&at_campaign=rss](https://www.bbc.co.uk/news/articles/crl7yjlpx2po?at_medium=RSS&at_campaign=rss)

---

### 7. Hamas condemns ‘new war crime’ as Israel kills 10 in crowded Gaza hubs

**Source:** Al Jazeera

**Category:** world

**Description:**
Israeli air strikes on Gaza kill 10 Palestinians, targeting police headquarters and a refugee camp in separate attacks.

🔗 **Read more:** [https://www.aljazeera.com/news/2026/8/19/hamas-condemns-new-war-crime-as-israel-kills-10-in-crowded-gaza-hubs?traffic_source=rss](https://www.aljazeera.com/news/2026/8/19/hamas-condemns-new-war-crime-as-israel-kills-10-in-crowded-gaza-hubs?traffic_source=rss)

---

### 8. US pressure on Israel needed for peace in Syria

**Source:** Al Jazeera

**Category:** world

**Description:**
With Israeli elections approaching, analysts say Netanyahu needs a new escalation, undermining deconfliction efforts.

🔗 **Read more:** [https://www.aljazeera.com/features/2026/8/19/us-pressure-on-israel-needed-for-peace-in-syria?traffic_source=rss](https://www.aljazeera.com/features/2026/8/19/us-pressure-on-israel-needed-for-peace-in-syria?traffic_source=rss)

---

### 9. US and Canada reach ‘very fair’ trade agreement, Trump says

**Source:** Al Jazeera

**Category:** world

**Description:**
New trade deal ensures no tariffs for US farmers and businesses exporting to Canada, Trump announces

🔗 **Read more:** [https://www.aljazeera.com/economy/2026/8/19/us-and-canada-reach-very-fair-trade-agreement-trump-says?traffic_source=rss](https://www.aljazeera.com/economy/2026/8/19/us-and-canada-reach-very-fair-trade-agreement-trump-says?traffic_source=rss)

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