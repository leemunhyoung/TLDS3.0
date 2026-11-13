# Button 높이 및 퀵메뉴 변경 — 2026-11-12

- 사용자 지정 규격은 xs 기존24px, Small32px, Default36px, Large48px.
- Button 원본1872:3230의 Default48개 variant를 h-9(VariableID:1044:219),36px로 연결. Small48개는 이미32px였음. 전체192개 variant의 실제 높이24/32/36/48 확인 및 대표4종 캡처 검수.
- Main Page의 퀵메뉴도 Default36px로 맞춤. 기존 외부 컴포넌트의 내부 크기 override가 반영되지 않아 두 퀵메뉴 컨테이너를 편집 가능한 Frame으로 변환하고 공용 Button Primary/Default/Rounded(1891:2700) 인스턴스로 교체. 기존 문구·배경·그림자·둥근 외형 유지, lucide/plus(128:2064) 사용.
- 이전 외부 인스턴스5050:3217 → 컨테이너5344:900 / 버튼5344:906. 이전5208:19164 → 컨테이너5344:917 / 버튼5344:923. 편집 시안5208:19149의 퀵메뉴 버튼5344:934, 상단 이동 버튼5208:19156도36px.
- 실제3개 퀵메뉴 버튼의 Size=Default 및 높이36px, 문구 퀵 메뉴, radius34px 확인. 최종 캡처 검수. 기존 원격 퀵메뉴 연결은 공용 Button 연결로 대체됨.
- Icon Button·Button Group·Input·Tabs·Social Login Button 크기는 이번 요청에 포함하지 않음.
