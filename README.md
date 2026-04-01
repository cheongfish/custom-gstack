# Custom GStack Workspace

이 프로젝트는 시니어 엔지니어링 수준의 AI 워크플로우와 페르소나가 통합된 커스텀 GStack 환경입니다.

## 🚀 팀원 온보딩 가이드 (Quick Start)

저장소 용량 최적화를 위해 GStack 엔진 바이너리와 빌드 결과물은 Git에 포함되지 않습니다. 프로젝트를 클론한 후 아래 단계를 통해 로컬 환경을 구성하십시오.

### 1. 요구 사항
- **[Bun](https://bun.sh/)**: 필수 (GStack 엔진 빌드 및 실행용)
- **Node.js**: Windows 사용자의 경우 필요

### 2. GStack 엔진 설치 및 활성화
아래 명령어를 실행하여 로컬에서 엔진을 빌드하고 스킬을 등록합니다.
```bash
cd gstack
bun install
./setup
```
*설치 후 AI 에이전트(Claude Code, Cursor 등)에서 `/qa`, `/review` 등의 스킬이 작동하는지 확인하십시오.*

## 📂 프로젝트 구조
- `gstack/`: 핵심 AI 도구 및 스킬 소스 코드
- `gstack/personas/`: AI가 준수해야 할 백엔드, 프론트엔드, QA 페르소나 정의
- `gstack/.agent/workflows/`: 커밋, PR 생성 등 자동화된 작업 가이드

## 🤖 AI 에이전트 사용 가이드
이 프로젝트에는 AI 에이전트의 행동을 제어하는 `CLAUDE.md` 파일이 포함되어 있습니다. AI는 모든 작업을 수행할 때 `gstack/personas/`에 정의된 원칙을 따릅니다.

---
**문의 사항:** 프로젝트 유지관리자에게 문의하거나 `gstack/ARCHITECTURE.md`를 참조하십시오.
