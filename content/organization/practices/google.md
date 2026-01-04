---
title: Google Engineering Practices
parent: Industry Practices
nav_order: 1
layout: default
---

# Google Engineering Practices

> **Reading time:** 5 min | **Level:** Intermediate

Google's engineering practices have influenced software development industry-wide. This note covers key quality practices that emerged from Google's scale and engineering culture.

---

## Code Review at Scale

### Philosophy

Google reviews **every** change before submission. Key principles:

- Code review is about code quality, not finding bugs
- Reviews should be fast (aim for <24 hours)
- Reviewer approves when code improves overall health
- Style consistency matters at scale

### Review Standards

**What reviewers look for:**

| Aspect | Questions |
|--------|-----------|
| Design | Does this change belong here? Is it well-designed? |
| Functionality | Does the code do what it's supposed to? |
| Complexity | Can the code be simpler? Will others understand it? |
| Tests | Are tests correct, sensible, and useful? |
| Naming | Are names clear and descriptive? |
| Comments | Are comments necessary and clear? |
| Style | Does it follow style guides? |
| Documentation | Is relevant documentation updated? |

### Speed vs Thoroughness

- **Fast reviews** enable rapid iteration
- **Thorough reviews** catch issues early
- Balance: review within one business day
- Small CLs (changelists) are easier to review

---

## Testing Philosophy

### The Test Pyramid

Google follows the test pyramid model:

```
        /\
       /  \      E2E Tests (10%)
      /----\     - Slow, expensive
     /      \    - Test full system
    /--------\   
   /          \  Integration Tests (20%)
  /------------\ - Test component interactions
 /              \
/----------------\ Unit Tests (70%)
                   - Fast, isolated
                   - Test single units
```

### Testing Principles

1. **Test behavior, not implementation** — Tests should survive refactoring
2. **Make tests hermetic** — No external dependencies
3. **Test at appropriate level** — Unit for logic, integration for interactions
4. **Prefer real implementations** — Mocking hides bugs

### Test Size Definitions

| Size | Time | Resources | Network |
|------|------|-----------|---------|
| Small | <100ms | Single process | No |
| Medium | <300s | Single machine | Localhost only |
| Large | Unlimited | Multiple machines | Yes |

Small tests run in CI; large tests run less frequently.

---

## Monorepo and Quality

### What is Monorepo?

Google stores most code in a single repository:
- ~2 billion lines of code
- 25,000+ developers
- Unified tooling and processes

### Quality Benefits

| Benefit | Description |
|---------|-------------|
| Atomic changes | Update library and all callers together |
| Code sharing | Easy to reuse and discover code |
| Consistent tooling | Same build, test, review tools |
| Dependency visibility | See who uses your code |
| Large-scale refactoring | Change everything at once |

### Quality Challenges

- Build times can be long
- Tests must be highly reliable
- Requires sophisticated tooling
- Not suitable for all organizations

---

## Release Engineering

### Continuous Integration

Google's CI principles:
- All changes tested before submission
- Tests run on every change
- Failures block submission
- Fast feedback (minutes, not hours)

### Safe Releases

Release practices for quality:

| Practice | Description |
|----------|-------------|
| Canary releases | Deploy to small % first |
| Feature flags | Separate deploy from release |
| Gradual rollout | Increase traffic slowly |
| Automatic rollback | Revert on error spike |
| Release trains | Regular, predictable releases |

### Release Qualification

Before production:
1. All tests pass
2. Canary shows no degradation
3. Load testing validates capacity
4. Security review (for sensitive changes)

---

## Postmortems

### Blameless Culture

When incidents occur:
- Focus on **systems**, not individuals
- Ask "what" failed, not "who" failed
- Assume best intentions
- Document for learning

### Postmortem Structure

```markdown
## Incident Summary
Brief description of what happened

## Impact
- Users affected: X
- Duration: Y minutes
- Revenue impact: $Z

## Timeline
- HH:MM - Event occurred
- HH:MM - Alert fired
- HH:MM - Response began
- HH:MM - Mitigated
- HH:MM - Resolved

## Root Cause
Technical explanation of why this happened

## Action Items
| Action | Owner | Priority | Status |
|--------|-------|----------|--------|
| Fix X  | Alice | P1       | Done   |
| Add monitoring for Y | Bob | P2 | Open |

## Lessons Learned
What we learned from this incident
```

---

## Code Health

### Readability

Google has a "readability" process:
- Engineers earn readability certification per language
- Readability reviewers ensure code quality
- Certified engineers can approve style/idioms

### Style Guides

Public Google style guides:
- C++, Java, Python, Go, JavaScript, Shell, HTML/CSS
- Consistency enables collaboration at scale
- Automated formatters enforce style

### Technical Debt

Google tracks and manages technical debt:
- Regular "fixit" weeks for cleanup
- Deprecation process for old APIs
- Large-scale changes (LSCs) for refactoring

---

## Key Practices Summary

| Practice | Purpose |
|----------|---------|
| Code review | Quality gate before submission |
| Test pyramid | Balanced test coverage |
| Monorepo | Unified codebase and tooling |
| CI/CD | Fast feedback, safe releases |
| Postmortems | Learn from failures |
| Style guides | Consistent, readable code |

---

## Applying Google Practices

### What Scales Down

These practices work at any size:
- Code review for every change
- Test pyramid approach
- Blameless postmortems
- Style guides and formatters

### What Requires Scale

These require significant investment:
- Monorepo tooling
- Readability process
- Large-scale changes infrastructure

---

## Related Topics

- [Code Review](../../verif/static/inspections/) — Review techniques
- [CI/CD Quality](../project-quality/) — Continuous integration
- [SRE Practices](sre/) — Operations engineering

---

## Further Reading

- [Software Engineering at Google](https://abseil.io/resources/swe-book/html/toc.html) — Winters, Manshreck, Wright (O'Reilly, 2020; free online)
- [Google Engineering Practices](https://google.github.io/eng-practices/) — Code review guide
- [Google Testing Blog](https://testing.googleblog.com/)
- [Google Style Guides](https://google.github.io/styleguide/)

---

{: .highlight }
**Disclaimer:** AI is used for text polishing and explaining. Authors have verified all facts and claims. In case of an error, feel free to file an issue.
