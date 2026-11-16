# Aathiseshan A K — Agent Engineering Portfolio

I design and ship AI tools for enterprise software support: LLM agents that read support cases, trace causes in
large codebases and draft answers, plus the servers, safety rules, tests and measurement around them. I came up
through customer support, so I build for the people who use the tools every day.

The projects below were built for my employer and their code is proprietary, so **this repository holds write-ups,
not code**: the problem, what I built, how it is put together, and what it achieved. No company code, customer data
or internal details are included.

## Projects

| Project | What it is | Main skills |
| --- | --- | --- |
| [Orbit](orbit/README.md) | An AI copilot for support cases, used team-wide across several enterprise ERP products | LLM agents, Python/Flask, client–server design, signed releases, testing, AI evaluation |
| [Skill Builder](skill-builder/README.md) | An MCP tool server that turns closed support cases into reusable troubleshooting guides | MCP, tool design for LLMs, personal-data scrubbing, validation |

### Also built

- **Atlas:** Claude Code commands that explain customers' own C# customisations in plain English, so support
  staff understand custom code without waiting for a developer.
- **Team workflows:** Power Automate flows for the support team's own processes, such as turning issue reports
  sent by e-mail into tracked Planner tasks.
- **Dart:** an analysis of existing AI agents, and the strategy for rebuilding them.

## What these projects have in common

- **The AI works where the data is allowed to be.** Models run on each analyst's own machine with their own
  account; shared servers hold no AI and no case data beyond what the team chose to share.
- **Read-only by default, a person confirms every write.** Agents get read-only tools confined to what one task
  needs; anything that changes a system goes through a preview and a human click.
- **Measured, not assumed.** Model changes, prompt changes and cost cuts ship only after a benchmark or a check on
  real, closed cases shows they help.
- **Built to be maintained.** Automated tests, secret scanning on every commit, reviewed pull requests and signed
  releases.

## Contact

[LinkedIn](https://www.linkedin.com/in/aathi-seshan-a-k-52491b260)
