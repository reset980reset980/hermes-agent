# 🤖 Hermes Agent - 함께 성장하는 AI 에이전트

![Banner](assets/banner.png)

**스스로 개선하는 AI 에이전트** [Nous Research](https://nousresearch.com)에서 제작했습니다. 내장된 학습 루프를 가진 유일한 에이전트입니다 — 경험에서 스킬을 생성하고, 사용 중 개선하며, 지식 지속을 스스로 유도하고, 과거 대화를 검색하며, 세션 간에 당신에 대한 깊은 모델을 구축합니다. $5 VPS, GPU 클러스터, 또는 유휴 시 거의 비용이 들지 않는 서버리스 인프라에서 실행하세요. 노트북에 묶이지 않습니다 — 클라우드 VM에서 작업하는 동안 Telegram에서 대화하세요.

[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Documentation](https://img.shields.io/badge/docs-hermes--agent.nousresearch.com-green.svg)](https://hermes-agent.nousresearch.com/docs/)
[![Discord](https://img.shields.io/badge/discord-NousResearch-purple.svg)](https://discord.gg/NousResearch)
[![Website](https://img.shields.io/badge/website-nousresearch.com-blue.svg)](https://nousresearch.com)

---

## ✨ 핵심 기능

### 🧠 자기 개선 루프

에이전트가 관리하는 메모리와 주기적 넛지(nudges). 복잡한 작업 후 자율적 스킬 생성. 사용 중 스킬 자체 개선. 세션 간 리콜을 위한 FTS5 세션 검색 및 LLM 요약. [Honcho](https://github.com/plastic-labs/honcho) 변증법적 사용자 모델링. [agentskills.io](https://agentskills.io) 오픈 표준과 호환.

### 🔄 모델 자유

원하는 모든 모델을 사용하세요 — [Nous Portal](https://portal.nousresearch.com), [OpenRouter](https://openrouter.ai) (200+ 모델), [z.ai/GLM](https://z.ai), [Kimi/Moonshot](https://platform.moonshot.ai), [MiniMax](https://www.minimax.io), OpenAI, 또는 자체 엔드포인트. `hermes model`로 전환 — 코드 변경 없음, 잠금 없음.

### 💻 진정한 터미널 인터페이스

완전한 TUI (Terminal User Interface) — 여러 줄 편집, 슬래시 명령 자동완성, 대화 기록, 중단-리디렉트, 스트리밍 도구 출력.

### 🌐 어디서든 살아갑니다

Telegram, Discord, Slack, WhatsApp, Signal, CLI — 단일 게이트웨이 프로세스에서 모두 지원. 음성 메모 전사, 크로스 플랫폼 대화 연속성.

### ⏰ 예약된 자동화

내장 크론 스케줄러로 모든 플랫폼에 전달. 일일 보고, 야간 백업, 주감사 — 모두 자연어로, 무인으로 실행.

### 🚀 위임 및 병렬화

병렬 작업 스트림을 위해 격리된 서브에이전트 생성. RPC를 통해 도구를 호출하는 Python 스크립트를 작성하여 다단계 파이프라인을 제로 컨텍스트 비용 턴으로 축소.

### 🖥️ 노트북뿐만 아니라 어디서든 실행

여섯 개 터미널 백엔드 — 로컬, Docker, SSH, Daytona, Singularity, Modal. Daytona와 Modal은 서버리스 지속성을 제공 — 에이전트 환경이 유휴 시 최대 절전 모드로 들어갔다가 요청 시 깨어납니다. 세션 사이에 거의 비용이 들지 않습니다. $5 VPS 또는 GPU 클러스터에서 실행하세요.

### 🔬 리서치 준비 완료

배치 궤적 생성, Atropos RL 환경, 툴 호출 모델의 다음 세대 훈련을 위한 궤적 압축.

---

## 🚀 빠른 시작

### 설치

```bash
curl -fsSL https://raw.githubusercontent.com/NousResearch/hermes-agent/main/scripts/install.sh | bash
```

**지원 OS:** Linux, macOS, WSL2

설치 프로그램이 모든 것을 처리합니다 — Python, Node.js, 종속성, hermes 명령. git을 제외한 선행 조건 없음.

**Windows:** 네이티브 Windows는 지원되지 않습니다. [WSL2](https://learn.microsoft.com/en-us/windows/wsl/install)를 설치하고 위 명령을 실행하세요.

### 첫 실행

```bash
source ~/.bashrc  # 또는: source ~/.zshrc
hermes setup      # LLM 공급자 구성
hermes            # 채팅 시작!
```

---

## 📖 기본 명령어

| 명령 | 설명 |
|------|------|
| `hermes` | 대화형 CLI — 대화 시작 |
| `hermes model` | 공급자 또는 모델 전환 |
| `hermes setup` | 설정 마법사 재실행 |
| `hermes gateway` | 메시징 게이트웨이 시작 (Telegram, Discord 등) |
| `hermes update` | 최신 버전으로 업데이트 |
| `hermes doctor` | 문제 진단 |

📖 **[전체 문서 →](https://hermes-agent.nousresearch.com/docs/)**

---

## 📚 문서

모든 문서는 [hermes-agent.nousresearch.com/docs](https://hermes-agent.nousresearch.com/docs/)에 있습니다.

### 사용자 가이드

| 섹션 | 내용 |
|------|------|
| [빠른 시작](https://hermes-agent.nousresearch.com/docs/getting-started/quickstart) | 설치 → 설정 → 첫 대화 2분 완성 |
| [CLI 사용법](https://hermes-agent.nousresearch.com/docs/user-guide/cli) | 명령, 키바인딩, 페르소나, 세션 |
| [구성](https://hermes-agent.nousresearch.com/docs/user-guide/configuration) | 구성 파일, 공급자, 모델, 모든 옵션 |
| [메시징 게이트웨이](https://hermes-agent.nousresearch.com/docs/user-guide/messaging) | Telegram, Discord, Slack, WhatsApp, Signal, Home Assistant |
| [보안](https://hermes-agent.nousresearch.com/docs/user-guide/security) | 명령 승인, DM 페어링, 컨테이너 격리 |

### 기능

| 섹션 | 내용 |
|------|------|
| [도구 및 툴셋](https://hermes-agent.nousresearch.com/docs/user-guide/features/tools) | 40+ 도구, 툴셋 시스템, 터미널 백엔드 |
| [스킬 시스템](https://hermes-agent.nousresearch.com/docs/user-guide/features/skills) | 절차적 메모리, 스킬 허브, 스킬 생성 |
| [메모리](https://hermes-agent.nousresearch.com/docs/user-guide/features/memory) | 지속 메모리, 사용자 프로필, 모범 사례 |
| [MCP 통합](https://hermes-agent.nousresearch.com/docs/user-guide/features/mcp) | 확장 기능을 위한 MCP 서버 연결 |
| [크론 스케줄링](https://hermes-agent.nousresearch.com/docs/user-guide/features/cron) | 플랫폼 전송 예약 작업 |
| [컨텍스트 파일](https://hermes-agent.nousresearch.com/docs/user-guide/features/context-files) | 모든 대화에 영향을 주는 프로젝트 컨텍스트 |

### 개발자 가이드

| 섹션 | 내용 |
|------|------|
| [아키텍처](https://hermes-agent.nousresearch.com/docs/developer-guide/architecture) | 프로젝트 구조, 에이전트 루프, 핵심 클래스 |
| [기여](https://hermes-agent.nousresearch.com/docs/developer-guide/contributing) | 개발 설정, PR 프로세스, 코드 스타일 |

### 레퍼런스

| 섹션 | 내용 |
|------|------|
| [CLI 레퍼런스](https://hermes-agent.nousresearch.com/docs/reference/cli-commands) | 모든 명령과 플래그 |
| [환경 변수](https://hermes-agent.nousresearch.com/docs/reference/environment-variables) | 완전한 env var 레퍼런스 |

---

## 🤝 기여

기여를 환영합니다! [기여 가이드](https://hermes-agent.nousresearch.com/docs/developer-guide/contributing)에서 개발 설정, 코드 스타일, PR 프로세스를 확인하세요.

### 기여자를 위한 빠른 시작

```bash
git clone --recurse-submodules https://github.com/NousResearch/hermes-agent.git
cd hermes-agent
curl -LsSf https://astral.sh/uv/install.sh | sh
uv venv .venv --python 3.11
source .venv/bin/activate
uv pip install -e ".[all,dev]"
uv pip install -e "./mini-swe-agent"
python -m pytest tests/ -q
```

---

## 📞 커뮤니티

- 💬 [Discord](https://discord.gg/NousResearch)
- 📚 [스킬 허브](https://agentskills.io)
- 🐛 [이슈](https://github.com/NousResearch/hermes-agent/issues)
- 💡 [토론](https://github.com/NousResearch/hermes-agent/discussions)

---

## 📄 라이선스

MIT — [LICENSE](LICENSE) 참조

---

[Nous Research](https://nousresearch.com)에서 제작했습니다.
