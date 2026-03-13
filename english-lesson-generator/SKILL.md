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
- **Grammar Topic:** Select a grammar focus.
- **Goals:** 2-3 specific objectives in Portuguese with English key terms.
- **Approval:** Request user confirmation before proceeding.

### Step 2: Core Content Development
- **Vocabulary:** 15-25 terms in a single-column table (Term, Empty Translation Column, Example Sentence).
- **Disambiguation:** Compare 1-2 confusing terms (e.g., *Job* vs. *Work*).
- **False Friends:** Include 2-3 terms that look/sound like Portuguese but have different meanings (e.g., *Parents* vs. *Parentes*).
- **Slangs & Idioms:** 3-4 relevant expressions with example sentences.
- **Abbreviations:** 4-6 acronyms related to the theme.
- **Approval:** Request user confirmation.

### Step 3: Grammar & Exercises
- **Grammar Explanation:** Portuguese explanation with an English pattern table.
- **Exercise Sequence (Mandatory):**
    1. **Exercise 1 (Vocabulary Selection):** Word bank matching terms to descriptions.
    2. **Exercise 2 (Grammar Practice):** Fill-in-the-blanks using `<span class="inline-blank"></span>` focused on grammar.
    3. **Exercise 3 (Personal Response):** Questions followed by 3 `<hr class="writing-line">` each.
    4. **Exercise 4 (Dictation):** Numerated fill-in-the-blanks using `<span class="inline-blank"></span>`.
    5. **Exercise 5 (Sentence Scramble):** Reorder words using `<hr class="writing-line">`.
    6. **Exercise 6 (Conversation):** Verbal-only task using slangs or abbreviations.
- **Approval:** Request user confirmation.

### Step 4: Reading & Comprehension
- **Exercise 7 (Reading Comprehension):**
    - **Text:** 100-150 words story using the theme's vocabulary and grammar.
    - **Questions:** 5 comprehension questions using `<hr class="writing-line">`.
- **Approval:** Request user confirmation.

### Step 5: Final Assembly & Answer Key
- **HTML Production:** Populate `assets/lesson-template.html` (see template below).
- **File Naming:** `aula-[number]-[topic-in-portuguese].html`.
- **Answer Key:** Create `aula-[number]-[topic]-answers.html` with full question text, audio transcripts for dictation, and expected answers.

## Technical Standards

- **Format:** HTML5 using **Bootstrap 5 (CDN)**.
- **Styling:** 
  - CDN: `https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css`
  - Font size: **12pt** for A4 paper.
  - Colors: Bootstrap defaults (text-dark, bg-light, etc.).
- **Print Optimization:** 
  - Use `<hr class="writing-line">` for multi-line spaces.
  - Use `<span class="inline-blank"></span>` for inline blanks.
  - **NEVER** use dots (`....`).
  - Ensure tables/sections do not break awkwardly across pages.

## Language & Style Guidelines
- **Language Balance:** Instructions and explanations in Portuguese; Vocabulary and exercises in English.
- **Formatting:** Key terms in **bold**; Example sentences in *italics*.
- **Consistency:** All exercises must be numbered sequentially (1 to 7).

## HTML Template

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Lesson X: Topic</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
    <style>
        body { font-size: 12pt; color: #212529; }
        @media print {
            @page { margin: 0; }
            body { padding: 1cm !important; margin: 0 !important; }
            .container { width: 100%; max-width: none; border: none; box-shadow: none; padding: 0 !important; }
        }
        .writing-line { border: 0; border-bottom: 1px solid #dee2e6; margin: 3rem 0 0.5rem 0; }
        .inline-blank { display: inline-block; min-width: 120px; border-bottom: 1px solid #212529; margin: 0 5px; vertical-align: bottom; }
    </style>
</head>
<body class="bg-light py-4">
    <div class="container bg-white p-5 shadow-sm">
        <h1 class="text-center mb-4 border-bottom pb-2">Lesson X: Topic</h1>
        <!-- Content follows the Workflow -->
    </div>
</body>
</html>
```
