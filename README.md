# 우리말답게 (urimal-dapge)

AI가 쓴 한국어를 우리말답게 고치는 Claude Code 스킬이에요. 번역투·리듬 같은 **어휘 티**와 함께 **"누가 하는가"가 빠진 문장 뼈대**까지 점검해요.

[epoko77-ai/im-not-ai](https://github.com/epoko77-ai/im-not-ai)의 `humanize-korean` 2.3.2를 바탕으로 만든 파생판이에요(MIT).

## 원본과 다른 점

원본은 어휘 티를 잘 잡지만, 이런 문장은 그대로 통과시켜요.

> 계약 통보서가 들어오면 시작한다.

통보서가 스스로 움직이고, "시작한다"의 주어도 비어 있어요. 사람은 이렇게 써요.

> 업무는 마케팅 담당이 계약 통보서를 받으면서 시작된다.

이를 잡으려고 더한 것:

- **구조 점검(Phase 2.6):** 윤문 뒤 문장마다 "누가 하는가?"를 확인해요. 행위자는 원문이나 작업 폴더에서 확인될 때만 채우고, 모르면 표시만 해요.
- **새 패턴 3개:** A-25 사물 주어 + 행위 동사, A-26 주어가 바뀌었는데 생략, C-15 산문 속 화살표 연쇄
- **Windows:** `python3`가 Store 바로가기여도 실제 파이썬을 찾아 게이트를 돌려요.

근거 문헌(이근희 2008, 국립국어원 지침, LLM 번역투 연구 등)은 [scholarship.md](skills/humanize-korean/references/scholarship.md)에 있어요.

## 설치

```
/plugin marketplace add sj-park-kr/urimal-dapge
/plugin install urimal-dapge@urimal-dapge
```

"AI 티 없애줘", "사람이 쓴 것처럼 윤문해줘"라고 하면 동작해요. 원본 `humanize-korean`과 스킬 이름이 같으니 하나만 설치하세요. Claude Code 전용이에요.

## 라이선스

MIT. 분류 체계·스크립트·에이전트는 원작자 [epoko77-ai](https://github.com/epoko77-ai/im-not-ai)와 기여자들의 작업이에요.
