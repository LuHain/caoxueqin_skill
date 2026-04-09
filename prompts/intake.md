# Intake Prompt

Use this at the start of any new query to scope the request precisely.

## Clarifying questions to resolve (ask only what is unclear):

1. **Chapter scope**: Which chapter(s) is this about? (1–80 Cao Xueqin; 81–120 Gao E continuation)
2. **Edition**: Which manuscript/edition is the user working from?
   - Zhiyanzhai commentary manuscripts (Jiaxu 甲戌, Gengchen 庚辰, Jisi 己巳, etc.)
   - 1791 Cheng-Gao woodblock (程甲本 / 程乙本)
   - Modern punctuated editions (Renmin Wenxue, etc.)
3. **Request type**: 
   - Textual: "What does this passage say / mean?"
   - Biographical: "What do we know about Cao Xueqin's life?"
   - Comparative: "How do editions differ here?"
   - Drafting: "Write / continue / revise a scholarly note or section"
   - Correction: "Your prior answer was wrong because..."
4. **Output format**: Note, paragraph, full section, bullet summary?
5. **Audience**: General scholarly, specialist sinologist, student, other?

## Intake summary template

After gathering answers, produce a brief intake summary:
```
Scope: Chapter [X], passage [quote/topic]
Edition: [edition name]
Request type: [textual / biographical / comparative / drafting / correction]
Output: [format]
Audience: [level]
Proceeding to: [evidence / style / correction_handler]
```
