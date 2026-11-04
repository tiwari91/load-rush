# Load Rush

A browser game about keeping a website up while traffic changes in real time.

**Play:** https://tiwari91.github.io/load-rush/

Requests flow through your system as moving dots. Drag parts onto the board (load balancer, app servers, autoscaler, cache, read replicas, standby database, CDN, rate limiter, queue and workers, canary deploys, timeouts and a circuit breaker) and keep the error budget above zero until the shift ends.

## Shifts

1. Launch Day: one server, rising traffic
2. Flash Sale: a short spike of shoppers
3. Bot Swarm: traffic jumps 8x but sales do not
4. Checkout Crunch: slow work inside requests
5. Friday Deploy: a bad release, twice
6. Memory Leak: servers slowly choke and restart
7. Failover Night: the main database dies
8. Zone Outage: half the servers vanish
9. Slow Partner: an outside payment API hangs
10. Viral Video: a homepage video is shared everywhere, mostly images
11. Payday Rush: salary day payments, then the payment network slows
12. Storm Night: a zone goes down, then the database dies
13. Release Week: a leaky release, a bot wave and a rushed hotfix
14. Black Friday: everything at once

Every shift also explains its problem **in everyday terms** (a shop, a bank, a restaurant), so developers from any background (frontend, mobile, data, QA) can follow the use case.

There is also a Sandbox with traffic sliders, buttons to break things on purpose, and nine guided experiments (load balancer, cache, bot flood, CDN, queue, safe database failover, losing a zone, a canary catching a bad release, a circuit breaker against slow payments), each ticked off when you reach its goal.

## On call (a new shift every day)

The top of the menu has **tonight's on-call shift**: a made-up company, 3 incidents (4 at weekends) drawn from
the game's own problems (now including a surprise server crash), and the same shift for everyone on the same day. A **handover note** announces some
incidents; others are a surprise. Halfway through, someone asks you for a **decision** (send the marketing email
now? cut the budget? release a fix mid-shift? switch the cache off for fresh prices? let a partner run a bulk import at peak time?). Afterwards you get **points**, an **incident report** (what
happened, what it cost, how you handled it, the lesson, and the real-world tools), your streak, and a result
you can copy and share. **Practice on call** gives random shifts as often as you like.

## For teaching

- **Start here** (top of the menu): Tutorial, Parts guide, a quiz, then shifts 1 to 3 and the Sandbox.
- **Real config and labs:** every part card shows a short real config (nginx, Kubernetes HPA, Redis, SQS in Terraform, RDS Multi-AZ...) and a **Try it yourself** lab: numbered beginner steps, free or local first (Docker, kind, Moto), real AWS only where needed with a $5 budget alarm and same-day cleanup. The guide also has an **API Gateway** card with its own free-tier lab.
- **AWS Builder** (menu, Learn the basics): put the real setup steps of 13 AWS services in order: VPC, IAM role, ALB, API Gateway + Lambda, CloudFront, Auto Scaling, ECS Fargate, RDS Multi-AZ, ElastiCache, SQS with a dead-letter queue, WAF, Route 53 with HTTPS, and a CloudWatch alarm. Each right step explains what it does.
- **Read the graph:** six dashboards (memory leak, bot flood, zone outage, bad release, traffic spike, slow partner); name the incident from the shape of the lines.
- **Try again with a hint:** after a rough shift, retry with the part that fixes what hurt most glowing in the tray.
- **Cost challenge:** win a shift under 80%, 90% or 100% of its spend limit for a Gold, Silver or Bronze cost medal, shown on the shift card.
- **Write-up practice:** after an On call shift, write the 3-line incident summary yourself, then compare it with a model answer built from your shift.
- **Challenge a friend:** after winning a shift, copy a link with your score; whoever opens it sees the challenge on the menu.
- **It really happened:** seven shift briefs link a real outage with the same lesson and the company's own write-up (Slack 2021, Cloudflare 2019, Facebook 2021, GitHub 2018, Amazon S3 2017, AWS us-east-1 2021, Fastly 2021).
- **Quiz: which part fixes this?** Eight short scenarios; each answer explains why and gives the everyday comparison.

- **Parts guide** (menu, and from Words): every part in the order a visit travels, with what it does, an everyday comparison, a concrete example, when to use it, when it is the wrong fix, and the shift that teaches it. Clicking a part on the board also shows its everyday comparison.

- **Tutorial:** the first time you open Launch Day, a short guided walk-through points at exactly where to drag. Replay it from the menu.

- **Help when health drops** (on by default): at 60% and 25% health, or when it is falling fast, the game pauses
  and explains what is happening, why, what to do and what comes next. *Do it for me* adds enough to fix it, or
  *Show me where* highlights the part and the column. The game then carries on at half speed.
- **Teach mode** pauses the game when something goes wrong, shows a small diagram, and asks what you would do.
- **Part cards:** click any part on the board to see what it does, what it costs, when it is the wrong fix, and
  its real-world name.
- **Learning path:** 13 skills (scaling out, caching, CDN, rate limiting, queues, canaries, failover, zones,
  timeouts, autoscaling, cost, judgement), each ticked off the first time you show it in a shift.
- **Who is playing:** Mid-level gets hints; Staff and Principal get fewer hints and discussion questions after each shift.
- **After each shift:** a chart of site health with what happened and what you did, plus the problem that hurt most and its fix.
- **Words:** a plain glossary of every term in the game.
- **Presenter mode:** bigger text for a projector or screen share.
- **Inspector:** click any column or chart to see the numbers behind it.

The numbers are a simple model chosen to teach the ideas, not a benchmark of any real product.

One HTML file, no build step. No cookies and nothing personal is collected: the live site sends anonymous play
counts (shift started, won or lost) and any feedback you choose to send to GoatCounter. Progress is kept only in your browser: a shift in progress is saved every few seconds and can be resumed after a reload, and **Menu → Copy my progress** gives a code you can paste into another browser to move your stars, settings, skills, best scores and on-call streak.
