# 메인시안 → Shadcn 매칭

기준일: 2026-11-06 · 상태: 사용자 작성 매칭표 반영 / 디자인 검토 중

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

## 사용자 작성 매칭표 반영 — 2026-11-06 (현행)

이 절은 아래 대상에 대한 과거 후보·미반영 기록을 대체한다. 기준은 [Main Page 작성용 매칭표](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5135-381)와 작업 직전 메인시안이다. 그 외 과거 기록은 변경 이력으로 보존한다.

### Card

- 기존 shadcn Card 예시(1932:3293)를 기본형으로 포함한 [Card 세트](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5140-641)를 추가했다. 기존 Card header/footer 원본은 보존한다.
- Type: Default / Banner with Actions / Thumbnail / Info Banner.
- 유형마다 독립된 Content 교체 속성을 사용해 Type 변경 시 이전 유형의 Content가 따라붙지 않도록 했다. Product Content는 네 상품, Info Content는 포인트·라운지 안내의 현재 구성을 교체한다.
- 이미지·문구·버튼 등이 들어 있는 Card Content 원본을 분리하고 상위 Card에서 인스턴스로 사용한다. 기존 변수 연결은 보존하고 실제 값이 일치하는 여백·글꼴 변수만 추가 연결했다.
- Card 문서 안에 [Banner Card](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5144-11113), [Thumbnail Card](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5144-11149), [Info Banner Card](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5144-11394)를 동등한 프레임으로 배치했다. 문서 제목·설명은 기존 양식에 맞춰 영문으로 작성했다.

| 메인 영역 | Type | 적용 인스턴스 |
|---|---|---|
| 제휴카드 안내 | Banner with Actions | [Affiliate](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5140-642) |
| BEST 상품 1 | Thumbnail | [World Lounge](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5140-735) |
| BEST 상품 2 | Thumbnail | [Matina Gold](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5140-804) |
| BEST 상품 3 | Thumbnail | [Airport Express](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5140-858) |
| BEST 상품 4 | Thumbnail | [eSIM](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5140-912) |
| 포인트 안내 | Info Banner | [Points](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5140-956) |
| 라운지 위치 안내 | Info Banner | [Lounge Location](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5140-1004) |

현재 APP 375px 시안에 맞춘 적용이다. 카드 Content를 다른 조합으로 바꾸거나 문구 길이가 달라질 때는 카드 크기와 내부 정렬을 별도 확인한다. 이번 적용으로 모든 콘텐츠 길이·반응형·상태가 검수되었다고 판단하지 않는다. 버튼 등 내부 요소의 추가 원본 통합·상태 정의는 별도 범위다.

### Service Menu 기반 조합

- 아이콘+텍스트 Item 구조를 공유하는 Service Menu Item 세트에 Info 4개·Bottom 5개 원본을 추가했다.
- [Info Menu](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5142-666): 바로가기 4개. [메인 적용](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5142-667), 335×104.
- [Bottom Menu](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5142-763): 하단 메뉴 5개와 기존 Home Indicator. [메인 적용](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5142-764), 375×90.
- 두 컴포넌트는 [Service Menu 구역](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5129-30069)의 별도 프레임에 원본·예시를 정리했다.
- 기존 아이콘 크기·메뉴명·간격·현재 선택 표시를 유지했다. 새 목적지나 전환 동작·다른 상태 정책을 임의 추가하지 않았다.

### 보류·미확정

- 메인 배너(hero): 이미지와 텍스트 일체형 여부 확정 전까지 원본 유지.
- 광고배너: 광고사 배너 영역으로 미확정, 컴포넌트화하지 않음.
- 퀵 메뉴: 바텀시트/펼침 방식 미확정, 컴포넌트화하지 않음.
- Navigation Menu: Active 의미·스크롤 고정 여부 미확정. 현재 상태 유지.

### 검수 기록

- 변환 전 기준과 최종 적용 9개 인스턴스의 너비·높이, 표시 텍스트 내용·좌표·영역 크기를 비교했고 0.05px 초과 차이 없음.
- Auto Layout·Instance Swap으로 발생한 크기 변동을 수정한 뒤 최종 메인 전체 캡처와 각 Card 유형 예시를 확인했다.
- Card Type 네 가지를 실제 전환하여 기본 Content와 크기가 바뀌는 것을 확인했다.
- 디자인 적용 및 검수 기록이며 사용자 최종 승인, 코드 구현, 실제 앱 동작·전체 Dark·반응형 검수 완료는 아니다.
