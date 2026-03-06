---
name: english-lesson-generator
description: Generates professional English lesson materials for intermediate Brazilian Portuguese speakers. Use when requested to create a new class, lesson, or teaching material following the project's multi-step workflow and Bootstrap-based HTML format.
---

# English Lesson Generator

This skill guides the creation of high-quality, print-optimized English lessons for intermediate (B1-B2) students who are native Brazilian Portuguese speakers.

## Workflow (Multi-Step Generation)

When generating a new lesson, follow this sequence and **stop for human review after each step**.

### Step 1: Lesson Outline & Alignment
- **Theme:** Identify a relevant topic (e.g., Food, Health, Shopping).
- **Grammar Topic:** Select a grammar focus (refer to `references/project-standards.md` for priority suggestions).
- **Goals:** 2-3 specific objectives in Portuguese with English key terms.
- **Approval:** Request user confirmation before proceeding.

### Step 2: Core Content Development
- **Vocabulary:** 15-25 terms with example sentences.
- **Disambiguation:** Compare 1-2 confusing terms (e.g., *Customer* vs. *Client*).
- **Slangs & Idioms:** 3-4 relevant expressions.
- **Abbreviations:** 4-6 acronyms related to the theme.
- **Approval:** Request user confirmation.

### Step 3: Grammar & Exercises
- **Grammar Explanation:** Portuguese explanation with an English pattern table.
- **Exercises:** Design 5-7 exercises (e.g., Vocabulary Matching, Fill-in-the-Blank, Personal Response, Sentence Scramble, Conversation Prompt).
- **Approval:** Request user confirmation.

### Step 4: Reading & Comprehension
- **Reading Text:** 100-150 words story using the theme's vocabulary and grammar.
- **Comprehension Questions:** 5 questions with writing lines.
- **Approval:** Request user confirmation.

### Step 5: Final Assembly & Answer Key
- **HTML Production:** Populate `assets/lesson-template.html`.
- **Answer Key:** Create a separate HTML file (`aula-X-[topic]-answers.html`) with all answers and a full dictation transcript.

## Guidelines
- **Language Balance:** Instructions and explanations in Portuguese; Vocabulary and exercises in English.
- **Technical Standards:** Use `<hr class="writing-line">` and `<span class="inline-blank"></span>`. Never use dots `....`.
- **Style:** Consistent 12pt font, Bootstrap 5 layout, print-optimized CSS.
- **Context:** Refer to [project-standards.md](references/project-standards.md) for detailed rules.
