# Vocabulary System Design for PET Preparation
*AI-assisted framework for distinguishing productive vs receptive vocabulary*

---

## The Core Problem

Standard PET preparation materials treat all 900+ words in the B1 Preliminary 
Vocabulary List equally. This ignores a fundamental distinction made by Cambridge 
itself:

- **Receptive vocabulary** – recognize in reading/listening; no production required
- **Productive vocabulary** – must spell correctly and use accurately in writing and speaking

No mainstream study guide makes this separation. The result: learners waste time 
drilling words they'll never need to write.

---

## The AI-Assisted Solution

Using Claude, we applied three filters to the full 900+ word list:

1. **Cambridge Learner Corpus frequency** – how often does this word appear in 
   actual B1 learner writing?
2. **PET Writing assessment criteria** – the Language dimension directly scores 
   vocabulary accuracy and range
3. **Spelling opacity** – words whose spelling is non-transparent or commonly 
   misspelled under exam conditions

**Result: ~220 words worth active drilling** — roughly 1/4 of the full list.

This filtering is only efficient with AI assistance. Manual curation would take 
days; the AI completed a defensible first-pass in one session.

---

## The 7-Layer Classification System

| Layer | Content | Volume | Practice Method |
|-------|---------|--------|-----------------|
| A | Discourse connectors (contrast / addition / cause / sequence / example / opinion) | ~30 phrases | Internalized through writing tasks |
| B | Core verbs (high output frequency, non-transparent spelling) | 50 words | Post-writing substitution review |
| C | Descriptive adjectives (replacing good/bad/nice) | 28 words | Post-writing substitution review |
| D | High-frequency nouns (essential for email/story tasks) | 22 words | Post-writing substitution review |
| E | Spelling danger zone (double letters, counter-intuitive patterns) | 20 words | 5-word dictation drill, weekly |
| F | Original example sentence bank (scene-based) | 60 sentences | Read aloud daily, 3–5 sentences |
| G | Triple-element synthesis sentences (exam-ready) | 20 sentences | Final sprint phase |

---

## Design Logic: Layers F and G

### The Problem with Template Memorization

Many candidates memorize essay templates during preparation. This creates two risks:
1. Multiple candidates in the same session submit structurally identical writing, 
   triggering similarity flags
2. Generic templates score poorly on the Language dimension — they demonstrate 
   range only in structure, not vocabulary

### The Solution: Memory-Anchored Original Sentences

Instead of templates, we built sentences around specific characters and scenes 
that are personally meaningful to the learner. The sentences are:
- Grammatically B1-appropriate
- Vocabulary-rich (each sentence naturally embeds 2–3 target words)
- Unique — only someone who knows these characters could have written them

### Exam Conversion Mechanism

Characters in the sentence bank are referred to by generic labels (e.g., "the 
dragon", "the dog") rather than personal names. Under exam conditions, the learner 
replaces the generic label with the character name given in the prompt. The 
sentence structure, vocabulary, and tone remain unchanged.

This converts personally memorized sentences into exam-ready responses in under 
5 seconds.

---

## Progress Tracking System

### Principle: 10-Second Maintenance

The tracking system is designed to sustain long-term use. If logging a practice 
session takes more than 30 seconds, compliance drops. The system uses:

**Top-level dashboard** (one screen, 7 rows, always visible)
- Layer A–G status: 🔴 Not started / 🟡 In progress / 🟢 Mostly acquired / ✅ Done
- Last practice date
- Notes

**Folded session logs** (per-layer, expanded only when needed)
- Date / method / result per session
- Weak item tracking: needs reinforcement vs acquired

### Layer E Dictation Schedule (pre-assigned)

| Week | Words |
|------|-------|
| W1 | accommodation / beginning / believe / definitely / embarrassed |
| W2 | environment / immediately / necessary / neighbour / receive |
| W3 | restaurant / separate / successful / tomorrow / certificate |
| W4 | comfortable / occasionally / opposite / practice·practise / whether |

---

## Key Insight

The value of AI in this workflow is not generating content — it is **making 
distinctions that humans would find too tedious to make manually**, at the scale 
required to be useful.

Filtering 900 words against three criteria, building a layered system, and 
generating 80 original sentences took one focused session with Claude. The same 
work done manually would take a subject-matter expert several days.

This is the core argument for AI-assisted exam preparation: not replacement of 
human judgment, but amplification of it.

---

*Part of the `ai-assisted-pet-prep` project*  
*Last updated: 2026-04-04*
