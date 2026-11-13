## 후속 수정: Default·Large 기본 상태의 버튼 텍스트 — 2026-11-09

- 사용자 제보: Button Components의 Default > Default와 Large > Default에서 텍스트가 보이지 않으며 Primary 색상 텍스트가 필요함.
- 확인 대상: Secondary / Size=Default / State=Default 원본 1872:3166, Secondary / Size=Large / State=Default 원본 1872:3199. 텍스트 1872:2518·1872:2515.
- 원인: 변수 별칭은 background·primary에 올바르게 연결되어 있었으나 paint의 실제 RGB 값이 검정(0,0,0)으로 남아 원본 캡처에서 글자가 배경과 겹쳐 보였습니다. 앞선 인스턴스 중심 캡처 검수에서는 이 원본 표시 오류를 놓쳤습니다.
- 수정: 변수 연결을 유지하고 실제 소비 노드에서 해석한 컬러를 paint RGB에 동기화했습니다. Light 기준 Secondary 배경 #FFFFFF, 텍스트·테두리 Primary #435CBC. Primary 면형의 텍스트는 기존 primary-foreground 흰색을 유지합니다.
- 같은 방식으로 수정된 Button·Icon Button·ButtonGroupButton·ButtonGroupIconButton의 Primary/Secondary/Third를 확인해 같은 원인의 paint 불일치 총 151건을 바로잡았습니다. 공유 변수 값·별칭·모드는 변경하지 않았습니다.
- 검수: 변경 후 Button 원본 세트를 1배율로 재캡처하여 Default·Large 라인형 기본 상태의 Button 문구가 Primary 색상으로 표시되는 것을 확인했습니다. 해당 원본 텍스트의 visible=true·문구·변수 ID·실제 RGB를 재조회했습니다.
- 결과 링크: https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=1872-3166 및 node-id=1872-3199.
- 이전 검수 완료 표기는 이 제보에 해당하는 원본의 paint 표시 오류를 검출하지 못한 한계가 있으며, 본 후속 수정·재검수 기록으로 보완합니다. 전체 제품 화면과 Dark 시각 검수는 별도입니다.
