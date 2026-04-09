# Caoxueqin Skill Call Card

Use these prompts to invoke the skill for post-80 continuation work under
first-80 constraints.

## Core rule

If the task is continuation, state clearly:

- use `caoxueqin-skill`
- do not read the later 40 chapters
- base the work on chapters 1-80, annotations, and `open_threads_template.md`

## Quick calls

### 1. Continuation outline

```text
用 caoxueqin-skill，不读后40回，写后续大纲第一版。
```

### 2. Plot projection

```text
用 caoxueqin-skill，按前80回正文、脂批和 open_threads_template，不读取后40回，做一个 plot projection。
```

### 3. Character projection

```text
用 caoxueqin-skill，不读后40回，只推演宝玉在80回后的走向。
```

### 4. Thematic continuation

```text
用 caoxueqin-skill，不读后40回，推演贾府衰败这条主线在80回后的发展。
```

### 5. Sequel prose

```text
用 caoxueqin-skill，不读后40回，按 continuation_builder prompt 写一段 post-80 的续写草稿。
```

### 6. Chapter-by-chapter outline

```text
用 caoxueqin-skill，不读后40回，给我一个 10 到 12 回的详细续写分回提纲。
```

## Best-practice add-ons

Add one more phrase when needed:

- `只做大纲，不写正文。`
- `先列 Known Setup / Open Threads / Probable Continuations / Boundary Notes。`
- `用 scholarly note 的方式写。`
- `用 style-guided sequel sketch 的方式写。`
- `只用前80回能支持的内容，不要装作知道原作结局。`

## Strong default call

```text
用 caoxueqin-skill，按前80回正文、前80回脂批和 open_threads_template，禁止读取后40回，先列 Known Setup / Open Threads / Probable Continuations / Boundary Notes，再写后续大纲。
```
