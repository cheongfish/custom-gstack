# Git PR Description Generation Prompt

---
description: Analyzes the commit history of the current branch to generate a reviewer-friendly GitHub Pull Request body.
---

1. Analyze the changes by reviewing git log main..HEAD --oneline and the detailed commit logs.

2. Categorize the analyzed commits into logical groups (e.g., Features, Fixes, Refactor, Infra).

3. Structure the content using the [Improved PR Markdown Template] below, and output it within a Markdown code block so that the user can copy it directly.

**[Improved PR Markdown Template]**
```markdown
# 🚀 [PR] Title (in Korean)

## 🔗 Related Issues (in Korean)
- #Issue Number (Enter the issue number if there is a related issue)

## 📝 Task Overview (in Korean)
- Summary of the task background and purpose (use nouns)
- 주요 기술적 결정 사항 및 해결 방법

## 🛠️ Major Changes (in Korean)
### ✨ Features & Improvements (in Korean)
- [ ] Feature 1 (~함)
- [ ] Feature 2 (~함)

### 🐛 Fixes (in Korean)
- [ ] Fix 1 (~함)

### 🏗️ Infra & Refactor (in Korean)
- [ ] Infra & Refactor 1 (~함)

## 💬 Additional Information (in Korean)
- Special requests for reviewers or questions
- Any issues or special circumstances encountered during the work
