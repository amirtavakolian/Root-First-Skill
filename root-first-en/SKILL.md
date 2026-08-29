---
name: root-first
description: "Use this skill whenever the user types the command \"/root-first\" followed by a word or term (usually a technical/programming concept like \"interface\", \"polymorphism\", \"abstraction\"). The user wants a deep etymology-first breakdown of the word BEFORE learning the actual concept it names — this is their personal learning method: understand where a word came from and what image the coiner had in mind, so the technical meaning clicks intuitively afterward. Always trigger this on the pattern \"/root-first\" followed by a word, even if the user gives no other context."
---

# Root First — Etymology-First Concept Primer

## Overview

The user has a specific learning habit: before diving into a technical concept (usually object-oriented programming or CS terms), they want to understand the **etymology of the word itself** — what root words it's built from, and what mental image or metaphor the person who coined/chose the word had in mind. This makes the later technical definition feel intuitive and "obvious" instead of arbitrary.

This skill is triggered by: `/root-first` followed by a word — e.g. `/root-first interface`.

**Important**: at the initial etymology stage, the user only wants the word's origin, the imagined metaphor, and real-world examples grounded in that metaphor — NOT a full explanation of the technical/domain concept itself. Do not explain the concept in depth at that point. That deeper explanation only happens later, after the user answers the domain question (see step 8), and even then it must stay explicitly anchored to the etymology already given rather than becoming a generic textbook definition.

## Response Language

The response should be written in English. Respond in English, in the tone of a knowledgeable, enthusiastic friend explaining something cool — not a dry dictionary printout.

## Instructions

### 1. Search the web, prioritizing etymonline.com

Run a web search specifically for "[the word] etymology etymonline". Etymonline is the primary/preferred source — always check it. Also let secondary sources surface naturally (Merriam-Webster, Wiktionary, OED) since they sometimes add a clarifying detail or a good illustrative phrase (like Merriam-Webster's habit of giving a plain-English gloss of the root meaning) — pull those in only if they add real value, don't pad.

If the word has a related base form worth checking too (e.g. the noun AND the verb, like "encapsulate" vs "encapsulation", or "abstract" vs "abstraction"), search for both — the etymology of the shorter/verb form is often more informative than the noun form's entry.

### 2. Break the word into its root pieces

Identify every morpheme (prefix / root / suffix) and give the plain-English meaning of each piece individually. Note the language of origin (Latin, Greek, Old French, etc.) for at least the core root — this is often the most interesting part.

### 3. Give the literal, original meaning

State clearly what the word meant literally when it first entered English (with the approximate century/year etymonline gives), before any figurative or technical usage existed.

### 4. Flag the moment it turned figurative/abstract, if there is one

Many technical terms were literal/physical words first (e.g. "encapsulate" = physically enclosing something in a capsule) and only later, often centuries later, picked up a figurative/abstract sense that eventually got borrowed into technical/CS vocabulary. If etymonline notes a "figurative use by [year]" or a similar shift, call this out explicitly — it's usually the bridge that explains why programmers later grabbed the word.

### 5. Reconstruct "what was in the coiner's head"

This is the heart of the response. Using the root meanings and the concrete imagery of the literal sense, describe the mental picture or metaphor a person would have had in mind when choosing this word — as if reverse-engineering their intuition. Ground this description in the actual root meanings, don't invent unrelated imagery. Use a short vivid analogy or example where it helps (a physical object, an action) — concrete beats abstract here.

### 6. Give 5 real-world examples, each as a problem → solution pair

This step is required, not optional. Provide exactly **5 distinct real-world examples** where the concept itself is actually used to solve something. Each example MUST follow this exact shape:

1. **State a concrete problem** — a real situation, in any domain (not necessarily technical), where something goes wrong or is hard without the concept.
2. **State the solution** — how applying the concept (using it, in a genuine instance of it) resolves that specific problem.

The concept must be *actually at work* in the example, not just mentioned in passing. Don't write vague or generic scenarios — pick concrete, recognizable situations (a real kind of tool, system, job, or everyday scenario) where a reader would immediately go "oh, that's a real problem, and I see how that idea fixes it." Vary the examples — don't make all 5 come from the same narrow field; draw from different walks of life (e.g. one from software, one from everyday objects, one from an organization/process, one from nature/biology if it fits, one from another domain entirely) unless the concept is so domain-specific that variety isn't possible.

Keep each example to 1–3 sentences: problem, then solution. Don't over-explain.

### 7. End with exactly two closing questions

After the real-world examples (and the optional comparison to an earlier word, if applicable), close with **two separate questions**, always naming the word itself in each question:

**Question 1 — domain application.** Ask the user which domain/field they have in mind where this word/concept is used, so that the concept can be explained *in that domain*, explicitly grounded in the etymology just given, with domain-specific examples. Something like (adapt naturally, always include the actual word): "Given the root meaning I just gave you for '[word]', which domain do you want to see this concept applied in? Tell me, and I'll explain it there while explicitly tying it back to that same root, with examples specific to that domain."

**Question 2 — comparison.** Ask whether there's another concept they want to compare against this one. Something like: "Is there another concept you'd like to compare against '[word]'?"

Ask both questions in the same closing message, as two distinct, clearly separated lines/bullets — don't merge them into one question. Do not explain the technical/domain meaning of the term proactively here — wait for the user's answer to Question 1.

### 8. Handling the domain-application answer (Question 1)

If the user names a domain/field (e.g. "artificial intelligence", "networking", "object-oriented programming"):

1. Explain what the word/concept means **specifically within that domain**, but the explanation must **explicitly reference back** to the etymology already given — the root meanings, the literal original sense, and/or the mental image reconstructed in step 5. Draw the connecting line out loud: point to the specific root/imagery and show how the domain's actual usage of the term still carries that same core idea. Don't just give a generic domain definition that happens to use the word — the whole point is to show the reader "see, this is exactly that root metaphor, just applied here."
2. Then give **5 real-world examples from that specific domain**, following the exact same problem → solution format as step 6: state a concrete problem that exists in that domain, then state how using the concept solves it. All 5 examples here must come from the domain the user named — this is what makes them different from the general-purpose 5 examples given in step 6. Keep each to 1–3 sentences.
3. After this domain explanation and its 5 examples, it's fine to still leave Question 2 open if the user hasn't answered it yet (or re-ask lightly if it makes sense), since the two questions are independent and can be answered separately or together.

### 9. Handling the comparison answer (Question 2)

If the user responds with another word/concept to compare:

1. Treat the new word exactly like a fresh `/root-first` invocation — run the FULL process from step 1 through step 6 for this new word (search etymonline, break into roots, literal meaning, figurative shift if any, reconstruct the mental image, and give its own 5 real-world problem → solution examples). Give it its own full write-up, don't shortcut it just because a comparison is coming.
2. After that full write-up, add a dedicated comparison section between the first concept and this new one. **Always explicitly state the relationship/connection between the two** — don't just list differences side by side; say how they relate, overlap, complement, or contrast, grounded strictly in the two words' actual root metaphors/imagery. If the two metaphors genuinely don't relate, say that plainly, but still attempt to articulate why they end up in similar or different technical contexts despite that.
3. End this response with the same two closing questions from step 7, adapted to the new word, in case the user wants to keep chaining.

If the user declines either question (says no / moves on to something else), just drop that thread — no forcing.

## Output Format

ALWAYS use these exact templates depending on the stage of the conversation.

**For a single word:**
```
## Word Roots
(root breakdown + language of origin + literal original meaning)

## Interesting Twist  [optional — only if there's a notable figurative-shift or historical quirk]
(the figurative turn, or any surprising twist in the word's history)

## What Was In the Coiner's Head?
(the reconstructed mental image / metaphor, grounded in the roots)

## Real-World Examples
1. **Problem:** ... **Solution:** ...
2. **Problem:** ... **Solution:** ...
3. **Problem:** ... **Solution:** ...
4. **Problem:** ... **Solution:** ...
5. **Problem:** ... **Solution:** ...

[optional short comparison to a previously-covered word, if relevant]

[Question 1: which domain do you want this explained in, referencing the etymology]
[Question 2: any other concept you want to compare with this one]
```

**For a domain-application answer:**
```
## [Word] in [Domain]
(domain-specific explanation, explicitly tied back to the roots/imagery from the etymology section)

## Real-World Examples in [Domain]
1. **Problem:** ... **Solution:** ...
2. **Problem:** ... **Solution:** ...
3. **Problem:** ... **Solution:** ...
4. **Problem:** ... **Solution:** ...
5. **Problem:** ... **Solution:** ...
```

**For a comparison follow-up (second word)**, repeat the single-word template above (including its own 5 Real-World Examples) for the new word, then append:
```
## Comparison with "[first word]"
(explicit statement of the relationship/connection between the two, grounded in their root metaphors)
```

## Quality Bar

- Cite concrete facts (years, source words, literal meanings) pulled from the actual search results — don't fabricate etymology.
- Keep it concrete and vivid, not academic-dry. The goal is a mental "click", not a dictionary entry.
- Keep total length proportionate to how rich the word's history is — don't pad a simple word's origin into something bloated.
- Every real-world example must be a genuine instance of the concept doing work to solve a stated problem — not a sentence that merely name-drops the word.