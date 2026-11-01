### Hi, I'm Istvan

Software engineer and team lead, 18 years in — backend (Node.js/TypeScript), Scrum, leading teams. Lately I work on one question: **how do humans and AI agents do reliable work together?** I treat that as an architecture and leadership problem, not as a tooling problem.

#### Problems I work on

**AI agents forget why things are the way they are.** Every session starts from zero, so agents repeat old mistakes and undo decisions they never saw.
→ [**Fabrica**](https://github.com/avataristvan/fabrica): a practice for letting agents inherit experience across sessions — decisions recorded with their reasons, superseded instead of deleted, read by a librarian agent that judges instead of scoring. *ai-mem* is its Claude Code plugin. Fabrica was built with its own practice — [here is how](https://github.com/avataristvan/fabrica/blob/main/docs/explanation/how-fabrica-built-itself.md) — and it ships with [what I measured](https://github.com/avataristvan/fabrica/blob/main/docs/explanation/what-we-measured.md), including what did not work.

**One agent ships a big task as one big bang.** No plan anyone checked, no review, nothing learned for next time.
→ [**dev-team**](https://github.com/avataristvan/dev-team): an agent team for Claude Code — plan in small verifiable chunks, review the plan, one coder per chunk that reviews its own work, tests enforced by a hook. Built on Fabrica: every chunk starts from the recorded decisions, and what the team learns goes back into the record.

**Agents start building before anyone understood the task.** A vague request turns into a lot of confident code for the wrong problem.
→ [**briefing-interviewer**](https://github.com/avataristvan/briefing-interviewer): a Claude Code plugin that interviews you first — charter, one domain per conversation, carry-only conclusions — and ends in a briefing an agent (or a colleague) can build from.

**Agents refactor by search-and-replace.** Moving a symbol across a codebase with grep and edit breaks imports in ways nobody notices until later.
→ [**AIDE**](https://github.com/avataristvan/a-i-d-e): a CLI that gives agents deterministic, test-verified refactoring toward Clean Architecture and capability-centric DDD, with rollback.

**Parallel agent sessions can't talk to each other.** Work splits into several sessions, and context gets lost between them.
→ [**kitchen-chat-mcp**](https://github.com/avataristvan/kitchen-chat-mcp): local, serverless messaging between Claude Code sessions — rooms, questions, answers.

**Good hardware gets abandoned by its vendor.** A 2016 tablet with a working screen and battery is e-waste only because its software stopped.
→ [**sm-t585-mainline**](https://github.com/avataristvan/sm-t585-mainline): mainline Linux bring-up for the Samsung Galaxy Tab A 10.1 (Exynos 7870) — kernel, device tree, U-Boot, postmarketOS.

#### Further experiments

- [**fp6sense**](https://github.com/avataristvan/fp6sense) — what can a phone's sensors tell you beyond their intended purpose? Heartbeat from the accelerometer (seismocardiography), motion sensors as a vibration microphone, a pseudo-infrared view from camera RAW data, tested on a Fairphone 6.
- [**WokTuna**](https://github.com/avataristvan/woktuna) — tuners show a handpan's frequencies, not where to hammer. WokTuna detects several partials live from the microphone and turns them into guidance: where on the tone field and along which axis. [Try it in the browser](https://avataristvan.github.io/woktuna/).

#### How I work

- **Understand before building.** Scope, terms and mode first; then deliver in small steps that can each be verified.
- **Decisions keep their reasons.** Written down with a date, replaced by a newer decision rather than deleted.
- **Measure, and publish the negative results too.**
- **Enforce with mechanisms, not with discipline.** Hooks, tests and checks over "please remember to".
- **The same architecture in every stack.** Domain, application, infrastructure, UI — in Python tools, Android apps and web apps alike.
- **Lead agents the way I lead people:** clear scope, honest uncertainty, room to say "I don't know".
