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
10. Black Friday: everything at once

There is also a Sandbox with traffic sliders and buttons to break things on purpose.

## For teaching

- **Tutorial:** the first time you open Launch Day, a short guided walk-through points at exactly where to drag. Replay it from the menu.

- **Teach mode** pauses the game when something goes wrong, shows a small diagram, and asks what you would do.
- **Who is playing:** Mid-level gets hints; Staff and Principal get fewer hints and discussion questions after each shift.
- **Inspector:** click any column or chart to see the numbers behind it.

The numbers are a simple model chosen to teach the ideas, not a benchmark of any real product.

One HTML file, no build step, no tracking. Progress is kept only in your browser.
