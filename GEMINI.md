# English Lessons Project - Instructions

## Overview
This project contains English lesson materials for **intermediate level** students who are **native Brazilian Portuguese (pt-BR) speakers**. The focus is on practical communication skills through exercises and conversation practice.

## Target Audience
- **Level:** Intermediate (B1-B2)
- **Native Language:** Brazilian Portuguese
- **Goal:** Improve conversational English and practical vocabulary

---

## Technical Standards (MANDATORY)

- **Format:** All lessons and answer keys must be written in **HTML5** using **Bootstrap 5 (CDN)**.
- **File Naming:** `aula-[number]-[topic-in-portuguese].html`
- **Styling:** 
  - CDN: `https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css`
  - Font size: **12pt** for optimal reading on A4 paper.
  - Colors: Use Bootstrap defaults (text-dark, bg-light, etc.) with minimal custom CSS.
- **Print Optimization:** 
  - Use dots (`....................`) for writing spaces.
  - Ensure tables and sections do not break awkwardly across pages.

---

## Content Guidelines

### Structure
Each lesson must follow this hierarchy:
1. **Goals:** 2-3 objectives mixing Portuguese explanation with English key terms.
2. **Vocabulary:** Single-column table (Term, Translation Dots, Example Sentence).
3. **Disambiguation:** Comparison of similar terms (e.g., *Job* vs. *Work*).
4. **Slangs and Idioms:** Table with expressions and example sentences.
5. **Famous Abbreviations:** List of common professional/topic acronyms.
6. **Grammar Topic:** **Every class must introduce a grammar topic** with a clear explanation and pattern table.
7. **Exercises:** All exercises must be numbered sequentially (1 to 7).

### Language Balance
- **Instructions and explanations:** Portuguese.
- **Vocabulary, examples, exercises:** English.
- **Key terms:** Always in **bold**.
- **Example sentences:** In *italics*.

### Answer Keys
- **Pattern:** `aula-[number]-[topic]-answers.html`.
- **Content:** Include full text of questions, full **Audio Transcripts** for dictation, and specific expected answers.

---

## Exercise Types (Standard Sequence)

1. **Exercise 1 (Vocabulary Selection):** Word bank at the top for students to match terms to descriptions.
2. **Exercise 2 (Grammar Practice):** Fill-in-the-blanks focused on the grammar topic.
3. **Exercise 3 (Personal Response):** Questions followed by 3 writing lines (dots) each.
4. **Exercise 4 (Dictation):** Numerated fill-in-the-blanks synchronized with the teacher's transcript.
5. **Exercise 5 (Sentence Scramble):** Reorder words to form correct sentences.
6. **Exercise 6 (Conversation):** Verbal-only task using specific slangs or abbreviations.
7. **Exercise 7 (Reading Comprehension):** Short text (100-150 words) with 5 comprehension questions.

---

## Recommended Topics
1. Greetings and Introductions
2. Seasons, Weather, Time
3. Family and Relationships
4. Daily Routines
5. Work and Business (Current: Aula 5)
6. Travel and Directions
7. Food and Restaurants
8. Shopping and Money
9. Health and Body
10. Hobbies and Free Time
11. Technology and Internet
12. Environment and Nature

---

## HTML Template (Lesson Structure)

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Lesson X: Topic</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
    <style>
        body { font-size: 12pt; color: #212529; }
        .dots { color: #6c757d; }
        .writing-lines { line-height: 2.5; color: #dee2e6; border-bottom: 1px solid #dee2e6; display: block; min-height: 1.5em; }
    </style>
</head>
<body class="bg-light py-4">
    <div class="container bg-white p-5 shadow-sm">
        <h1 class="text-center mb-4 border-bottom pb-2">Lesson X: Topic</h1>
        <!-- Content follows the Structure guidelines -->
    </div>
</body>
</html>
```
