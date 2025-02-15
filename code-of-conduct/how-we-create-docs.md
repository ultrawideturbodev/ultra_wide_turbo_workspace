---
document_type: code of conduct
goal: define structure for knowledge, protocol and process documents
gpt_action: follow this template when asked to create new documents
---

# Document Format

Every document must have this header:
```markdown
---
document_type: [protocol|code of conduct|prompt|template]
goal: [clear goal statement]
gpt_action: [specific instruction for GPT]
---
```

# Writing Rules

1. Every step must follow this format:
   - Start with uppercase Gherkin style keyword: GIVEN, WHEN, THEN, AND, OR, IF, IF ELSE, ELSE
   - Followed by an [[Actor]] or [[Component]] in double brackets
   - Followed by a VERB or STATE word (IS, HAS, NEEDS, EXISTS) in uppercase
   - Max 1 words in CAPS after [[Actor]] or [[Component]]
   - Always use [[double brackets]] for actors, repeated concepts, and components

2. Step hierarchy:
   1. State and hard preconditions start with GIVEN
   2. Steps start with WHEN
   3. Sub steps indent and start with THEN, AND or OR
   4. Conditionals indent and start with IF, ELSE, ELSE IF

# Example

```markdown
1. GIVEN [[User]] GIVES [[input]]
2. WHEN [[You]] START [[implementation]]
   1. AND [[You]] WRITE tests
   2. AND [[You]] ADD code
   3. WHEN [[implementation]] IS complete
      1. THEN [[You]] RUN tests
   4. IF [[tests]] FAIL
      1. THEN [[You]] FIX issues
      2. AND [[You]] RETRY tests
```

Code examples use triple backticks with language:
```dart
void example() {
  print('Hello');
}
```
