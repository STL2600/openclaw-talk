% Welcome to the shitshow / OpenClaw
% Robert / Joe
%![](static/qrcode.png)<br/>Talk: [${TALK_URL}](${TALK_URL})<br/>Repo: [${REPO_URL}](${REPO_URL})

# What is it?

# Why would you want that?

# The Horror

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

### So What?

 - GitHub and Twitter handles immediately squatted
 - Dozens of fradulent packages on NPM
 - Crypto pump & dump schemes
  
## Malicious Skills

## Old Fashioned Vulnerabilities

-- 

CVE-2026-25253 (CVSS 8.8)

::: notes

One click RCE.  User just has to visit a malicious site.

:::

--

CVE-2026-25157 (CVSS 7.8)

::: notes

Allows for arbritrary command exec on any system that the agent can ssh into.

:::

--

CVE-2026-24763 (CVSS 8.8)

::: notes

Sandbox escape.

:::

## Prompt Injection

## Exposed Instances

![](static/exposed-instances.png)

::: notes

Mac Mini is the most popular deployment
Deployment instructions had "just forward a port"
Insecure by default

:::

## Shadow IT

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

# The End

---

Robert / Joe

![](static/qrcode.png)

Talk: [${TALK_URL}](${TALK_URL})

Repo: [${REPO_URL}](${REPO_URL})
