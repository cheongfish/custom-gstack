# 🔄 Session Handover & Context Compression Prompt

---
**Description:** Analyzes the current session's core context (changes, design decisions, tech stack, remaining tasks) and generates a structured handover document in **Korean** for seamless "Context Injection" into a new AI session.
---

## 1. Analysis & Extraction Guidelines
1. **History Analysis**: Review the conversation history and code changes within the current session to identify the core project purpose (Context) and the technical stack (Frameworks, DBs, etc.).
2. **Decision Log (Why)**: Beyond simple changes, extract "why" certain libraries or logic patterns were chosen to preserve established design principles and prevent redundant discussions.
3. **User Preference Identification**: Identify the user's coding style (e.g., functional programming, specific error handling patterns) and communication preferences to maintain consistency in the next session.

## 2. Prompting Rules (for the AI)
1. **AI-to-AI Tone**: Write in an instructional and clear tone so the receiving AI can immediately adopt its role as an expert.
2. **Token Optimization**: Use noun-based keywords and bullet points. Avoid unnecessary polite fillers or flowery language to save tokens in the new session.
3. **Context Independence**: Ensure the output is self-contained so the new AI can recover over 90% of the context without needing the previous chat history.
4. **Clean Output**: Output **ONLY** the Markdown code block. Do not include any conversational fillers (e.g., "Here is your handover...") outside the block.

## 3. Output Format (Mandatory Korean Template)
Please generate the handover document using the following Korean template:

# 🔄 프로젝트 상황 핸드오버 (새 세션)

> **Instruction**: 너는 이전 세션의 작업 내용을 완벽히 이어받은 [해당 분야 전문가 역할]이다. 아래 기술된 현재 상황과 맥락을 숙지하고, 이후 사용자의 지시에 따라 일관성 있게 작업을 수행하라.

## 🛠 1. 기술 스택 및 개발 환경
- **주요 스택**: (내용 작성)
- **데이터베이스/상태관리**: (내용 작성)
- **특이 설정**: (내용 작성)

## 🎯 2. 핵심 컨텍스트 및 의사결정 사항 (Why)
- **현재 작업 목표**: (내용 작성)
- **주요 설계 결정**: (내용 작성)

## 🏗 3. 최근 변경 사항 및 아키텍처 (What)
- **주요 수정 파일**:
    - `[파일 경로]`: (변경 내용 및 이 파일의 핵심 역할)
- **데이터/로직 흐름**: (내용 작성)

## 🚧 4. 남은 과제 및 리스크 (Next Step)
- **즉시 수행 과제**: (내용 작성)
- **잔여 이슈/리스크**: (내용 작성)
- **제약 사항**: (내용 작성)

## 📝 5. 사용자 선호도 및 스타일
- **코딩 스타일**: (내용 작성)
- **소통 방식**: (내용 작성)