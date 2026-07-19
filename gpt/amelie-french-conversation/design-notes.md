# Design notes — Parle avec Amélie

## The problem I was solving

I know a fair amount of French. What I don't have is immersion. There's a real gap between *knowing* a language and being able to *use* one — knowledge versus reflexes — and you cannot build the reflexes without having conversations. The usual tools build the knowledge and then leave you with no one to talk to at 7:15 on a Tuesday morning. Amélie is the missing partner: patient, available, and willing to have the hundredth and thousandth conversation until speaking simply becomes normal.

The biggest lever is **volume**. Everything below serves keeping a real conversation going long enough, and often enough, for reflexes to form.

## Core decisions (and the default behavior each one fights)

The prompt is largely written *against* the default LLM instincts that would undermine practice:

- **Conversation is the product** — not lessons. Learning rides inside the conversation; when teaching would interrupt a good exchange, the exchange wins.
- **Teach without constantly teaching.** Model the correct form in a natural reply and reuse it, instead of stopping to explain a rule.
- **Don't correct everything.** A deliberate accuracy-for-fluency trade: correct only what changes meaning, blocks understanding, or recurs. Producing sentences at all comes first.
- **Don't interview.** No question after every turn. React, observe, or wait — real conversation breathes.
- **Meet the learner silently.** No placement test, no announced level; gauge and adjust from the conversation itself.
- **Let the learner struggle.** English is a bridge used sparingly, not an escape hatch triggered by a moment's hesitation.
- **Remember.** Continuity — the people, the threads, the interests — is what makes it feel like a person rather than a tool.

## French-specific choices

- **Default to *tu*.** The whole point is relaxed, frequent, personal conversation, and *vous* sets the wrong temperature for that. It shifts to *vous* on request or when formality genuinely calls for it, and will briefly explain register when useful — because *tu*/*vous* is exactly the kind of thing a learner needs to feel, not memorize.
- **Pronunciation is intelligibility-first**, with selective attention to rhythm, liaison, and connected speech — the features that make spoken French click — rather than correcting every sound in flight.
- Contemporary standard French, gradually introducing common spoken forms in context so the learner meets real French, not textbook French.

## Tensions I'm accepting on purpose

- **Fluency over correctness, early.** An explicit bet that free-but-messy beats perfect-but-silent.
- **Under-correction risk.** Errors can fossilize; the mitigation is prioritizing recurring mistakes, not catching every one.
- **Register as feel, not rule.** Leaning on *tu* and modeling register in context means less explicit instruction — intentional, but it asks the learner to absorb rather than be told.

## What may change

An experiment, not a finished system. Open questions: how fast to escalate correction as fluency grows, how to handle cross-session memory, and whether spoken-form exposure should ramp faster. Suggestions welcome — see the README.
