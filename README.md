# my-llm-wiki — 시작 구조

2026-07-10에 세팅한 LLM wiki의 시작 구조.

```
my-llm-wiki/
├── CLAUDE.md                        ← 스키마: 운영 규칙서 (전체를 감싼다)
├── 2026/                            ← raw 층: 절대 수정하지 않음
│   └── 07/
│       ├── 10.md                    ← 오늘의 학습 기록
│       └── 10-llm-wiki-보고서.md     ← 과제 보고서 (raw 원본)
├── wiki/                            ← 위키 층: LLM이 쓰고 사람이 검토
│   ├── index.md
│   └── llm-wiki.md                  ← 첫 지식 페이지
└── book/                            ← 원고 층: 당분간 비워둠
```

## 기존 저장소(ai-learning-log)에 합치는 법

이 폴더의 내용을 저장소 루트에 복사한 뒤:

```bash
cd ~/ai-learning-log        # 실제 저장소 경로로 이동
git add .
git commit -m "LLM wiki 구조 세팅: CLAUDE.md, wiki 층, 첫 페이지"
git push
```

주의: 명령어를 붙여넣을 때 한글 주석(#)을 함께 붙여넣지 말 것.

## 다음 할 일

1. wiki/llm-wiki.md를 읽고 검토 (내 이해와 다른 항목이 있는지)
2. commit + push
3. 7월 말: Claude Code에게 첫 ingest + lint 요청
   - "CLAUDE.md 규칙을 읽고, 2026/07/ 기록에서 위키로 승격할 지식을 골라 반영해줘"
   - "wiki/ 전체에서 중복·모순·깨진 링크를 점검해줘"
