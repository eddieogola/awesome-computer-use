# Contributing to Awesome Computer Use

Thank you for your interest in contributing to this curated list! This document provides guidelines for contributions.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How to Contribute](#how-to-contribute)
- [Formatting Guidelines](#formatting-guidelines)
- [Quality Standards](#quality-standards)
- [Pull Request Process](#pull-request-process)

## Code of Conduct

- Be respectful and constructive in discussions
- Focus on the quality and relevance of resources
- Help maintain an inclusive community

## How to Contribute

### Adding a New Resource

1. **Fork** this repository
2. **Create a branch** for your addition: `git checkout -b add-resource-name`
3. **Add your resource** to the appropriate section in `README.md`
4. **Commit** your changes with a clear message
5. **Push** to your fork and submit a **Pull Request**

### Suggesting Changes

- Open an [Issue](../../issues) to discuss major changes before submitting a PR
- For typos and minor fixes, feel free to submit a PR directly

### Reporting Broken Links

- Open an issue with the title: `[Broken Link] Resource Name`
- Include the section where the link appears

## Formatting Guidelines

### Papers

```markdown
- [Paper Title](https://arxiv.org/abs/XXXX.XXXXX) - Brief one-sentence description. *Institution, Year* · [Code](url)
```

**Example:**
```markdown
- [OSWorld: Benchmarking Multimodal Agents](https://arxiv.org/abs/2404.07972) - The definitive benchmark for computer use agents with 369 tasks. *Salesforce et al., 2024* · [Code](https://github.com/xlang-ai/OSWorld)
```

### Tools & Projects

```markdown
- [Project Name](url) - Description of what it does and key features.
```

**Example:**
```markdown
- [Browser Use](https://github.com/browser-use/browser-use) - High-level framework for building browser automation agents with LLMs.
```

### Open Source Models

Add to the table in the "Open Source Computer Use" section:

```markdown
| [Model Name](url) | Size | Key highlights and benchmark scores. | [Paper](url) · [Code](url) |
```

### General Formatting Rules

- Use **Title Case** for resource names
- Keep descriptions **concise** (one sentence, ~15 words max)
- Include **year** for papers and time-sensitive resources
- Add **relevant links** (paper, code, docs) where available
- Use **bold** for featured/highlighted resources

## Quality Standards

### What We Accept

- **Open source models** with published weights
- **Peer-reviewed papers** or preprints from arXiv, OpenReview, etc.
- **Actively maintained** tools and frameworks
- **Well-documented** commercial platforms
- **Educational content** (tutorials, videos, blog posts) of high quality

### What We Don't Accept

- Resources not directly related to computer use / GUI automation
- Abandoned projects with no recent activity (>2 years)
- Paywalled content without free alternatives
- Self-promotional content without clear value
- Duplicate entries

### Featured Resources

Resources may be **bolded** as featured if they meet these criteria:

- Significant impact on the field
- State-of-the-art results on established benchmarks
- Widely adopted by the community
- Exceptional documentation and accessibility

## Pull Request Process

### Before Submitting

- [ ] Resource is relevant to computer use / GUI automation
- [ ] Link is valid and accessible
- [ ] Formatting follows the guidelines above
- [ ] Resource is placed in the correct section
- [ ] No duplicate entries exist

### PR Title Format

```
Add [Resource Name] to [Section]
```

**Examples:**
- `Add UI-TARS to Open Source Models`
- `Add WebArena to Benchmarks`
- `Fix broken link in Research section`

### Review Process

1. A maintainer will review your PR within 7 days
2. You may be asked to make changes or provide additional context
3. Once approved, your contribution will be merged

## Questions?

If you have questions about contributing, feel free to:

- Open an [Issue](../../issues) with the `question` label
- Start a [Discussion](../../discussions)

---

Thank you for helping make this resource better for the community!
