# Icon Button·Button Group 규격 확장 — 2026-11-09

상태: Figma 반영 및 요청 범위 AI 검수 완료 / 사용자 검토 전

## 요청과 기준

사용자가 앞선 Button 수정과 동일하게 Icon Button·Button Group도 수정하도록 요청했습니다. Small 32px·Default 40px·Large 48px, Primary(면)·Secondary(라인)·Third(회색 라인), radius-sm 6px를 적용합니다. 아이콘형은 같은 너비·높이의 정사각형입니다. 그룹의 맞닿는 모서리는 radius-none 0px, 바깥쪽 모서리는 6px로 관리합니다.

기존 원본 ID: Icon Button 1892:615, ButtonGroupButton 1882:4083, ButtonGroupIconButton 2201:6503. 파일·페이지는 기존 [TLDS3.0 Components](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=2429-55)입니다.

그룹에는 Primary가 없어 기존 Secondary 라인형의 위치·크기·상태 구조를 복제하고 앞서 수정한 Button Primary의 색상·상태 스타일을 적용합니다. 기존 Outline→Secondary, Secondary→Third로 이름과 외형을 맞추며 Ghost 등 특수 종류, 기존 xs와 아이콘 교체 속성·원본 ID는 유지합니다. 그룹의 Left·Right·Middle·Top·Bottom 위치 구분도 보존합니다.

높이: h-8 / h-10 / h-12. 아이콘 너비: w-8 / w-10 / w-12. 기존 변수 값·별칭·모드는 변경하지 않습니다. 공유 원본 수정에 따라 연결된 인스턴스에도 반영됩니다.

## 검수 결과

- Icon Button 160개 변형, ButtonGroupButton 204개 변형, ButtonGroupIconButton 240개 변형에 적용했습니다. 기존 그룹 원본은 유지하고 Primary 변형 132개를 추가했습니다.
- 전체 604개 변형에서 요청 크기·아이콘 정사각형·위치별 외곽 6px/연결부 0px·보이는 직계 자식의 세로 넘침을 확인했습니다. 오류 및 중복 변형명 0건입니다.
- [Figma 검토 화면](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5213-11856): Small·Default·Large의 세 버튼 종류, 가로 텍스트 그룹·아이콘 그룹, Default/Hover/Focus/Disabled, 세로 Top/Bottom 그룹을 확인했습니다. 96개 예시 인스턴스 모두 원본 연결을 유지합니다.
- 1배율 캡처에서 아이콘·라벨 정렬, 가로·세로 연결부, 외곽 모서리, 상태별 색상과 효과를 확인했습니다. 잘림·누락은 관찰되지 않았습니다. 기존 텍스트의 실제 폰트를 읽어 로드하고 색상 연결만 변경했습니다. 텍스트 크기·굵기·문구와 아이콘 형태는 유지했습니다.
- 앞선 Button 원본의 같은 종류·크기·상태에서 면·테두리·라벨/아이콘 색상·효과·불투명도를 가져왔습니다. 변수 생성·값 수정·모드 수정은 없습니다. Icon Button의 Focused 표기와 그룹의 Focus 표기를 유지했습니다.
- Variant 이름은 Icon Button의 Default→Primary, Outline→Secondary, Secondary→Third, 그룹의 Outline→Secondary, Secondary→Third로 변경했습니다. Size는 sm→Small, default→Default, lg/large→Large입니다. 이름으로 조회하는 외부 작업에는 새 표시값이 필요합니다.

## 미검증 범위

전체 제품 화면·다른 파일 라이브러리 참조·Dark 시각 검수·프론트 구현·실제 앱 동작은 별도입니다. 이번 범위는 지정된 재사용 컴포넌트와 검토 예시입니다.

사용자 검토자:

사용자 검토 결과:

## 후속 수정: Default·Large 기본 상태의 버튼 텍스트 — 2026-11-09

- 사용자 제보: Button Components의 Default > Default와 Large > Default에서 텍스트가 보이지 않으며 Primary 색상 텍스트가 필요함.
- 확인 대상: Secondary / Size=Default / State=Default 원본 1872:3166, Secondary / Size=Large / State=Default 원본 1872:3199. 텍스트 1872:2518·1872:2515.
- 원인: 변수 별칭은 background·primary에 올바르게 연결되어 있었으나 paint의 실제 RGB 값이 검정(0,0,0)으로 남아 원본 캡처에서 글자가 배경과 겹쳐 보였습니다. 앞선 인스턴스 중심 캡처 검수에서는 이 원본 표시 오류를 놓쳤습니다.
- 수정: 변수 연결을 유지하고 실제 소비 노드에서 해석한 컬러를 paint RGB에 동기화했습니다. Light 기준 Secondary 배경 #FFFFFF, 텍스트·테두리 Primary #435CBC. Primary 면형의 텍스트는 기존 primary-foreground 흰색을 유지합니다.
- 같은 방식으로 수정된 Button·Icon Button·ButtonGroupButton·ButtonGroupIconButton의 Primary/Secondary/Third를 확인해 같은 원인의 paint 불일치 총 151건을 바로잡았습니다. 공유 변수 값·별칭·모드는 변경하지 않았습니다.
- 검수: 변경 후 Button 원본 세트를 1배율로 재캡처하여 Default·Large 라인형 기본 상태의 Button 문구가 Primary 색상으로 표시되는 것을 확인했습니다. 해당 원본 텍스트의 visible=true·문구·변수 ID·실제 RGB를 재조회했습니다.
- 결과 링크: https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=1872-3166 및 node-id=1872-3199.
- 이전 검수 완료 표기는 이 제보에 해당하는 원본의 paint 표시 오류를 검출하지 못한 한계가 있으며, 본 후속 수정·재검수 기록으로 보완합니다. 전체 제품 화면과 Dark 시각 검수는 별도입니다.
