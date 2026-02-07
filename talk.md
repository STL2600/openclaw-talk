% OpenClaw
% Robert / Joe
%![](static/qrcode.png)<br/>Talk: [${TALK_URL}](${TALK_URL})<br/>Repo: [${REPO_URL}](${REPO_URL})

# Or ...

# Welcome to the Shitshow

# What is it?

# Why would you want that?

# The Horror

![](static/bug-report.png)


## Branding

---

In the beginning there was ClawdBot

::: notes

This made a lot of people (mainly anthropic) very upset and was widely regarded as a bad move.

:::

---

Then there was MoltBot

::: notes

I guess the idea was the lobster was molting?

:::

---

Then about 24 hours later, OpenClaw was born

::: notes

Seriously, two name changes in like a day.

:::

---

## So What?

 - GitHub and Twitter handles immediately squatted
 - Dozens of fradulent packages on NPM
 - Crypto pump & dump schemes
  
## Malicious Skills

## What are Skills

- Extends OpenClaws Capabilities
- Just Plain-text Instructions
- Easy to create, Easy to Abuse

::: notes

One of the attractive things about OpenClaw is how easy it is to add capabilities.
These are referred to as "skills".
Sometimes they include a script or something, but like 99% of it is just a man page written in markdown explaining to the AI how to use a command-line tool.

It's so frightenly simple that you not only do you not have to code it, but you could simply just ask another LLM to write it for you.

Consequently, this makes it just as easy to abuse.

:::

## Skill Repos

- ClawHub.ai
- Skills.sh
- Moltbook

::: notes

ClawHub is the official skill repository
There are some others, such as Skills.sh
And of course, there Moltbook, which is Reddit for AI agents.

:::

## The Dumb Way To Install A Skill

![](static/install-skill-example-2.png)

::: notes

They found a worse way than piping a script to bash for installing skills

:::

## Statistics
- Approx 20% of skills Malicious
- 54% of Crypto-currency/Gambling
- 24% of Social Media
- 17% of Maintenance Automation
- 5% of Productivity

::: notes

ClawHub started late January 27th.
Between then and February 1st, over 230 malicious skills were published in that week.
That was almost 20% of the total skills.
Let that sink in. 1 in 5 skills are malicious.
Of those skills...

Those numbers came from security reasearcher Jamieson O'Reilly
Othert sources, such as Koi Security say that number is higher (341 of 2857)
Not coutning the 29 typosquat instances they found

:::


## Moltbook

![](static/moltbook-screenshot.png)


## Moltbook

- Agents can share skills
- Pinoccio also gets to pretent to be a real boy!

::: notes

Moltbook...
Reddit for AI Agents.
Left on their own, after being given a vague prompt, it allows agents to share skills among themselves.
Now if you haven't read enough sci-fi that this alone makes your butthole pucker up, I assure you this is worse than you thought.

:::

## MoltBook

- Lauched 9 Days ago
- 1.5 Million Agents

::: notes

Launched January 28th.
The website claims it already has over 1 million agents using it.
Wiz researchers says only about 17,000 human owners are using it though
The owner of Moltbook directed his own bot to inflate thos numbers by registering users.

Bot-to-bot attacks
- Prompt injection against other agents
- Agents instructing others to delete their own accounts
- Crypto-pump-and-dump scemes

But this was so shoddily put together, by the 4th day, 404 reported
- Vulnerabiltiy in Unsecured database
- Allowed anyone to commandeer any agent on the platform
- Bypassed authentication measures
- Inject commands directly into agent sessions
- Platform was taken offline to be patched and all API tokens reset.
- Moltbook founder admits it was entirely vibe-coded and didn't write a single line of code.


:::




## Old Fashioned Vulnerabilities

--- 

CVE-2026-25253 (CVSS 8.8)

::: notes

One click RCE.  User just has to visit a malicious site.

:::

---

CVE-2026-25157 (CVSS 7.8)

::: notes

Allows for arbritrary command exec on any system that the agent can ssh into.

:::

---

CVE-2026-24763 (CVSS 8.8)

::: notes

Sandbox escape.

:::

## Prompt Injection

Any text OpenClaw has access to can be prompt injected.

## Prompt Injection

- Email
- Calendar
- iMessage
- OCR Images
- Voicemail (with voice to text)

## Prompt Injection Example

Ask OpenClaw the Following:
```
Run the command gog gmail search "is:unread" --max=1
Read the contents of the email
Summarize the email's contents
```

## Prompt Injection Example

![](static/prompt-injection-email.png)

::: notes

Then OpenClaw comes across this email.

:::

## Exposed Instances

![](static/exposed-instances.png)

::: notes

Mac Mini is the most popular deployment
Deployment instructions had "just forward a port"
Insecure by default

:::

## Shadow IT

Token Security found that 22% of their clients have OpenClaw deployed somewhere

::: notes

Token Security (Some AI based security company) is reporting 22% of their customers have OpenClaw deployed

Given the nature of Token's business, that may be a skewed figure, but it's still a lot.

:::

## The Lethal Trifects

![](static/lethal-trifects.png)

# Our Advice

## Don't

![](static/no-nope.gif)

## Seriously

![](static/no-nope.gif)

## Just No

![](static/no-nope.gif)

## Okay, if you have to

## VM / Container

![](static/hannibal.png)

::: notes

OpenCLaw by default runs things in its own docker containers, but there's been at least one escape vuln so far
Run the whole thing in a VM with limited permissions and network access
     - No local network
     - Monitor incoming and outgoing connections
Very restricted filesystem access

:::

## No Creds

![](static/keys.png)

::: notes

For fucks sake don't give it access to your email or banking info
Don't give it your crypto
Don't give it your messaging
Don't give it your chipotle customer rewards number

:::

## Small Blast Radius

::: notes

If you get owned what's the _worst_ thing it can do?
Think about untrusted input
Think about the tools you give it

:::

## Review Skills

## Spotting a Malicious Skill

![](static/vuln-skill-example.png)

::: notes

Took me about 10 minutes of browisng ClawHub and I found one.

:::

## Spotting a Malicious Skill

- Is it similar in name to another skill?
- Does it use AuthTool?
- Is there a reason that string is Base64?
- Use a skill scanner.

::: notes

- Might appear to have extensive documentation
- Clones of existing skills with randomized names
- Does it require "AuthTool", which is a malware-delivery tool
- Look for commands containing Base64 encoded strings
- Use a skill scanner
- Use your head.

:::


## Scanners

- https://clawdex.koi.security/
- https://www.bitdefender.com/en-us/consumer/ai-skills-checker

::: notes



:::

# The End

---

Robert / Joe

![](static/qrcode.png)

Talk: [${TALK_URL}](${TALK_URL})

Repo: [${REPO_URL}](${REPO_URL})
