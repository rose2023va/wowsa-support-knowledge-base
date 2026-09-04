# Certificate/credential not received after completing the course

## What it is

Customer says they finished the course but never got their certificate or credential. This has a known, specific, recurring root cause, check it before anything else.

## Known bug pattern: manually-graded quiz silently stalls certification

The Safe Coach Risk Management module's documentation-submission quiz (Kajabi lesson `2199374267`, quiz media `1516302`, tag `SC-RM-Q4`, module "S4 — Documentation" in course `2149536037`) contains open-response/upload questions, so Kajabi marks it **graded manually**. The `SC-RM-Q4` tag only fires once an admin actually grades the submission. If nobody grades it, no tag fires, which means: no Airtable assessment result, no "Course Requirement Satisfied," no credential issued. The learner just sits there with no error and no alert to anyone. This stalled 8 learners for up to 2 weeks the last time it was checked.

**Safe Organizer Foundations has the equivalent quiz (`SO-RM-Q4`, "S4 Quiz — Documentation Submission") and almost certainly behaves identically.**

## How to recognize it

"I finished the course but don't have my certificate," "it's been X days since I completed everything."

## Where to check

1. First, in **WOWSA Education & Credentials** (`appm0S89Eu53KWqXc`), check the learner's Course Completions / Assessment records for the `SC-RM-Q4` (or `SO-RM-Q4`) tag/result specifically. If it's missing while other module tags (Q1/Q2/Q3/Q5) are present, this is almost certainly the cause.
2. In Kajabi, check whether the learner's Q4 submission is sitting ungraded in the manual-grading queue for that quiz.
3. Cross-check "Paired Course URL / Paired Course Name" lookups if the learner is asking about the wrong-seeming course link, there's a known crossed-lookup issue (an SC-DM record can show Risk Management as its paired course and vice versa) — harmless to eligibility but can send the wrong link in an automated email.

## How to answer

- If the Q4 submission is ungraded: grade it (or ask whoever handles grading to prioritize it), then check that the tag fires and `EDU-SYS-01` issues the credential. Tell the customer you found the hold-up and it's being resolved, with a realistic timeline.
- If everything looks correctly tagged/graded and the credential still didn't issue, don't guess further, escalate.

## Escalate if

- The Q4 tag is present and graded but the credential still wasn't issued (this points to `EDU-SYS-01` failing on a different field mismatch, which has happened before due to a singleSelect choice-name mismatch, and needs Rose to check the automation directly, not something fixable from the support side).
- The learner disputes the grading outcome itself, not just the delay.
