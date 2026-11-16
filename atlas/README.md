# Atlas — code explained for support staff

**Role:** designer and developer (2026 – present).

## The problem

Many customers run their own customisations on top of an enterprise product, written in C#. When one of them
misbehaves, a support analyst has to understand what that custom code does, which usually means waiting for a
developer to read it.

## What it does

Atlas is a set of **Claude Code commands** that read a customer's customisation and explain it in plain English:
what it changes, when it runs and what it touches, so that support staff can understand custom code without
waiting for a developer.

## Design choices

- **Commands, not a chatbot.** Each command does one job with a fixed shape of answer, so explanations are
  consistent from one analyst to the next.
- **Plain English for non-developers.** The output is written for support staff, not for programmers.
- **Read-only.** The commands read and explain; they change nothing.

## Skills

Claude Code custom commands, prompt design, LLM code comprehension, writing for a non-technical audience.
