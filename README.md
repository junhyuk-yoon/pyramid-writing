# so-what-mece

So What · Why So · MECE 원칙으로 업무 문서를 쓰고 고치는 Claude 스킬입니다.

문서 링크나 본문을 주고 "이 스킬로 고쳐줘"라고 하면, 결론이 먼저 보이고 근거가 바로 아래에 붙으며 겹침과 누락이 없는 문서로 다듬어 줍니다. Confluence, Google Docs, Notion, Word, Apple Notes, Markdown, Slack, 이메일 어디에 쓰는 문서든 같은 원칙을 적용하고 서식만 도구에 맞춥니다.

## 세 가지 원칙

| 원칙 | 묻는 것 | 대표 규칙 |
|---|---|---|
| So What | 그래서 결론이 무엇인가 | 소제목을 결론 문장으로, 수치 뒤에 할 일을 화살표로 |
| Why So | 왜 그렇게 말할 수 있는가 | 결론 바로 아래에 근거 수치와 출처, 추정은 요약에서 제외 |
| MECE | 빠지거나 겹친 것은 없는가 | 불릿 하나에 지표 하나, 불리한 정보는 비고에 남기기 |

여기에 두 가지를 더 적용합니다.

- 구분 기호는 ` : `로 고정합니다. `1. 정의 — 내용`이 아니라 `1. 정의 : 내용`으로 씁니다.
- 번역투, 상투적인 맺음말, 과장 어휘, 접속사 남발 같은 AI 특유의 문체를 걷어냅니다.

전체 규칙은 [SKILL.md](skills/so-what-mece/SKILL.md), 도구별 서식은 [references/tools.md](skills/so-what-mece/references/tools.md), AI 문체 목록은 [references/ai-tells.md](skills/so-what-mece/references/ai-tells.md)에 있습니다.

## 설치

### Claude Code : 플러그인으로 설치

```
/plugin marketplace add junhyuk-yoon/so-what-mece
/plugin install so-what-mece@so-what-mece
```

### Claude Code : 폴더만 복사

```bash
git clone https://github.com/junhyuk-yoon/so-what-mece.git
cp -r so-what-mece/skills/so-what-mece ~/.claude/skills/
```

### Claude 앱 (claude.ai, 데스크톱)

1. 이 저장소를 내려받습니다.
2. `skills/so-what-mece` 폴더를 zip으로 압축합니다.
3. 설정의 스킬 메뉴에서 zip 파일을 올립니다.

## 사용 예

```
이 문서를 so-what-mece 스킬로 고쳐줘: <문서 링크>
```

```
아래 회의 메모를 주간 보고로 정리해줘. Notion에 붙여 넣을 거야.
<메모 본문>
```

```
이 보고서 초안에서 So What이 약한 부분만 짚어줘.
```

링크로 준 문서를 Claude가 읽으려면 해당 도구의 커넥터(Atlassian, Google Drive, Notion 등)가 연결되어 있어야 합니다. 연결되어 있지 않으면 본문을 붙여 넣으면 됩니다.

## 고치기 전과 후

고치기 전:

```
2. 프로모션 결과

지난주 진행한 무료 배송 프로모션은 전반적으로 좋은 성과를 보였습니다.
참여 매장 매출 1.9배 · 주문 1.8배 · 전환율 6.4 → 9.8%로 크게 회복했습니다.
다만 장기 효과는 아직 확인이 필요합니다.
```

고친 뒤:

```
2. 무료 배송 유효 판정 : 다음 달 전체 매장 확대

- **참여 매장 매출 1.9배 → 전체 매장으로 확대**
  - 매출 1.9배
  - 주문 1.8배
  - 전환율 6.4 → 9.8%
- 사후관리
  - 확대 후 4주 전환율이 8% 미만이면 재검토

비고
- 장기 효과 미확인 : 4주 뒤 재구매율로 재확인
```

## 우선순위

팀이나 개인이 이미 정한 양식과 용어가 있으면 그것이 이 스킬보다 우선합니다. 이 스킬은 따로 정한 것이 없을 때의 기본값입니다.

## 참고한 자료

AI 문체 목록은 [epoko77-ai/im-not-ai](https://github.com/epoko77-ai/im-not-ai)(MIT)의 분류를 참고해 업무 문서에 맞게 추렸습니다. 긴 글을 본격적으로 윤문하려면 그 스킬을 함께 쓰는 것을 권합니다.

## 라이선스

MIT
