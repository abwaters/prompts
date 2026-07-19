# Design notes — Parolu kun Klara

## The problem I was solving

Esperanto is designed to be learned quickly, but "learnable" and "spoken" aren't the same thing — you still cannot build conversational reflexes without conversing, and for Esperanto the immersion problem is sharper than for major national languages: there simply aren't speakers on every corner. That makes an always-available partner unusually valuable here. Klara is the missing partner: patient, on demand, for as many conversations as it takes until speaking becomes normal.

As with the others, the biggest lever is **volume**, and every decision below serves keeping the conversation going.

## Core decisions (and the default behavior each one fights)

The prompt is written *against* the default LLM instincts that would undermine practice:

- **Conversation is the product** — not lessons. Learning rides inside the conversation.
- **Teach without constantly teaching.** Model the natural form and reuse it; don't stop to explain a rule.
- **Don't correct everything.** Correct only what changes meaning, blocks understanding, or recurs — a deliberate fluency-first trade. When a micro-correction is worth it, it's one line (*"Eta korekto…"*) and then straight back to talking.
- **Don't interview**, **meet the learner silently**, **let them struggle** (English as a bridge, not an escape hatch), and **remember** the conversation — the same load-bearing choices as the other partners.

## Esperanto-specific choices

- **No national accent.** Esperanto belongs to an international speech community, not one country. Klara deliberately avoids imitating any single native language's speech patterns — the target is clear, neutral, internationally understandable Esperanto.
- **Word-building over vocabulary lists.** Esperanto's productive system of roots, prefixes, and suffixes is its superpower, but it's tempting to over-teach it. The choice: demonstrate how roots generate related meanings *in context*, and resist turning every unfamiliar word into a morphology lesson.
- **Accept the x-system.** Learners often can't type ĉĝĥĵŝŭ conveniently, so `cx gx hx jx sx ux` input is accepted naturally, while Klara replies in proper diacritics unless asked otherwise. A small friction-remover that keeps people talking.
- **Selective focus on the real sticking points** — the accusative **-n**, agreement, correlatives, participles, and over-literal translation — rather than drilling grammar just because Esperanto's grammar is regular and drillable.

## Tensions I'm accepting on purpose

- **Fluency over correctness, early**, with the usual under-correction risk mitigated by prioritizing recurring mistakes.
- **Regularity is a trap.** Because the grammar is so systematic, there's constant temptation to *analyze* instead of *converse*. The prompt explicitly pushes back on that — the goal is communication, not admiring the machinery.
- **Standard over stylistic.** Klara accepts valid but unusual word-formation rather than "correcting" it to the common form, but defaults to broadly-understood Esperanto — a bias toward being understood everywhere over being clever.

## What may change

An experiment, not a finished system. Open questions: how much word-building to surface for eager learners without derailing conversation, and how to handle the very wide ability range Esperanto attracts. Suggestions welcome — see the README.
