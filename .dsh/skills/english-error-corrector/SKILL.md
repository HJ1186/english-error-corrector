---
name: english-error-corrector
description: "Use when the user supplies English text and asks to check, correct, revise, proofread, or polish it, including requests such as “check my English”, “fix the grammar”, “检查英文错误”, “修改英文”, or “润色英文”. Covers sentences, paragraphs, emails, and essays. Do not use for translation, pure rewriting, or non-English text."
---

# English Error Corrector

Correct only the English text the user provides. Preserve its meaning, tone, and paragraph structure.

## Output format

Your response must begin with the exact line `**错误内容：**` and must contain only the three labeled sections below. Never preface the output with a title, acknowledgement, skill name, input restatement, or any other sentence. Do not add a closing, summary, encouragement, or extra commentary.

**错误内容：**

List one numbered item per distinct error, using exactly this shape:

`1. “original fragment” —— 语法：brief description of the error.`

Replace `语法` with exactly one of `语法`, `拼写`, `搭配`, or `表达`.

**错误内容修改：**

Use the same item numbers and order as above. Each item gives the corrected fragment and exactly one reason sentence, using this shape:

`1. “corrected fragment” —— one sentence explaining the correction.`

**修改后的完整句子：**

Output only the fully corrected text.

## Rules

- **错误内容：** one numbered item per distinct error. Use exactly one of these type labels: 语法 / 拼写 / 搭配 / 表达. Do not include the correction or a rewrite.
- **错误内容修改：** keep strict one-to-one correspondence with 错误内容. State the corrected fragment first, then one reason sentence.
- **修改后的完整句子：** reproduce the whole corrected paragraph, not only the changed fragments. Preserve paragraph breaks and omit notes or labels inside the text.
- Make minimal corrections. Fix clear errors and unidiomatic usage; do not rewrite for style, add information, or change the intended meaning.
- If there are no errors, write `未发现错误。` in 错误内容, `无需修改。` in 错误内容修改, and repeat the original text in 修改后的完整句子.
