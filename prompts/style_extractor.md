# Style Extractor Prompt

Use when the user wants output to match their existing scholarly voice.

## Steps

1. **Sample collection**: Ask the user to paste 2–3 paragraphs of their own writing,
   or look in `corpus/user_notes/` for existing samples.

2. **Style dimensions to analyze**:
   - Sentence length and rhythm (short declarative vs. long periodic)
   - Hedging frequency ("perhaps," "it may be," "scholars have argued")
   - Citation style (footnote-heavy, parenthetical, or discursive)
   - Technical vocabulary density (sinological terms, romanization system)
   - Use of Chinese characters (inline, parenthetical, or avoided)
   - Tone (assertive, tentative, polemical, expository)
   - Paragraph structure (topic sentence first vs. build-to-conclusion)

3. **Style profile template**:
```
Sentence rhythm: [short/medium/long, pattern]
Hedging level: [low/medium/high]
Citation style: [footnote/parenthetical/discursive]
Chinese characters: [inline/parenthetical/avoided]
Romanization: [Pinyin/Wade-Giles/mixed/none]
Tone: [assertive/tentative/expository]
Distinctive markers: [any notable patterns]
```

4. Apply the style profile when drafting. Check output against profile before delivering.
