# 컬러 기준과 작업 전 변경 확인

컬러 기준 버전: v1 · 2026-11-05 · 사용자 제공 수정본 Colors(1).png 적용

[실제 Figma 컬러 가이드](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5075-39) · 위치: Color 페이지

## 기준 구조

- 기존 `tw/colors` 컬렉션(`VariableCollectionId:89:14`)의 `indigo/50~900`을 Brand Color로, `gray/50~900`을 Gray로 사용한다. 기존 Indigo 기본값을 그대로 사용하는 것이 아니라 사용자 수정 HEX로 변경한 값이다.
- 같은 컬렉션에 `system/*`, `system-bg/*` 각 4개를 추가했다.
- Primary는 기존 `mode/primary`(`VariableID:424:349`)의 Light 값 → `indigo/500` 별칭이다. 최종 표시값은 #435CBC.
- Brand Color 1과 별도 CTA 팔레트·역할은 사용 대상에서 제외했다. #131920은 Gray 900으로 남으며 CTA 역할을 뜻하지 않는다.
- White 및 기존 공유 변수, 950 단계, 다른 팔레트, rdx/colors는 의존 관계 보존을 위해 이번에 삭제하지 않았다. 새 컴포넌트의 컬러 선택은 아래 사용 팔레트를 기준으로 한다.
- 기존 Shadcn 의미 변수의 역할을 유지한다. Gray 전체를 foreground·border 등에 임의 배정하지 않는다. System도 destructive 등 모든 의미 변수에 자동 연결하지 않았다.
- Dark 모드는 원래 값을 보존한다. 현재 작업 범위는 Light 컬러 커스텀과 기존 Shadcn Dark 설정 보존이며, 지금 Light/Dark 팔레트를 새로 매칭하는 작업은 요구하지 않는다.
- 로컬 스타일: `TLDS/Brand/*`, `TLDS/Gray/*`, `TLDS/System/*`, `TLDS/System-bg/*`, `TLDS/Role/primary`. 29개 모두 변수 바인딩이다.

## 사용 팔레트 기준값

| 변수 경로(tw/colors) | HEX | 현재 변수 ID |
|---|---|---|
| `indigo/50` | `#ECEFF8` | `VariableID:90:162` |
| `indigo/100` | `#D9DEF2` | `VariableID:90:163` |
| `indigo/200` | `#B4BEE4` | `VariableID:90:164` |
| `indigo/300` | `#697CC9` | `VariableID:90:165` |
| `indigo/400` | `#566CC2` | `VariableID:90:166` |
| `indigo/500` | `#435CBC` | `VariableID:90:167` |
| `indigo/600` | `#364996` | `VariableID:90:168` |
| `indigo/700` | `#283771` | `VariableID:90:169` |
| `indigo/800` | `#1B254B` | `VariableID:90:170` |
| `indigo/900` | `#0D1226` | `VariableID:90:171` |
| `gray/50` | `#F0F2F5` | `VariableID:90:30` |
| `gray/100` | `#E7EBEE` | `VariableID:90:31` |
| `gray/200` | `#DCE0E4` | `VariableID:90:32` |
| `gray/300` | `#C6CCD2` | `VariableID:90:33` |
| `gray/400` | `#B0B8C1` | `VariableID:90:34` |
| `gray/500` | `#8B95A1` | `VariableID:90:35` |
| `gray/600` | `#6B7684` | `VariableID:90:36` |
| `gray/700` | `#4E5968` | `VariableID:90:37` |
| `gray/800` | `#333D4B` | `VariableID:90:38` |
| `gray/900` | `#131920` | `VariableID:90:39` |
| `system/info` | `#2578F8` | `VariableID:5075:2` |
| `system/error` | `#D32F2F` | `VariableID:5075:3` |
| `system/warning` | `#E65100` | `VariableID:5075:4` |
| `system/success` | `#2E7D32` | `VariableID:5075:5` |
| `system-bg/info` | `#E3F2FD` | `VariableID:5075:6` |
| `system-bg/error` | `#FDE8E8` | `VariableID:5075:7` |
| `system-bg/warning` | `#FFF3E0` | `VariableID:5075:8` |
| `system-bg/success` | `#E8F5E9` | `VariableID:5075:9` |

## 확인된 역할 연결

| 용도 | 변수 | 상태 |
|---|---|---|
| Primary | mode/primary Light → indigo/500 | #435CBC |
| GNB Active 텍스트·밑줄 | mode/primary | 연결 |
| GNB Default 텍스트 | tw/colors gray/600 | #6B7684에 연결. 메인 외부 변수 직접 참조 제거 |
| 기타 의미 컬러 | 기존 Shadcn 의미 변수 | 기존 연결 유지. 개별 역할 매칭 후 수정 |

## 모든 AI 작업 시작 전 필수 확인

1. 이 문서와 최신 사용자 요청·변경 기록을 읽는다. 대화 기억이나 오래된 이미지에서 색을 가져오지 않는다.
2. Figma에서 실제 컬렉션·모드·변수 ID/경로, HEX 및 별칭 관계를 읽는다. 위 28개 팔레트와 Primary 연결을 작업마다 대조한다. 같은 HEX라도 잘못된 역할·외부 변수 연결인지 확인한다.
3. 기준 HEX는 sRGB 채널을 0~255로 반올림해 비교한다. 알파와 paint opacity, 명시적 Light/Dark 모드도 따로 확인한다.
4. 변경 또는 불일치가 있으면 작업 기록에 이전 기준·현재 값·변경 근거·영향 범위를 남긴다. 가이드 견본·로컬 스타일도 변수와 같은 값을 표시하는지 확인한다.
5. 사용자의 최신 요청으로 승인된 변경이면 허용 범위에서 적용하고 기준표·버전·변경 이력을 갱신한다. 이미 승인한 내용을 반복 확인받지 않는다.
6. 승인 근거가 없는 차이는 자동으로 옛 값으로 복원하거나 현재 값을 새 기준으로 확정하지 않는다. 영향받는 컬러 적용을 보류하고 필요한 확인을 요청한다. 영향 없는 작업은 계속한다.
7. 읽을 수 없으면 '확인 불가'로 보고한다. 확인하지 않고 변경 없음·검수 통과로 처리하지 않는다.

작업 중 새 컬러가 필요하면 기존 역할 변수로 가능한지 먼저 확인한다. 임의 HEX를 넣거나 비슷한 색이라는 이유로 다른 역할 변수를 사용하지 않는다. 확장 필요 시 용도·값·영향을 제안한다.

## 완료 검수와 변경 이력

- 팔레트 HEX 28개 및 Primary 별칭 재조회 완료. 모두 기준값 일치.
- mode 컬렉션의 Dark 값은 작업 전후 동일함을 확인.
- 변수 20개 값 갱신, 시스템 변수 8개 추가, Primary Light 별칭 변경. 기존 변수 삭제 없음.
- 2026-11-05: 수정된 Colors(1).png를 기준으로 v1 설정. Brand Color 1·CTA 제외. 컬러 변수·로컬 스타일·가이드 추가.
- 새로 바뀐 컬러는 이 이력에 날짜·변수·이전/새 값·요청 근거를 추가한다.

- 2026-11-05: 기존 컬러 가이드를 사용자 생성 Color 페이지로 이동하고 제공 이미지 형태로 재배치. 가이드 노드 ID와 컬러 변수 값 유지.
