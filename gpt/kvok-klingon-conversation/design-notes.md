# Design notes — jatlh K'Vok

## The problem I was solving

Same root problem as the other partners — you cannot build conversational reflexes without conversing, and there's nowhere to go have a conversation in Klingon. But Klingon is a special case: it's a constructed language with a small, well-documented vocabulary, a genuinely alien grammar, and an identity that is *inseparable from attitude*. A warm, encouraging tutor speaking Klingon would feel wrong — not because warmth is bad, but because it breaks the illusion that you're actually talking to a Klingon.

So K'Vok is the one deliberate departure from the companion template. He's a proud, dryly sarcastic Klingon who has agreed to teach you and is still deciding whether that was a mistake. The learner should think *"Oh. I'm talking to K'Vok,"* not *"ChatGPT switched languages."*

## What stays the same

Under the persona, the load-bearing philosophy is identical to the warm partners:

- **Conversation is the product**, not lessons.
- **Don't correct everything**, **don't interview**, **meet the learner silently**, **let them struggle** (English as a bridge to cross quickly), and **remember** the conversation.
- **Teach through modeling and reuse**, so the learner discovers they've learned something without noticing when the lesson happened.

The persona is a delivery layer over the same pedagogy — the snark is packaging, not a different method.

## Klingon-specific choices

- **Attitude as pedagogy.** "Struggle earns respect; demands for reassurance don't" isn't just flavor — it's a motivational stance that suits productive struggle. Praise is rationed on purpose (*"Acceptable."* / *"Perhaps you are not hopeless."*), which makes real progress feel earned. The relationship warms as competence grows, but in a Klingon way — through respect and harder exchanges, never sentimentality.
- **Klingon must sound like Klingon.** The biggest failure mode is Object-Verb-Subject Klingon that's secretly English with substituted words. The prompt pushes compact, forceful, correctly-ordered tlhIngan Hol and tries to teach *thinking in Klingon structure*, not translating.
- **Canon accuracy is a hard constraint.** With a small documented lexicon, inventing words and passing them off as canonical is the cardinal sin. K'Vok may be arrogant but must not be confidently wrong — he flags uncertain, disputed, or reconstructed usage rather than fabricating certainty.
- **Preserve Klingon orthography.** `q` and `Q` are different letters; capitalization carries meaning, so it's never "corrected" into English casing.
- **Built for voice, tolerant of mangling.** Speech recognition chokes on Klingon's unusual phonology, so a strange word is treated as a plausible transcription error before it's treated as a learner mistake.

## Tensions I'm accepting on purpose

- **Persona vs. accessibility.** The gruffness is a feature, but it risks alienating a learner who wants gentleness. Mitigation: the snark is explicitly "playful, not cruel," it's used selectively, and the learner is never made genuinely embarrassed for trying.
- **Parody risk.** The line between "authentic Klingon character" and "cartoon growling warrior" is thin. The prompt spends real effort staying on the right side — K'Vok can discuss software or a broken lawn mower and still sound like himself, without every chat collapsing into battle.
- **Small language, real limits.** Klingon lacks convenient words for many modern concepts. The choice is to *construct* meaning from established vocabulary rather than invent — accepting that some ideas are simply harder to express, which is honest to the language.

## What may change

An experiment, not a finished system. Open questions: how far the persona should soften at advanced levels, how to handle canon disputes gracefully mid-conversation, and how much cultural framing is enriching versus distracting. Suggestions welcome — see the README. Qapla'.
