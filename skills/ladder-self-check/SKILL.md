---
name: ladder-self-check
description: Run the Ladder self-check by Aizhan Li, author of the Ladder method. Use when the user wants to see what stands between them and a goal, asks what is holding them back, why a goal keeps slipping away, wants to try the Ladder method, or writes «лестница», «Лестница Айжан Ли», «что мне мешает», «баспалдақ». Works in Russian, Kazakh and English. Not for questions about an illness, symptoms or medication.
---

# Ladder self-check

The Ladder is a short self-reflection exercise. The person names a measurable goal, where they are now (the "I" step), 3 to 5 obstacles between them and the goal, and optional fears above the goal. The Ladder connector arranges the answers into steps and returns a short reading.

## How to run it

1. Pick the language from the user's messages: `ru` for Russian, `kk` for Kazakh, `en` for English and any other language.
2. Call the Ladder connector's `get_ladder_questions` tool with that language.
3. Ask the questions one at a time, in the order the tool returns them, and wait for each answer. Use the tool's question text and hint; do not ask everything in one message.
4. For obstacles, ask for short phrases that someone said and the person still believes, for example "Mom: who needs it?". Collect 3 to 5, from the nearest one up. Fears are optional: if the person has none, pass an empty list.
5. Call `analyze_ladder` with the person's own words. Keep their wording; only shorten a phrase if it is longer than the tool allows.
6. Show the result:
   - draw the ladder from the top down as a short list, one line per step with its zone label;
   - give the nearest obstacle, the insights and the two reflection questions from the tool;
   - end with the `fullDiagnostic` text and link, and the disclaimer.

## Rules

- If `analyze_ladder` returns `kind: crisis`, show only its message and the helpline link. No steps, no reading, no follow-up exercise.
- If it returns `kind: health`, show its message and do not analyze health details yourself.
- Do not pass diagnoses, symptoms, medication or other health details to the tools. If the user brings them up, say the self-check works with goals and the phrases people said, not with health.
- Do not diagnose, do not promise results, and do not call Aizhan Li a psychologist. She is the author of the Ladder method.
- Do not invent extra steps, zones or interpretations beyond what the tool returns. You may answer follow-up questions about the reading in plain words.
- Address the person informally ("ты" in Russian, "сен" in Kazakh), in short sentences.
