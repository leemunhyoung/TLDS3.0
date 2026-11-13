# 소셜 로그인 아이콘 수집

수집일: 2026-11-10. 각 서비스의 공식 로그인 디자인 자료를 내려받았습니다. 앱의 일반 로고나 임의 제작 아이콘으로 대체하지 않았습니다. 수집 이후 Figma 적용 내용은 ../../tasks/2026-11-10-social-login-buttons.md와 ../../tasks/2026-11-10-auth-social-button-followups.md에 기록했습니다.

## 바로 사용할 파일

`ready-to-use/`에 선택본을 모았습니다. 파일명만 정리했으며 도형·색상·여백은 원본 그대로입니다.

| 서비스 | 선택본 | 원본 형식과 범위 |
|---|---|---|
| 카카오 | kakao-login-icon.svg / .png | 공식 말풍선 원형 아이콘. PNG @4x 및 SVG. 전체 한국어·영어 버튼도 kakao/에 포함 |
| 네이버 | naver-login-icon-green.png / naver-login-icon-white.png | 공식 녹색·흰색 배경 아이콘형 H56 원본. AI 파일은 originals/에 보존 |
| 구글 | google-login-icon-light.svg / google-login-icon-dark.svg / google-login-icon-round.svg | 공식 Android+Web 아이콘 전용 SVG. 전체 PNG·SVG는 google/에 포함 |
| 애플 | apple-login-icon-black.svg / apple-login-icon-white.svg | 공식 Logo-only SVG. PNG·PDF 및 로고+텍스트 버튼용 정렬 자료는 apple/에 포함 |

미리보기: `index.html`. 공식 원본 압축파일: `originals/`.

## 공식 출처와 사용 시 참고

- [카카오 로그인 디자인 가이드](https://developers.kakao.com/docs/ko/kakaologin/design-guide) · [공식 리소스](https://developers.kakao.com/tool/resource/login). 노란색·검은색과 말풍선 형태를 유지합니다. 카카오톡 공유용 TALK 로고와 로그인용 심볼을 구분합니다.
- [네이버 로그인 가이드](https://developers.naver.com/docs/login/bi/bi.md). 현재 지정 녹색은 #03A94D입니다. 원본의 N 형태·비율·여백을 유지합니다. PNG와 AI 원본을 함께 확보했습니다.
- [Google 로그인 브랜딩 가이드](https://developers.google.com/identity/branding-guidelines). 공식 컬러 G와 제공 버튼의 크기·여백을 유지합니다. 다운로드 묶음의 Light·Dark·Neutral 및 아이콘형/텍스트형을 보존했습니다.
- [Apple 디자인 자료](https://developer.apple.com/design/resources/) · [Sign in with Apple 가이드](https://developer.apple.com/design/human-interface-guidelines/sign-in-with-apple). 공식 로고에 포함된 여백을 자르거나 로고를 다시 그리지 않습니다. 검정·흰색 버전과 원본 라이선스를 보존했습니다.

아이콘 수집은 기존 TLDS 공통 버튼의 6px radius·크기 규격을 각 브랜드에 일괄 적용했다는 뜻이 아닙니다. 실제 로그인 버튼 제작 시 각 서비스의 제공형과 여백 규칙을 기준으로 구성합니다.

## 보존·검증

공식 서버에서 받은 ZIP·AI·DMG를 originals/에 보존했습니다. 애플 DMG는 외부 실행파일을 사용하지 않고 로컬에서 압축 데이터와 파일 구조를 읽어 원본 SVG·PNG·PDF·라이선스를 추출했습니다. 파일 내용과 선택본의 SHA-256은 sources.json에 기록합니다.

선택본은 원본과 해시 일치를 확인했습니다. PNG 크기와 SVG 헤더를 확인했고 카카오·네이버 PNG의 형태를 열어 확인했습니다. 최종 사용 화면의 크기·대비·가이드 적합성 검수는 실제 배치 시 진행합니다.
