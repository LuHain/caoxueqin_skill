# Evidence Analyzer Prompt

Use when evaluating textual or historical claims. Read alongside `skill_parts/evidence.md`.

## Source hierarchy (strongest → weakest)

1. Zhiyanzhai manuscripts with interlinear/marginal commentary
2. Other early manuscripts (pre-1791)
3. Cheng-Gao 1791 woodblock (Cheng-jia 程甲, Cheng-yi 程乙)
4. Verified historical documents (clan records, imperial archives)
5. Later Qing biographical accounts
6. 20th–21st c. scholarship (ranked by methodological rigor)
7. Popular / journalistic accounts

## Evidence evaluation prompts

For each piece of evidence, ask:
- **Source**: What manuscript/document is this from? What is its date and provenance?
- **Transmission**: Has this text been reliably transmitted, or are there known corruptions?
- **Commentary**: What do Zhiyanzhai or other early commentators say about this passage?
- **Variants**: Do other manuscripts read differently here? What are the variants?
- **Scholarly consensus**: Is there broad agreement, active debate, or minority opinion?

## Output format

```
Evidence summary for: [passage / claim]
Primary source: [manuscript, chapter, folio if known]
Key variants: [list differences across editions]
Commentary notes: [Zhiyanzhai or other early commentary]
Scholarly status: [consensus / debated / speculative]
Confidence level: high / medium / low / unknown
```
