# Secondary·Third Hover 구분 — 2026-11-10

상태: Figma 반영 및 Light 화면 검수 완료 / 사용자 검토 전

- 요청: Button의 Secondary·Third에서 Default와 Hover가 구분되도록 수정.
- 범위: Button1872:3230, Icon Button1892:615, ButtonGroupButton1882:4083, ButtonGroupIconButton2201:6503의 Secondary·Third Hover. 앞선 동일 규격 적용 범위에 맞춰 네 계열에 일관 반영했습니다.
- 변경 수: Button16개, Icon Button16개, ButtonGroupButton30개, ButtonGroupIconButton36개, 총98개 Hover 변형.
- Secondary Hover: mode/primary-hover(VariableID:5247:12189)를 추가해 배경에 연결했습니다. Light→tw/colors indigo/50(VariableID:90:162, #ECEFF8), Dark→기존 mode/accent(VariableID:511:703) 별칭. 범위 FRAME_FILL·SHAPE_FILL, WEB 코드 표기 var(--primary-hover).
- Third Hover: 기존 mode/accent(VariableID:511:703)를 배경에 연결했습니다. Light→neutral/100, Dark→neutral/800. 기존 역할 변수와 Dark 설정을 재사용합니다.
- 기존 Primary, Default·Focus·Disabled, 문구·폰트·아이콘·테두리·높이·radius·노드 불투명도 연결은 변경하지 않았습니다. 기존 공유 변수의 값·별칭·모드는 변경하지 않았으며 새 역할 변수1개만 추가했습니다.
- 검증:98개 Hover 원본 모두 한 개의 SOLID 배경과 종류별 정확한 역할 변수 연결을 확인했습니다. 오류0건. [버튼 상태 비교](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5210-15330)와 [아이콘·그룹 상태 비교](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5213-11856)를 캡처해 기본 흰 배경과 Hover의 연한 브랜드색·회색 배경 차이를 확인했습니다.
- 중간 합성 테스트는 최종 산출물에 남기지 않았습니다. 최종 Hover 배경은 불투명 단일 역할 변수입니다. Dark 별칭 구조는 확인했지만 Dark 시각 검수·전체 사용 화면·개발의 실제 마우스 동작은 미검증입니다.

사용자 검토 결과:
