# Components 버튼·입력 규격 수정 — 2026-11-09

상태: Figma 반영 및 요청 범위 AI 검수 완료 / 사용자 검토 전

## 요청과 적용 범위

사용자 요청: Button 높이 Small 32px·Default 40px·Large 48px, 버튼 radius 6px 변수 적용, Primary(면)·Secondary(라인)·Third(라인그레이), Input·Input Group·Select 높이 통일.

파일: [TLDS3.0 Components](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=2429-55). 기존 재사용 원본을 수정했습니다. 화면설계서·참고 시안·보관 페이지는 직접 편집하지 않았습니다. 공유 원본 변경에 따른 다른 페이지 인스턴스 반영은 발생할 수 있습니다.

## 실제 변경

| 대상 | 원본 ID | 변경 |
|---|---|---|
| Button | 1872:3230 | sm→Small 32px, default→Default 40px, lg→Large 48px. 모든 모서리 radius-sm 6px. Default→Primary, Outline→Secondary, Secondary→Third. |
| Input | 1928:3990 | Default 40px, Large 48px, 기존 상태별 Small 32px 추가. 32→48개 변형. |
| InputGroup | 2159:2541 | Default 40px, Large 48px, Small 32px 추가. 내부 Addon·Control 높이도 부모와 통일. 16→24개 변형. |
| Select | 2058:943 | 기존 Button 인스턴스가 원본 변경을 따라 Default 40px로 반영. Small·Large도 같은 Button 원본 사용. |
| NativeSelect | 2172:937 | Size 속성 및 Small·Default·Large 추가, 32·40·48px. 4→12개 변형. |

높이 변수: h-8(VariableID:1044:226), h-10(VariableID:1044:225), h-12(VariableID:1044:214). Radius: radius-sm(VariableID:1358:254) → 기존 6px 기본 변수. 기존 공유 변수 값·이름·모드·별칭은 변경하지 않았습니다.

Secondary는 background 면과 primary 테두리·라벨, Third는 background 면과 기존 border 회색 테두리·foreground 라벨에 연결했습니다. 기존 Hover·Focus·Disabled의 불투명도·효과를 유지했습니다. 기존 xs(24px), Ghost·Destructive·Link는 기존 참조 보존을 위해 유지했습니다. Icon Button·Button Group 원본은 이번 변경 대상에 포함하지 않았습니다. Input·InputGroup·NativeSelect의 radius는 요청된 높이와 별개인 기존 규격을 유지했습니다.

## 검수

- [검토 화면](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5210-15330): 크기별 Button 3종·Input·InputGroup·Select·NativeSelect와 버튼 Default/Hover/Focus/Disabled. 33개 인스턴스 모두 원본 연결 유지.
- 원본 4세트의 276개 변형에 대해 요청 크기, 높이 변수, 버튼 6px radius 변수, InputGroup 내부 높이를 확인했습니다. 해당 검사 492건, 오류 0건. 중복 변형명·보이는 직계 자식의 세로 넘침·Button 원본 간 겹침 없음.
- 검토 화면을 1배율 캡처로 확인했습니다. 잘림·프레임 밖 요소 없음. Select 기존 예시 5개의 Default 40px 연결을 확인했습니다.
- Pretendard Regular·Medium 및 버튼 텍스트에서 사용한 글꼴을 실제 로드했습니다. 글꼴 크기·굵기·기존 타이포 변수는 유지했습니다.
- 컬러 v1 팔레트 28개와 Primary Light→indigo/500(#435CBC)의 현재 값·별칭을 대조했습니다. 값 변경 없음. Dark 변수 및 모드는 변경하지 않았습니다. Dark 시각 검수는 하지 않았습니다.
- 기존 Button의 일부 변형은 Label 속성과 실제 텍스트 연결이 없는 상태였습니다. 원본의 해당 구조는 그대로 두고 검토용 인스턴스에만 표시 라벨을 직접 적용했습니다.

## 영향과 미검증 범위

Button의 Variant·Size 표시값이 변경됐으므로 이를 이름으로 조회하는 외부 작업은 새 이름을 사용해야 합니다. 원본 ID와 기존 상태·아이콘·인스턴스 관계는 유지했습니다. 전체 파일의 모든 참조 화면·다른 파일 라이브러리 사용·실제 앱·프론트 구현·키보드 동작은 검증하지 않았습니다. 공유 원본 반영으로 영향을 받는 실제 화면은 별도 화면 검수가 필요합니다.

사용자 검토자:

사용자 검토 결과:

기준 커밋:

프로젝트 공통 웹 가이드는 이번 작업에서 재조회하지 않았습니다. 로컬 디자인 기준과 이번 사용자 요청을 적용했습니다.

## 후속 수정: Default·Large 기본 상태의 버튼 텍스트 — 2026-11-09

- 사용자 제보: Button Components의 Default > Default와 Large > Default에서 텍스트가 보이지 않으며 Primary 색상 텍스트가 필요함.
- 확인 대상: Secondary / Size=Default / State=Default 원본 1872:3166, Secondary / Size=Large / State=Default 원본 1872:3199. 텍스트 1872:2518·1872:2515.
- 원인: 변수 별칭은 background·primary에 올바르게 연결되어 있었으나 paint의 실제 RGB 값이 검정(0,0,0)으로 남아 원본 캡처에서 글자가 배경과 겹쳐 보였습니다. 앞선 인스턴스 중심 캡처 검수에서는 이 원본 표시 오류를 놓쳤습니다.
- 수정: 변수 연결을 유지하고 실제 소비 노드에서 해석한 컬러를 paint RGB에 동기화했습니다. Light 기준 Secondary 배경 #FFFFFF, 텍스트·테두리 Primary #435CBC. Primary 면형의 텍스트는 기존 primary-foreground 흰색을 유지합니다.
- 같은 방식으로 수정된 Button·Icon Button·ButtonGroupButton·ButtonGroupIconButton의 Primary/Secondary/Third를 확인해 같은 원인의 paint 불일치 총 151건을 바로잡았습니다. 공유 변수 값·별칭·모드는 변경하지 않았습니다.
- 검수: 변경 후 Button 원본 세트를 1배율로 재캡처하여 Default·Large 라인형 기본 상태의 Button 문구가 Primary 색상으로 표시되는 것을 확인했습니다. 해당 원본 텍스트의 visible=true·문구·변수 ID·실제 RGB를 재조회했습니다.
- 결과 링크: https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=1872-3166 및 node-id=1872-3199.
- 이전 검수 완료 표기는 이 제보에 해당하는 원본의 paint 표시 오류를 검출하지 못한 한계가 있으며, 본 후속 수정·재검수 기록으로 보완합니다. 전체 제품 화면과 Dark 시각 검수는 별도입니다.
