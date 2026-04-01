---
description: Suggests atomic commit commands in Korean with inferred intentions and supports iterative updates based on user feedback.
---

## 1. Analysis Guidelines
1. **Change Analysis**: Analyze the provided `git diff`, untracked files, or full file content.
   - **New Files**: Treat the entire content as an addition.
2. **Inferred Intention**: Based on the code changes, infer the *technical intent* (e.g., improving stability, removing redundancy, fixing edge cases).
3. **Atomic Commits**: Ensure each suggestion covers only one logical task.
4. **No Linting**: Ignore code style or linting issues. Focus only on the logic and data flow.

## 2. Commit Message Rules
- **Language**: Commit messages (Subject and Body) must be written in **Korean**.
- **Tone & Style**: 
  - **Task-Oriented & Objective**: No exaggerations (e.g., "Improved", "Optimized"). Use neutral, fact-based language.
  - **No Module Names**: Do not mention specific module or package names in the **Body**.
  - **Format**: Use noun phrases (~함, ~추가) and bullet points (-), max 3 lines.
- **Feedback Loop**: If the user provides the "Actual Intent," regenerate the message prioritizing that context over the AI's initial guess.

## 3. Output Format (Two-Step Process)

### STEP 1: Initial Suggestion
For each logical unit, output the following:

**[논리적 단위 분석]**
* **추측된 작업 의도**: (AI가 판단한 기술적 변경 이유를 한 줄로 설명)

**[커밋 제안]**
(커밋 제목: Conventional Commits 형식)
(커밋 본문: 작업 내용 중심, 모듈명 제외)

**[실행 명령어]**
```bash
git add [파일 경로]
git commit -m "(제목)

(본문)"