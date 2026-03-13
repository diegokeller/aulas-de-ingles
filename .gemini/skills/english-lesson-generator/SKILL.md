---
name: english-lesson-generator
description: Generates professional English lesson materials for intermediate Brazilian Portuguese speakers. Use when requested to create a new class, lesson, or teaching material following the project's multi-step workflow and Bootstrap-based HTML format.
---

# English Lesson Generator

This skill guides the creation of high-quality, print-optimized English lessons for intermediate (B1-B2) students who are native Brazilian Portuguese speakers.

## Workflow (Interleaved Dynamic Generation)

When generating a new lesson, follow this sequence. **Update the lesson HTML file at each step** to allow for immediate review of the layout and content.

### Step 1: Lesson Outline & Alignment
- **Theme:** Identify a relevant situational topic.
- **Grammar Topic:** Select a grammar focus.
- **Goals:** 2-3 specific objectives in Portuguese with English key terms.
- **Approval:** Request user confirmation before starting the file.

### Step 2: Vocabulary & Foundation (Initial File Creation)
- **Vocabulary:** 15-25 terms in a table (Term, Empty Translation, Example).
- **Disambiguation:** Compare 1-2 confusing terms.
- **False Friends:** 2-3 terms that look like Portuguese but have different meanings.
- **Exercise 1 (Vocabulary Matching):** Match terms from the table to descriptions.
- **Exercise 2 (Contextual Practice):** Focus on False Friends or Disambiguation.
- **Action:** Create the HTML file (`aula-X-[topic].html`) with Header, Goals, and this content.

### Step 3: Grammar Topic & Practical Application
- **Grammar Explanation:** Portuguese explanation with an English pattern table.
- **Exercise 3 (Grammar Focus):** Fill-in-the-blanks using `<span class="inline-blank"></span>`.
- **Exercise 4 (Personal Response):** Questions followed by 3 `<hr class="writing-line">` each.
- **Action:** Update the HTML file with this section.

### Step 4: Fluency, Slangs & Oral Practice
- **Slangs & Idioms:** 3-4 relevant expressions with example sentences.
- **Abbreviations:** 4-6 acronyms related to the theme.
- **Exercise 5 (Dictation):** Numerated fill-in-the-blanks using `<span class="inline-blank"></span>` (often using slangs).
- **Exercise 6 (Conversation):** Verbal-only task using slangs or abbreviations.
- **Action:** Update the HTML file with this section.

### Step 5: Reading & Finalization
- **Exercise 7 (Reading Comprehension):**
    - **Text:** 100-150 words story integrating all previous concepts.
    - **Questions:** 5 comprehension questions using `<hr class="writing-line">`.
- **Answer Key (MANDATORY):** Create or update `aula-X-[topic]-answers.html`.
    - **Note:** The answer key MUST be synchronized with every change made to the lesson file, including updated vocabulary, exercise numbering, and content.
- **Action:** Perform final update to the lesson file and generate/update the answer key.

## Technical Standards

- **Format:** HTML5 using **Bootstrap 5 (CDN)**.
- **Styling:** 
  - CDN: `https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css`
  - Font size: **12pt** for A4 paper.
- **Print Optimization:** 
  - Use `<hr class="writing-line">` for multi-line spaces.
  - Use `<span class="inline-blank"></span>` for inline blanks.
  - **NEVER** use dots (`....`).
- **Language Balance:** Instructions/explanations in Portuguese; Content/exercises in English.
- **Formatting:** Key terms in **bold**; Example sentences in *italics*.

## HTML Template Structure

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
        <!-- Interleaved Content Sections -->
    </div>
</body>
</html>
```
