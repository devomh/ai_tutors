# Knowledge Base Template & Examples

## File Structure Template

### subjects/[subject_name]/topics.json
```json
{
  "subject": "calculus",
  "version": "1.0",
  "last_updated": "2025-01-19",
  "navigation": {
    "\\limits": {
      "path": "limits/",
      "display": "Limits and Continuity",
      "prerequisites": ["algebra_review"]
    },
    "\\derivatives": {
      "path": "derivatives/", 
      "display": "Derivatives",
      "prerequisites": ["limits"]
    }
  },
  "learning_sequence": ["limits", "derivatives", "integrals"],
  "assessment_criteria": {
    "mastery_threshold": 0.8,
    "prerequisite_threshold": 0.7
  }
}
```

### subjects/[subject]/[topic]/concepts.md
```markdown
# Topic: Limits

## Core Definitions
**Limit (Intuitive)**: The value that f(x) approaches as x approaches a certain value.

**Formal Definition**: For every ε > 0, there exists δ > 0 such that if 0 < |x - a| < δ, then |f(x) - L| < ε.

## Essential Understanding
Students must grasp:
1. Limits describe behavior NEAR a point, not AT the point
2. The function may not even be defined at the limit point
3. Left and right limits may differ

## Prerequisite Check Questions
- "Can you evaluate f(2) if f(x) = (x² - 4)/(x - 2)?"
- "What happens when we divide by zero?"
- "Can you factor x² - 4?"

## Common Student Language
- "What does the function equal when x equals..."
- "Just plug in the number"
- "The answer is undefined"

## Bridging Questions
- "What if we can't 'plug in' the number directly?"
- "What happens to f(x) when x gets very close to but doesn't equal a?"
```

### subjects/[subject]/[topic]/examples.md
```markdown
# Limits: Worked Examples for Reference

## Example 1: Direct Substitution
**Problem**: Find lim(x→3) (2x + 1)
**Student Guidance Path**:
1. "What happens if you substitute x = 3?"
2. "Does the function have any issues at x = 3?"
3. "So what's 2(3) + 1?"

## Example 2: Indeterminate Form 0/0
**Problem**: Find lim(x→2) (x² - 4)/(x - 2)
**Student Guidance Path**:
1. "What happens when you substitute x = 2?"
2. "We get 0/0. What does this tell us?"
3. "Can you factor the numerator?"
4. "What's (x + 2)(x - 2)/(x - 2) when x ≠ 2?"
5. "Now what's lim(x→2) (x + 2)?"

## Example 3: One-sided Limits
**Problem**: Find lim(x→0⁺) 1/x and lim(x→0⁻) 1/x
**Student Guidance Path**:
1. "What happens to 1/x when x is a small positive number?"
2. "What happens when x is a small negative number?"
3. "Do these limits agree?"
```

### subjects/[subject]/[topic]/exercises.md
```markdown
# Limits: Practice Problems

## Level 1: Direct Substitution
**Problem 1A**: lim(x→1) (3x - 2)
- Prerequisites: Basic arithmetic, linear functions
- Expected difficulty: Easy
- Common errors: None typically

**Problem 1B**: lim(x→-2) (x² + x - 1)
- Prerequisites: Polynomial evaluation, order of operations
- Expected difficulty: Easy
- Common errors: Sign mistakes with (-2)²

## Level 2: Algebraic Manipulation Required
**Problem 2A**: lim(x→3) (x² - 9)/(x - 3)
- Prerequisites: Factoring difference of squares, rational function simplification
- Expected difficulty: Medium
- Common errors: 
  - Saying limit doesn't exist because of 0/0
  - Not factoring before simplifying

**Problem 2B**: lim(h→0) [(2+h)² - 4]/h
- Prerequisites: Expanding binomials, algebraic simplification
- Expected difficulty: Medium-Hard
- Common errors:
  - Expanding (2+h)² incorrectly
  - Not recognizing this as a derivative definition
```

### subjects/[subject]/[topic]/common_errors.md
```markdown
# Limits: Error Diagnosis & Response Guide

## Error Pattern 1: Direct Substitution in Indeterminate Forms
**Student Behavior**: "lim(x→2) (x² - 4)/(x - 2) = 0/0 = 0"
**Diagnosis Questions**:
- "What does 0/0 mean mathematically?"
- "Is 0/0 the same as 0/5 or 5/0?"
**Guidance Strategy**:
- Explain indeterminate forms
- Guide through algebraic manipulation
- Connect to "removable discontinuity" concept

## Error Pattern 2: Confusing Limit with Function Value
**Student Behavior**: "The limit doesn't exist because f(a) is undefined"
**Diagnosis Questions**:
- "What's the difference between f(a) and lim(x→a) f(x)?"
- "Can you think of a function that's undefined at x=2 but has a limit there?"
**Guidance Strategy**:
- Use graphical intuition
- Provide concrete examples
- Emphasize "approaching" vs "arriving"

## Error Pattern 3: Incorrect Algebraic Manipulation
**Student Behavior**: Factoring errors, cancellation mistakes
**Diagnosis Questions**:
- "Can you check your factoring by expanding back?"
- "What are the restrictions when canceling terms?"
**Guidance Strategy**:
- Return to prerequisite algebra review
- Practice factoring systematically
- Emphasize domain restrictions
```

## Implementation Guidelines

### Loading Strategy for GPT
1. **Primary Load**: Topics relevant to current session
2. **Secondary Load**: Prerequisite checking materials
3. **Tertiary Load**: Advanced extensions if student shows mastery

### Content Updating Process
1. **Version Control**: Track changes in topics.json
2. **A/B Testing**: Compare different explanation approaches
3. **Student Feedback Integration**: Refine based on confusion patterns

### Multilingual Considerations
```
knowledge_base/
├── subjects_en/
├── subjects_es/
└── subjects_fr/
```

### Quality Assurance Checklist
- [ ] All prerequisite chains are complete
- [ ] Error patterns include diagnostic questions
- [ ] Examples progress from simple to complex
- [ ] Language is student-appropriate
- [ ] Guidance never gives direct answers

This template ensures consistent, high-quality knowledge base development across all subjects and topics.