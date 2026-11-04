# 메인시안 타이포그래피 연결 결과

기준일: 2026-11-04 · [기준 프레임](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5050-3170)

## 적용 결과

- 텍스트 84개 중 80개에 기존 타이포 변수 연결 306건 적용.
- Family·Weight·Size·Line height·Letter spacing 중 정확히 일치하는 속성만 연결했다.
- 기존 변수 컬렉션·이름·값·모드는 변경하지 않았다. 새 변수와 텍스트 스타일을 생성하지 않았다.
- 혼합 굵기는 텍스트 구간별로 연결했다. 현재 텍스트 문구·폭·높이 변화가 없음을 확인하고 캡처를 검토했다.
- 컬러는 기존 상태를 유지했다. 기존 텍스트 스타일에 맞추기 위해 다른 속성을 덮어쓰지 않았다.

## 기존 시스템에 없는 값

| 항목 | 미존재 값 | 처리 |
|---|---|---|
| Font size | 10·11·17·22px | 원래 값 유지 |
| Font family | Gmarket Sans | 원래 서체 유지. 현재 환경에서 로드할 수 없어 해당 4개 텍스트 연결 보류 |
| Line height | 22px, 100·120·130·150%, Auto | 원래 값·단위 유지. 기존 leading 숫자 변수는 px 기준이므로 비율값 직접 연결 금지 |
| Letter spacing | 약 -0.408px, -0.2px, -2·-3·-5% | 원래 값·단위 유지. 가까운 변수로 대체하지 않음 |

한 텍스트에 일부 속성은 연결되고 일부는 미연결일 수 있다. Gmarket Sans가 없는 것과 현재 환경에서 로드되지 않는 것은 별개 사유다. 신규 토큰 추가·서체 업로드·스타일 통일은 별도 결정한다.

## 노드별 미연결 속성

텍스트 구간별 기록이다. 동일 노드에서 서로 다른 굵기가 사용되면 여러 행으로 나타날 수 있다.

