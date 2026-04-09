# Cao Xueqin Research Skill

A structured skill for scholarly work on *Dream of the Red Chamber* (红楼梦)
by Cao Xueqin (曹雪芹), including annotation, interpretation, manuscript comparison,
and constrained post-80 continuation work.

Current local path:

`/Users/hain/Documents/GitHub/caoxueqin_skill`

## What this skill does

- Annotates chapters with textual, historical, and interpretive notes
- Compares manuscript traditions such as Zhiyanzhai commentaries, Gengchen, and Jiaxu
- Drafts scholarly sections, essays, and research notes
- Handles contested readings and tracks corrections over time
- Extracts and matches the user's scholarly writing style
- Supports constrained post-80 projection based only on chapters 1-80 and related evidence

## Directory structure

```text
caoxueqin_skill/
├── SKILL.md                    <- Main skill entry point
├── README.md                   <- This file
├── CALL_CARD.md                <- Fast invocation phrases
├── prompts/                    <- Reusable prompt templates
│   ├── intake.md
│   ├── evidence_analyzer.md
│   ├── interpretation_analyzer.md
│   ├── style_extractor.md
│   ├── continuation_builder.md
│   └── correction_handler.md
├── corpus/                     <- Research materials
│   ├── original_texts/         <- Chapter texts and editions
│   ├── annotations/            <- Prior annotation layers
│   ├── historical_records/     <- Biographical and archival materials
│   ├── research/               <- Secondary scholarship
│   └── user_notes/             <- Working notes, including open threads
├── skill_parts/                <- Modular instruction sets
│   ├── evidence.md
│   ├── interpretation.md
│   ├── style.md
│   ├── continuation.md
│   └── guardrails.md
└── outputs/                    <- Generated content
    ├── chapter_notes/
    └── draft_sections/
```

## How to use this skill

### 1. General scholarly use

Use `caoxueqin-skill` when the task involves:

- chapter reading or annotation
- textual variants and manuscript comparison
- Cao Xueqin biography and evidentiary status
- character analysis
- redology interpretation
- style-matched scholarly drafting

Example calls:

```text
用 caoxueqin-skill，帮我解读第5回这一段，并注明依据。
```

```text
用 caoxueqin-skill，比较庚辰本和甲戌本这里的异文。
```

```text
用 caoxueqin-skill，用 scholarly note 的方式写一段关于黛玉病体意象的分析。
```

### 2. Constrained post-80 continuation use

When asking for post-80 inference, projection, outline, or sequel prose, state the
constraint clearly:

- use `caoxueqin-skill`
- do not read the later 40 chapters
- base the work on chapters 1-80, annotations, and `open_threads_template.md`

Strong default call:

```text
用 caoxueqin-skill，按前80回正文、前80回脂批和 open_threads_template，禁止读取后40回，先列 Known Setup / Open Threads / Probable Continuations / Boundary Notes，再写后续大纲。
```

Useful variants:

```text
用 caoxueqin-skill，不读后40回，只推演宝玉和黛玉在80回后的走向。
```

```text
用 caoxueqin-skill，不读后40回，给我一个 10 到 12 回的详细续写分回提纲。
```

```text
用 caoxueqin-skill，不读后40回，按 continuation_builder prompt 写一段 post-80 的续写草稿。
```

Helpful add-ons:

- `只做大纲，不写正文。`
- `先列 Known Setup / Open Threads / Probable Continuations / Boundary Notes。`
- `用 scholarly note 的方式写。`
- `用 style-guided sequel sketch 的方式写。`
- `只用前80回能支持的内容，不要装作知道原作结局。`

### 3. Comparative use with the later 40 chapters

By default, continuation tasks should not read or rely on chapters 81-120.

Read or compare the later 40 chapters only when the user explicitly asks for:

- comparison with Cheng-Gao / Gao E continuation materials
- differences between a first-80 projection and the transmitted later ending
- stylistic or structural comparison between the two

Example comparative call:

```text
用 caoxueqin-skill，对比前80回约束下的宝黛后续推演，和资料里后40回的处理有什么不同。
```

## Workflow summary

The skill follows this path:

`intake -> evidence -> interpretation -> style -> continuation -> guardrails -> output`

Quick guidance:

- Read `SKILL.md` for the full operating contract.
- Use `CALL_CARD.md` for ready-made continuation prompts.
- Use `corpus/user_notes/open_threads_template.md` when doing post-80 projection work.
- Save outputs to `outputs/chapter_notes/` or `outputs/draft_sections/` as appropriate.

## Continuation guardrails

When working in first-80 continuation mode:

- Treat chapters 1-80 as the primary narrative base.
- Treat early commentary and annotations as the primary commentary base.
- Do not smuggle Gao E plot points into the answer unless comparison is explicitly requested.
- Do not present any projection as "what Cao Xueqin definitely wrote."
- Distinguish between explicit setup, strong inference, weak projection, and open uncertainty.

The goal is bounded reconstruction, not recovery of a supposedly fixed lost original.

## Notes on the later 40 chapters

This repository may include chapters 81-120 in `corpus/original_texts/chapters/`.
For continuation tasks, those chapters are restricted materials unless the user asks
for direct comparison.

When direct comparison is requested, a useful framing is:

- chapters 1-80 support structural pressure, tonal drift, and open-ended inference
- chapters 81-120 often convert those pressures into explicit event chains and settled outcomes

## Example: difference between a first-80 Baoyu-Daiyu projection and the transmitted later 40 chapters

If we project Baoyu and Daiyu's post-80 trajectory using only the first 80 chapters,
the likely emphasis is:

- the garden atmosphere cools before decisive events occur
- Baoyu and Daiyu become spiritually closer while reality makes them harder to unite
- Daiyu turns further inward through illness, compression, and emotional restraint
- Baoyu's later transformation is driven by loss, belated recognition, and disillusion
- the relationship reaches completion through non-fulfillment rather than tidy resolution

By contrast, the transmitted later 40 chapters tend to:

- turn structural pressure into a fixed event sequence
- settle the Baoyu-Daiyu-Baochai line through explicit marriage misdirection and death
- make the tragedy more theatrical and more determinate
- move Baoyu back toward a more managed domestic order after the shock
- give sharper closure where the first 80 chapters often preserve ambiguity

### In short

The first-80 method asks:

- What does the text strongly set up?
- What remains unresolved?
- What can be responsibly inferred without pretending to know the ending?

The later 40 chapters answer a different question:

- How can these pressures be converted into a concrete, transmitted ending?

That is why a first-80 constrained projection is usually more open, more tonal, and
more cautious than a summary of the later continuation text.

## Getting started

1. Put source materials in the appropriate `corpus/` subdirectory.
2. Decide whether the task is evidentiary, interpretive, stylistic, or continuation-based.
3. If it is a continuation task, say explicitly whether the later 40 chapters are forbidden or being compared.
4. Start with a direct prompt using `caoxueqin-skill`.

For fast prompt templates, see:

- `/Users/hain/Documents/GitHub/caoxueqin_skill/CALL_CARD.md`
- `/Users/hain/Documents/GitHub/caoxueqin_skill/SKILL.md`
