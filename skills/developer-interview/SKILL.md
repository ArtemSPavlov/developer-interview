---
name: developer-interview
description: Runs a developer interview in three phases — job description, one-question-at-a-time Q&A with follow-ups, then a competency scorecard and the topics the candidate should improve. Triggers: "conduct an interview", "developer interview", "assess a candidate", "interview a developer".
---

# Developer Interview

Three phases: JD → Q&A → report. Do not mix or skip them.

## 1. Input

Ask for the job description (text, link, or screenshot) — the only required item. Everything else does not block the start:

- candidate resume;
- level (junior / middle / senior);
- stack and session length (default 45 minutes, ~10 questions);
- interview language (defaults to the language of the job description; override only if the user asks).

If the JD is vague — 2–3 clarifying questions, then start. Do not turn intake into a questionnaire.

## 2. Preparation (do not show the user)

Use the competency structure and scorecard from the `interview-prep` skill (Anthropic knowledge-work-plugins) if installed. Otherwise use the scale below. Build:

- 4–6 competencies from the JD (language/framework, design, debugging, testing, communication, etc.);
- 2 questions per competency + a follow-up for each;
- for each question — what it checks and what counts as a strong vs weak answer.

Ask behavioral and situational questions ("tell me about a time…", "what would you do if…"), not API trivia. If a resume is available — 1–2 questions about specific experience from it.

Scale: 1 — no answer or wrong, 2 — generalities with no experience, 3 — working experience with gaps, 4 — strong independent experience and conscious trade-offs.

## 3. Session

- One question per message, wait for the answer.
- Do not give scores, hints, or correct answers during the session.
- Follow up when the answer is generic, has a logical gap, or touches interesting experience. At most 3 levels deep.
- Commands: "skip", "pause", "stop" (stop → report on what exists).
- Keep the timebox: the competencies most important for the role come last.

## 4. Report

After the session or "stop":

1. **Competencies** — table: score 1–4 and evidence (quote or fact from the answer). No inflation: do not give everyone 3 out of 4.
2. **Strengths** — 2–3 points with evidence.
3. **Topics to improve** — up to 5, sorted by impact on the role: topic, why it failed, what exactly to learn, how to verify progress (question or task).
4. **Verdict** — hire / no-hire / one more interview needed, and what was missing for a decision.

Write in the language of the job description, unless the user explicitly chose another interview language. Do not invent the candidate's experience or fill gaps with guesses — mark as "not verified".
