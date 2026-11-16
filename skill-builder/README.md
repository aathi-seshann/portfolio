# Skill Builder — support knowledge, captured

**Role:** designer and developer.

## The problem

When a hard support case is solved, the solution usually stays in that one case: in an e-mail thread, a comment, a
code change. The next analyst with the same problem starts again. Writing it up as a guide takes time nobody has,
and a guide copied from a case carries customer names and details that must not be shared.

## What it does

Skill Builder is an **MCP tool server**: a set of tools that an LLM (for example Claude) calls to turn a closed
support case into a reusable troubleshooting guide, a "skill", written for any customer.

The model does the writing. The tools do the parts a model should not guess at:

| Step | Tool's job |
| --- | --- |
| Gather | Fetch the closed case with its comments and e-mails; plan a batch of cases at once |
| Ground | Search the product's code and read the files and symbols the case points to |
| Check | Validate the guide's structure, check its citations, and find existing guides that already cover it |
| Protect | Scan for personal data and customer details before anything is saved |
| Review | A subject-matter-expert review step before a guide is published |
| Save | Save with a dry run first; keep a tracker of what was built, and a usage report |

## Design choices

- **The model authors, the tools verify.** The server never writes prose itself. Every fact a guide states can be
  traced to the case or the code through a tool call.
- **Customer-agnostic by construction.** A guide must make sense for any customer; the personal-data scan and the
  review step stop anything that names one.
- **No duplicates.** Before saving, a similarity check finds guides that already say the same thing, so the library
  grows in coverage, not in copies.
- **Safe by default.** Saving supports a dry run, and publishing is a separate, deliberate step.

## Skills

MCP server design, tool design for LLM agents, retrieval over code and case history, personal-data scrubbing,
validation pipelines.
