# Continuation Builder Prompt

Use this prompt when the user wants to infer, outline, or draft what may happen
after chapter 80 without relying on chapters 81-120 as source material.

## Objective

Produce a constrained post-80 continuation based on:

- `corpus/original_texts/chapters/ch001.txt` through `ch080.txt`
- `corpus/annotations/chapters/ch001.txt` through `ch080.txt`
- `corpus/user_notes/open_threads_template.md`
- relevant historical or research notes when they clarify structure rather than
  import a known later continuation

Do not treat the task as recovery of Cao Xueqin's lost original ending.

## Hard rules

1. Do not read or rely on chapters 81-120 unless the user explicitly requests
   comparison with the later continuation tradition.
2. Do not import known Gao E plot points as if they were deduced from chapters 1-80.
3. Do not state or imply "this is what Cao Xueqin actually wrote."
4. Distinguish explicit setup from inference at every important step.

## First-step checklist

Before generating, identify:

- the requested mode
- the relevant open threads from `open_threads_template.md`
- the most important chapters or scenes from 1-80
- whether the user wants analysis, outline, or actual prose
- whether the user wants scholarly register or style-guided imitation

## Supported modes

Choose one mode first, and state it internally:

1. `plot projection`
   Build a likely post-80 event sequence.

2. `thematic continuation`
   Explain how major themes are likely to continue or close.

3. `character destiny map`
   Project likely outcomes for major and secondary figures.

4. `style-guided sequel sketch`
   Write fresh prose guided by first-80 structure and style.

## Evidence procedure

1. Read the relevant entries in `open_threads_template.md`.
2. Pull only the first-80 chapters needed for the current task.
3. Prefer repeated structural signals over one-off details.
4. Check whether commentary or scholarship supports the inference.
5. Rank major claims by confidence:
   - `High` = strongly supported by repeated first-80 patterns
   - `Medium` = plausible and structurally coherent
   - `Low` = interesting but speculative

## Output structure

Unless the user explicitly wants only prose, organize the response with these parts:

### 1. Known Setup

State only what chapters 1-80 clearly establish.

### 2. Open Threads

List the unresolved lines that matter for the requested task.

### 3. Probable Continuations

Project the next-stage developments. Prefer 3-5 strong lines over many weak ones.
If useful, rank them by confidence.

### 4. Boundary Notes

State what remains uncertain, what cannot be deduced, and where the continuation
becomes imaginative reconstruction rather than strong inference.

## If the user wants actual sequel prose

Add a short prefatory note in substance equivalent to:

"The following passage is a constrained sequel sketch derived from chapters 1-80
and related evidence. It is not presented as Cao Xueqin's original text."

Then apply these style controls:

- privilege atmosphere, echo, and indirect judgment
- let household detail carry structural meaning
- avoid modern pacing and explicit thesis statements
- preserve tonal ambiguity where the first 80 chapters preserve ambiguity
- do not over-resolve every relationship or prophecy

## Anti-patterns

Do not:

- collapse Daiyu/Baochai into a crude binary
- turn prophecy into a mechanical spoiler chart
- write a neat moral ending unsupported by first-80 texture
- rely on shock events without prior structural preparation
- confuse imitation with authenticity

## Quick output templates

### Template A: Outline

```text
Mode: plot projection

Known Setup:
- ...

Open Threads:
- ...

Probable Continuations:
1. ...
2. ...
3. ...

Boundary Notes:
- ...
```

### Template B: Scholarly note

```text
Based on chapters 1-80, the strongest continuation pressure falls on three areas:
...

What can be said with relatively high confidence is ...
What remains uncertain is ...
```

### Template C: Sequel sketch

```text
This is a constrained sequel sketch derived from chapters 1-80 and related evidence.
It is not presented as Cao Xueqin's original text.

[prose]
```