| 노드 링크 | 해당 문구 | 미연결 속성·사유 |
|---|---|---|
| [I5050:3172;5526:2400;839:7100](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3172;5526-2400;839-7100) | 9:41 | fontSize 17 / lineHeight 22px / letterSpacing -0.40799999237060547px |
| [I5050:3173;6867:25057](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3173;6867-25057) | 1 | 행간 100% / fontSize 10 / letterSpacing -0.20000000298023224px |
| [I5050:3174;6870:32407](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3174;6870-32407) | 라운지 | 행간 150% |
| [I5050:3174;6870:32409](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3174;6870-32409) | 공항F&B | 행간 150% |
| [I5050:3174;6982:29651](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3174;6982-29651) | 공항교통 | 행간 150% |
| [I5050:3174;6870:32411](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3174;6870-32411) | 해외이심 | 행간 150% |
| [I5050:3174;6870:32413](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3174;6870-32413) | 투어·티켓 | 행간 150% |
| [I5050:3174;7087:61210](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3174;7087-61210) | 호텔 | 행간 150% |
| [I5050:3174;7087:61273](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3174;7087-61273) | 골프 | 행간 150% |
| [I5050:3174;7123:36176](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3174;7123-36176) | 이벤트 | 행간 150% |
| [I5050:3174;7123:36249](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3174;7123-36249) | 공항할인쿠폰 | 행간 150% |
| [5050:3179](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5050-3179) | 1 | 행간 150% / fontSize 11 |
| [5050:3180](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5050-3180) | / | 행간 150% |
| [5050:3181](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5050-3181) | 5 | 행간 150% / fontSize 11 |
| [5050:3189](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5050-3189) | 돌아오는 공항 | 행간 120% / 자간 -5% / fontFamily Gmarket Sans / 글꼴 로드 불가: Gmarket Sans / fontSize 22 |
| [5050:3190](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5050-3190) | 에서도 | 행간 120% / fontSize 22 |
| [5050:3192](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5050-3192) | 해외라운지 | 행간 120% / 자간 -5% / fontFamily Gmarket Sans / 글꼴 로드 불가: Gmarket Sans / fontSize 22 |
| [5050:3193](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5050-3193) | 쉽게 찾기! | 행간 120% / fontSize 22 |
| [I5050:3196;7109:31635](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3196;7109-31635) | 공항라운지 | 행간 150% |
| [I5050:3196;7109:31637](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3196;7109-31637) | 인기 | 행간 100% / fontSize 11 / letterSpacing -0.20000000298023224px |
| [I5050:3196;7109:34056](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3196;7109-34056) | 공항다이닝 | 행간 150% |
| [I5050:3196;7109:31642](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3196;7109-31642) | 공항리무진 | 행간 150% |
| [I5050:3196;7109:34373](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3196;7109-34373) | 공항직통열차 | 행간 150% |
| [I5050:3196;7109:31678](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3196;7109-31678) | 더라운지eSIM | 행간 150% |
| [I5050:3196;7109:31680](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3196;7109-31680) | New | 행간 100% / fontSize 11 / letterSpacing -0.20000000298023224px |
| [I5050:3196;7109:31646](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3196;7109-31646) | 패스트트랙 | 행간 150% |
| [I5050:3196;7109:31693](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3196;7109-31693) | 투어/티켓 | 행간 150% |
| [I5050:3196;7109:35469](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3196;7109-35469) | 호텔브런치 | 행간 150% |
| [I5050:3197;7097:42351](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3197;7097-42351) | 더라운지  | 행간 130% / 자간 -3% |
| [I5050:3197;7097:42351](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3197;7097-42351) | 회원 10명 중 9명 | 행간 130% / 자간 -3% |
| [I5050:3197;7097:42351](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3197;7097-42351) | 은 / 제휴카드로  | 행간 130% / 자간 -3% |
| [I5050:3197;7097:42351](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3197;7097-42351) | 라운지를 무료 이용 | 행간 130% / 자간 -3% |
| [I5050:3197;7097:42351](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3197;7097-42351) | 하고 있어요 | 행간 130% / 자간 -3% |
| [I5050:3197;7097:42354](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3197;7097-42354) | 제휴카드 알아보기 | 행간 Auto |
| [I5050:3197;7097:42356](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3197;7097-42356) | 제휴카드 등록 | 행간 150% |
| [I5050:3198;7095:36620](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3198;7095-36620) | 더라운지 BEST 상품 | 행간 150% |
| [I5050:3198;7095:38773](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3198;7095-38773) | 전세계 라운지 이용권 | 행간 150% |
| [I5050:3198;7095:38777](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3198;7095-38777) | 35,000 | 행간 150% |
| [I5050:3198;7095:38778](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3198;7095-38778) | 부터 | 행간 150% |
| [I5050:3198;6774:32493](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3198;6774-32493) | 사용처 | 행간 Auto |
| [I5050:3198;7080:35732](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3198;7080-35732) | 구매하기 | 행간 Auto |
| [I5050:3198;7095:38258](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3198;7095-38258) | 마티나 골드 이용권 | 행간 150% |
| [I5050:3198;7095:38260](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3198;7095-38260) | 77,000원 | 행간 100% |
| [I5050:3198;7095:38263](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3198;7095-38263) | 42% | 행간 100% |
| [I5050:3198;7095:38266](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3198;7095-38266) | 45,000 | 행간 150% |
| [I5050:3198;7095:38267](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3198;7095-38267) | 원 | 행간 150% |
| [I5050:3198;7080:36109](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3198;7080-36109) | 사용처 | 행간 Auto |
| [I5050:3198;7080:36114](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3198;7080-36114) | 구매하기 | 행간 Auto |
| [I5050:3198;7095:39177](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3198;7095-39177) | 공항 직통열차 예매권 | 행간 150% |
| [I5050:3198;7095:39179](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3198;7095-39179) | 13,000원 | 행간 100% |
| [I5050:3198;7095:39182](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3198;7095-39182) | 8% | 행간 100% |
| [I5050:3198;7095:39185](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3198;7095-39185) | 12,000 | 행간 150% |
| [I5050:3198;7095:39186](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3198;7095-39186) | 원 | 행간 150% |
| [I5050:3198;7080:36505](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3198;7080-36505) | 사용처 | 행간 Auto |
| [I5050:3198;7080:36510](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3198;7080-36510) | 구매하기 | 행간 Auto |
| [I5050:3198;7095:36692](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3198;7095-36692) | 최대 37% 할인 | 행간 100% / fontSize 11 / letterSpacing -0.20000000298023224px |
| [I5050:3198;7095:37730](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3198;7095-37730) | 더라운지 eSIM | 행간 150% |
| [I5050:3198;7095:37734](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3198;7095-37734) | 4,600 | 행간 150% |
| [I5050:3198;7095:37735](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3198;7095-37735) | 부터 | 행간 150% |
| [I5050:3198;7080:37027](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3198;7080-37027) | 구매 / 충전 하기 | 행간 Auto |
| [I5050:3198;7115:49733](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3198;7115-49733) | 더보기 | 행간 150% |
| [I5050:3199;7142:37260](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3199;7142-37260) | 1 | 행간 150% / fontSize 11 |
| [I5050:3199;7142:37261](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3199;7142-37261) | / | 행간 150% |
| [I5050:3199;7142:37262](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3199;7142-37262) | 3 | 행간 150% / fontSize 11 |
| [I5050:3199;7142:37266](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3199;7142-37266) | Pay | 행간 Auto |
| [I5050:3199;7142:37267](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3199;7142-37267) | 손해보험 | 행간 150% |
| [I5050:3199;7142:37269](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3199;7142-37269) | 안전 귀국 시  | 행간 120% / 자간 -5% / fontFamily Gmarket Sans / 글꼴 로드 불가: Gmarket Sans / fontSize 22 |
| [I5050:3199;7142:37270](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3199;7142-37270) | 10% 캐시백 | 행간 120% / 자간 -5% / fontFamily Gmarket Sans / 글꼴 로드 불가: Gmarket Sans / fontSize 22 |
| [I5050:3199;7142:37271](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3199;7142-37271) | (최대 3만원) | 행간 100% / 자간 -2% |
| [I5050:3199;7142:37273](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3199;7142-37273) | AD | 행간 150% / fontSize 10 |
| [5050:3204](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5050-3204) | 광고 보고 포인트 받기 | 행간 150% |
| [5050:3205](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=5050-3205) | 매일 선물상자 열고 포인트 받아가세요. | 행간 150% |
| [I5050:3213;6014:6093](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3213;6014-6093) | 고객지원 | 행간 150% |
| [I5050:3213;6014:6101](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3213;6014-6101) | 공지사항 | 행간 Auto |
| [I5050:3213;6303:19742](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3213;6303-19742) | 고객센터 | 행간 Auto |
| [I5050:3213;6014:6108](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3213;6014-6108) | FAQ | 행간 Auto |
| [I5050:3213;6014:6121](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3213;6014-6121) | 이용안내 | 행간 Auto |
| [I5050:3214;6000:11970](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3214;6000-11970) | 인천국제공항 라운지 위치 | 행간 150% |
| [I5050:3214;6000:11971](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3214;6000-11971) | 탑승게이트에서 가까운 라운지는 어디? | 행간 150% |
| [I5050:3214;7097:42646](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3214;7097-42646) | 1 | 행간 150% / fontSize 11 |
| [I5050:3214;7097:42647](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3214;7097-42647) | / | 행간 150% |
| [I5050:3214;7097:42648](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3214;7097-42648) | 10 | 행간 150% / fontSize 11 |
| [I5050:3216;5671:11996](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3216;5671-11996) | 홈 | 행간 150% / fontSize 11 |
| [I5050:3216;6901:23027](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3216;6901-23027) | 사용처 탐색 | 행간 150% / fontSize 11 |
| [I5050:3216;6901:23224](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3216;6901-23224) | 이용권 구매 | 행간 150% / fontSize 11 |
| [I5050:3216;6901:23229](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3216;6901-23229) | 마이 | 행간 150% / fontSize 11 |
| [I5050:3216;6901:23237](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3216;6901-23237) | 전체 메뉴 | 행간 150% / fontSize 11 |
| [I5050:3217;7097:40807](https://www.figma.com/design/1Qe6U3JD2oHDmofvcKr4ho/TLDS3.0?node-id=I5050-3217;7097-40807) | 퀵 메뉴 | 행간 100% |
