# 메인시안 → Shadcn 매칭

기준일: 2026-11-04 · 상태: 부분 반영 / 검토 중

기준: [Main Page / #비로그인](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5050-3170), APP 375px. 메인 원본은 수정하지 않는다. 메인에서 관찰한 값과 모든 화면에 적용할 확정 정책을 구분한다.

| 메인 요소 | Shadcn 대응 | 확인된 근거 | 처리 |
|---|---|---|---|
| 채움형 버튼 | Button / Default | 메인 카드 등록·구매 버튼 | 기본 상태 default(32px)·lg(40px), 반경 4px, Pretendard 14px Bold 반영 |
| 브랜드 외곽선 버튼 | Button / Outline | 메인 카드 알아보기·사용처 버튼 | 위 2개 크기의 기본 상태, 브랜드 테두리·텍스트 반영 |
| 상단 서비스 메뉴 | GNB Text Link / 탐색 링크 패턴 | 사용자 확인: 서브페이지 이동용. 48px 높이, 16px, Active Bold·Default Regular | Default/Active 생성. Default gray/600, Active primary. Tabs/명령 Button으로 취급하지 않음 |
| 인기·New 배지 | Badge 후보 | 반경 4px, 11px, 패딩 상하 2px·좌우 4px | 여러 색상·역할이 있으므로 공통 Badge 전체에 단일 값 적용 보류 |
| 제휴카드 안내 영역 | Card 기반 조합 후보 | 내부 패딩 20px, 간격 16px, 반경 8px, 배경 #F0F2F5 | 기본 Card 전체와 동일하다고 확정하지 않음 |
| 상품 카드·목록 | Card + Button + 이미지/텍스트 조합 | 2열, 열 간격 12px, 내부 간격 8·4·2px | 조합 패턴. 단일 Card에 모든 내용을 고정하지 않음 |
| 제목·본문·보조 | 기존 타이포 변수 매칭 | 18px Bold / 14px Regular / 12px Regular 등 | 역할별 관찰값. 폼 제목·라벨 규칙으로 일괄 확장하지 않음 |
| 배너 강조 문구 | 배너 전용 타이포 후보 | 원래 Gmarket Sans Bold 22px → Pretendard Bold 22px | 사용자 요청으로 배너 4개 교체. 이미지 일체형/텍스트 분리 방식은 미확정 |
| 화면 여백 | 기존 spacing 변수 매칭 | 주요 콘텐츠 좌우 20px, 섹션 패딩 상하 20px, 내부 16px | 메인에서 관찰한 관계 기준. 모든 gap을 16px로 통일하지 않음 |

## 이번 반영

[버튼 검토용 인스턴스](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5054-12609)

- 기존 Button 원본 4개를 수정했다. Variant/Size/State/원본 ID와 인스턴스 관계를 유지한다.
- 기존 높이 h-8·h-10, 반경 rounded-sm(4px), size/sm(14px), weight/bold(700)를 연결했다.
- 기존 primary의 Light 값은 2026-11-05 컬러 기준에 따라 로컬 tw/colors indigo/500 별칭으로 연결했다. 실제 표시 색은 #435CBC다. primary-foreground Light는 기존 white 변수로 연결했다.
- 공유 영향: Light의 primary·primary-foreground를 참조하는 다른 컴포넌트와 기존 서브페이지에도 색상 변경이 전파된다. 전체 화면의 시각 검수 완료를 뜻하지 않는다.
- Dark 모드 값과 변수 컬렉션·이름·모드·타입은 유지했다.
- 버튼 기본 4개는 검토용 인스턴스 캡처로 확인했다. 고객 승인 또는 전체 Button 확정 상태가 아니다.

## 남은 기준

- Hover·Focus·Disabled는 메인에 근거가 없어 기존 설정 유지. 공유 색상 변경의 상태별 조화 검토가 필요하다.
- xs·sm 및 Rounded 변형은 크기 매칭 미확정으로 직접 수정하지 않았다.
- 메인에 없는 라벨–인풋 간격, 플레이스홀더, 오류·포커스 표현은 기존 Shadcn 설정을 유지하고 미확정으로 남긴다.
- 대표 서브 레이아웃과 연결한 후 폼 간격·제목 계층을 결정한다.
- 카드·배지·탭의 상세 반영 및 다른 화면의 영향 검수는 후속 작업이다.

## 컬러 기준 갱신 — 2026-11-05

[컬러 기준 v1](colors.md)을 따른다. [GNB 링크 상태](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5069-12633)는 Default gray/600, Active primary에 연결했다. 실제 링크 목적지와 Hover/Focus 동작은 이번 범위에서 구현하지 않았다.

## 메인 GNB 교체 완료 — 2026-11-05

- [메인 GNB](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5077-18682)의 표시 링크 9개를 기존 [GNB Text Link](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5069-12633) 인스턴스로 교체했다. 이는 Shadcn 탐색 역할에 맞춘 더 라운지 전용 확장 컴포넌트이며 기존 Navigation Menu 원본의 직접 인스턴스는 아니다.
- 라운지 Active 1개, 나머지 Default 8개. 문구·순서·개별 너비·높이 48px·좌우 여백 20px·항목 간격 16px 유지. 기존 숨김 항목 2개 보존.
- 컬러 기준 28개를 실제 값과 대조해 일치 확인. 글꼴·크기·굵기·상태 색상 및 컨테이너 간격은 기존 변수에 연결.
- 기존 프로토타입에 링크 목적지가 없어 URL이나 전환 동작을 임의 추가하지 않았다. 현재 작업은 디자인 인스턴스 교체이며 실제 서비스 링크 구현 완료를 뜻하지 않는다.
- GNB 캡처로 표시 상태 확인. 나머지 헤더·본문은 변경하지 않았다.

## Navigation Menu 직접 수정으로 변경 — 2026-11-05

이 절은 앞선 GNB Text Link 별도 확장 방식을 대체한다. 사용자 지시에 따라 기존 NavigationMenuItem 원본 세트(2111:6527)의 LTR Default(2111:6526)를 메인 텍스트 링크로 직접 수정하고 Active(5091:12634)를 추가했다. 별도 Type=GNB는 사용하지 않는다. 메인 9개 인스턴스도 이 원본으로 교체했다. 라벨·16px·높이48px·밑줄3px·기존 너비·순서 유지와 원본 연결을 캡처 및 구조로 검증했다. 기존 Hover·RTL의 상세 스타일은 유지, 후속 검토 범위다. 이전 별도 GNB Text Link는 Legacy로 표시하고 신규 사용하지 않는다. 기존 검토용 인스턴스 참조가 남아 있어 자동 삭제하지 않았다.
