# 메인시안 → Shadcn 매칭

기준일: 2026-11-04 · 상태: 부분 반영 / 검토 중

기준: [Main Page / #비로그인](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5050-3170), APP 375px. 메인 원본은 수정하지 않는다. 메인에서 관찰한 값과 모든 화면에 적용할 확정 정책을 구분한다.

| 메인 요소 | Shadcn 대응 | 확인된 근거 | 처리 |
|---|---|---|---|
| 채움형 버튼 | Button / Default | 메인 카드 등록·구매 버튼 | 기본 상태 default(32px)·lg(40px), 반경 4px, Pretendard 14px Bold 반영 |
| 브랜드 외곽선 버튼 | Button / Outline | 메인 카드 알아보기·사용처 버튼 | 위 2개 크기의 기본 상태, 브랜드 테두리·텍스트 반영 |
| 상단 서비스 메뉴 | Tabs 또는 Navigation Menu 조합 | 48px 높이, 16px 글자, 선택 Bold·비선택 Regular | 페이지 이동인지 패널 전환인지 동작 근거를 확인한 뒤 선택. 외형만 보고 Tabs로 확정하지 않음 |
| 인기·New 배지 | Badge 후보 | 반경 4px, 11px, 패딩 상하 2px·좌우 4px | 여러 색상·역할이 있으므로 공통 Badge 전체에 단일 값 적용 보류 |
| 제휴카드 안내 영역 | Card 기반 조합 후보 | 내부 패딩 20px, 간격 16px, 반경 8px, 배경 #F0F2F5 | 기본 Card 전체와 동일하다고 확정하지 않음 |
| 상품 카드·목록 | Card + Button + 이미지/텍스트 조합 | 2열, 열 간격 12px, 내부 간격 8·4·2px | 조합 패턴. 단일 Card에 모든 내용을 고정하지 않음 |
| 제목·본문·보조 | 기존 타이포 변수 매칭 | 18px Bold / 14px Regular / 12px Regular 등 | 역할별 관찰값. 폼 제목·라벨 규칙으로 일괄 확장하지 않음 |
| 배너 강조 문구 | 배너 전용 타이포 후보 | Gmarket Sans Bold 22px | 제품 UI의 Pretendard와 구분. 전역 서체 교체하지 않음 |
| 화면 여백 | 기존 spacing 변수 매칭 | 주요 콘텐츠 좌우 20px, 섹션 패딩 상하 20px, 내부 16px | 메인에서 관찰한 관계 기준. 모든 gap을 16px로 통일하지 않음 |

## 이번 반영

[버튼 검토용 인스턴스](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5054-12609)

- 기존 Button 원본 4개를 수정했다. Variant/Size/State/원본 ID와 인스턴스 관계를 유지한다.
- 기존 높이 h-8·h-10, 반경 rounded-sm(4px), size/sm(14px), weight/bold(700)를 연결했다.
- 기존 primary의 Light 값은 메인에서 사용하는 브랜드 변수 별칭으로 연결했다. 실제 표시 색은 약 #435CBC다. primary-foreground Light는 기존 white 변수로 연결했다.
- 공유 영향: Light의 primary·primary-foreground를 참조하는 다른 컴포넌트와 기존 서브페이지에도 색상 변경이 전파된다. 전체 화면의 시각 검수 완료를 뜻하지 않는다.
- Dark 모드 값과 변수 컬렉션·이름·모드·타입은 유지했다.
- 버튼 기본 4개는 검토용 인스턴스 캡처로 확인했다. 고객 승인 또는 전체 Button 확정 상태가 아니다.

## 남은 기준

- Hover·Focus·Disabled는 메인에 근거가 없어 기존 설정 유지. 공유 색상 변경의 상태별 조화 검토가 필요하다.
- xs·sm 및 Rounded 변형은 크기 매칭 미확정으로 직접 수정하지 않았다.
- 메인에 없는 라벨–인풋 간격, 플레이스홀더, 오류·포커스 표현은 기존 Shadcn 설정을 유지하고 미확정으로 남긴다.
- 대표 서브 레이아웃과 연결한 후 폼 간격·제목 계층을 결정한다.
- 카드·배지·탭의 상세 반영 및 다른 화면의 영향 검수는 후속 작업이다.
