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
- **Approval:** If the user explicitly asked to create the lesson, proceed directly. Only stop for confirmation when the topic, grammar focus, or target format is ambiguous.

### Step 2: Vocabulary & Foundation (Initial File Creation)
- **Vocabulary:** 15-25 terms in a table (Term, Empty Translation, Example).
- **Disambiguation:** Compare 1-2 confusing terms. Prefer compact side-by-side Bootstrap cards/columns when space allows.
- **False Friends:** 2-3 terms that look like Portuguese but have different meanings.
- **Exercise 1 (Vocabulary Matching):** 7-8 terms from the table matched to descriptions.
- **Exercise 2 (True or False):** 4 sentences (exactly 2 True / 2 False) focused on False Friends or Disambiguation.
- **Action:** Create the HTML file (`aula-X-[topic].html`) with Header, Goals, and this interleaved content.

### Step 3: Grammar Topic & Practical Application
- **Grammar Explanation:** Portuguese explanation with an English pattern table.
- **Exercise 3 (Grammar Focus):** 8 fill-in-the-blank sentences using `<span class="inline-blank"></span>`. Use `mb-3` for line spacing.
- **Action:** Update the HTML file with this section.

### Step 4: Fluency, Slangs & Oral Practice
- **Slangs & Idioms:** 3-4 relevant expressions with example sentences. Keep this section visually compact with reduced card padding/margins when needed for print length.
- **Abbreviations:** 4-6 acronyms related to the theme.
- **Exercise 4 (Personal Response):** 2 questions using slangs/idioms. If page count is tight, do not add writing lines; instead instruct students in Portuguese to answer on the back of the page.
- **Exercise 5 (Dictation):** 3 elaborate sentences with **two spread-out blanks** each.
- **Exercise 6 (Conversation):** Verbal-only task with at least **4 specific situational scenarios**. Describe the scenarios in **pt-BR**, not English, so students cannot simply read the prompt as support.
- **Action:** Update the HTML file with this section.

### Step 5: Reading & Finalization
- **Exercise 7 (Reading Comprehension):**
    - **Text:** Prefer an engaging story around **180-300 words**, integrating the lesson vocabulary, grammar, and oral-practice themes.
    - **Formatting:** In the reading text, put target vocabulary in `<strong>`. If a slang/idiom or false friend appears naturally in the story, emphasize it with `<em>`.
    - **Questions:** 5 comprehension questions using `<hr class="writing-line">`.
- **Appendix (Recommended):** Add a quick-reference appendix when the grammar focus benefits from memorization support. For verb-focused lessons, prefer a table of **irregular verbs only**, including **Base Verb**, **Past Simple**, **Translation (PT-BR)**, and a short example. Mix lesson-context verbs with very common English verbs.
- **Answer Key (MANDATORY):** Create or update `aula-X-[topic]-answers.html`.
    - **Note:** The answer key MUST be synchronized with every change made to the lesson file.
- **Action:** Final update to the lesson file and generate/update the answer key.

## Technical Standards

- **Format:** HTML5 using **Bootstrap 5 (CDN)**.
- **Styling:** 
  - CDN: `https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css`
  - Font size: **11pt** for A4 paper.
- **Print Optimization:** 
  - Use `<hr class="writing-line">` for multi-line spaces.
  - Use `<span class="inline-blank"></span>` for inline blanks.
  - Prefer compact spacing in dense sections to keep the lesson within a practical printed page count.
  - Avoid forced page breaks unless the user explicitly asks for them or pagination clearly requires them.
  - **NEVER** use dots (`....`) or Markdown bolding (`**`). Always use `<strong>`.
- **Language Balance:** Instructions/explanations in Portuguese; Content/exercises in English.
- **Formatting:** Key terms in **bold** (`<strong>`); Example sentences in *italics*.

## HTML Template Structure

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Lesson X: Topic</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
    <style>
        body { font-size: 11pt; color: #212529; }
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
