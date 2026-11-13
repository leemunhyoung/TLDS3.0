# 비회원 주문조회 Header 및 Button xs28px — 2026-11-12

- 사용자 시안5347:16870을 기준으로 Header 세트5096:12776에 Type=Guest Order Lookup(5350:12522) 추가.
- Button 세트1872:3230의 xs48개 variant를 h-7(VariableID:1044:220)에 연결해28px로 변경. 최종 높이 xs28/Small32/Default36/Large48 확인.
- 새 Header는375×48px. 로고150×30px, 비회원 주문조회 버튼113×28px, 검색24×24px, 우측 간격12px 및 좌우20px 여백을 시안과 동일하게 구성.
- 시안의 Btn Frame을 Button Third/xs/Default 인스턴스5350:12526으로 교체. 버튼 문구는 비회원 주문조회, Text-sm/Medium14px 스타일 적용. 시안의 배경·테두리·모서리 변수 연결을 보존.
- Header 사용 예시5096:12836에 새 인스턴스5350:12536 추가. 사용자 원본 시안은 보존.
- 구조와 실제 높이 검수 완료. 일반 screenshot 결과에서 우측 영역이 누락되어 별도 영역 캡처와 공식 get_screenshot contentsOnly=true로 전체 Header를 재확인했으며 로고·버튼·검색이 정상 표시됨. 주변 형제 프레임의 겹침 없음 확인.
- 사용자 검토 전.
- 결과 https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5350-12522
