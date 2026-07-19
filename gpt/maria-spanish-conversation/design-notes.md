# Design notes — Conversaciones con María

## The problem I was solving

I know a fair amount of Spanish. What I don't have is anyone to speak it with. There's a real gap between *knowing* a language and being able to *use* one — the first is knowledge, the second is reflexes, and you cannot build the reflexes without actually having conversations. Traditional tools (audio courses, vocabulary decks, grammar books) build the knowledge and then leave you stranded at the water's edge. María exists to be the missing partner: someone patient to talk to, on demand, for as many conversations as it takes.

The single biggest lever is **volume**. Hundreds of conversations, potentially thousands — enough repetition that speaking stops feeling like a performance and starts feeling normal. Every design decision below is downstream of "keep the conversation going long enough, and often enough, for that to happen."

## Core decisions (and the default behavior each one fights)

Most of the prompt is written *against* a default LLM tendency that would quietly sabotage practice:

- **Conversation is the product** — not lessons. The learning rides along inside the conversation. When teaching would interrupt a good exchange, the exchange wins.
- **Teach without constantly teaching.** The reflex to explain a grammar rule every time is the enemy of flow. Prefer modeling the correct form in a natural reply and reusing it later.
- **Don't correct everything.** This is a deliberate accuracy-for-fluency trade. Correct only what changes meaning, blocks understanding, or recurs. The first goal is producing sentences *at all*; accuracy improves inside that process.
- **Don't interview.** LLMs love to end every turn with a question — an interrogation with good manners. Real conversation breathes, so sometimes react, observe, or just wait.
- **Meet the learner silently.** No placement test, no "I estimate you're B1." Level is gauged from the conversation and adjusted quietly.
- **Let the learner struggle.** Retrieval difficulty is the exercise. English is a bridge, used sparingly — not an automatic escape hatch the moment someone hesitates.
- **Remember.** Nothing feels more artificial than re-asking for something you were just told. Continuity is what makes it feel like a person.

## Spanish-specific choices

- Standard, broadly understandable contemporary Spanish rather than a single strong regional register — the goal is a partner most learners can carry into the real world, not an accent cosplay.
- Pronunciation help is selective and intelligibility-first, not a phonetics course interrupting every sentence.

## Tensions I'm accepting on purpose

- **Fluency over correctness, early.** A learner who speaks messily but freely is ahead of one who speaks perfectly but rarely. That's an explicit bet.
- **Under-correction risk.** Errors can fossilize if never addressed. The mitigation is "recurring mistakes get priority," not "every mistake gets caught."
- **No level dashboard.** Some learners want to see progress numbers. I traded that legibility for a more natural experience.

## What may change

This is an experiment, not a finished system. Open questions: how aggressively to escalate correction as a learner advances, how to handle very long-term memory across sessions, and whether the personality should shift as familiarity grows. Suggestions welcome — see the README.
