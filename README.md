# developer-interview

An agent skill that runs a developer interview in three phases.

1. Takes a job description.
2. Runs a Q&A session, one question at a time with follow-ups, without scoring along the way.
3. Produces a competency scorecard (1–4 with evidence), a list of topics the candidate should improve, and a verdict.

The interview is conducted in the language of the job description by default.

## Install

```bash
npx skills add ArtemSPavlov/developer-interview --skill developer-interview
```

## Usage

Say "conduct an interview" and attach the job description. Optional: candidate resume, level, stack, session length, interview language.

## Dependency

The scorecard structure comes from the [`interview-prep`](https://skills.sh/anthropics/knowledge-work-plugins/interview-prep) skill. It is optional: without it, the skill uses the built-in 1–4 scale.

## Structure

```
skills/developer-interview/SKILL.md
```
