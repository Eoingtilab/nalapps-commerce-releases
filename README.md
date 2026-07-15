# 날라앱스 커머스 공식 배포 저장소

날라앱스 커머스 Core와 공식 애드온의 고객 설치·자동 업데이트 파일을 제공하는 공개 저장소입니다.

> 이 저장소에는 원본 소스코드, 개발용 전체 소스 ZIP, 서버 인증정보, 고객정보를 게시하지 않습니다.

## 배포 제품

- 날라앱스 커머스 Core
- 한국형 우커머스 애드온
- 위탁쇼핑몰 관리 애드온
- SMS·알림톡·이메일 애드온
- 간편 SMTP 애드온
- 팝업슬라이드 애드온

`app.nal.la` 전용 EDD 브리지는 고객 배포 대상이 아니므로 이 저장소의 공개 Release에 포함하지 않습니다.

## 저장소 역할

- GitHub Releases를 통한 설치 ZIP 배포
- Core와 애드온 버전 카탈로그 제공
- WordPress 관리자 업데이트 알림 연결
- ZIP SHA-256 무결성 정보 제공
- 버전별 릴리즈 노트와 변경이력 보존
- 긴급 롤백을 위한 이전 정식버전 자산 보존

라이선스 활성화·도메인·만료·날라앱스 커머스 Pro 권한은 `app.nal.la`의 Easy Digital Downloads가 담당합니다.

## 공개 파일 원칙

허용되는 파일:

- `nalapps-commerce-x.y.z.zip`
- `nalapps-commerce-addon-*-x.y.z.zip`
- 애드온 카탈로그 JSON
- 릴리즈 인벤토리 JSON
- SHA-256 검증파일
- 자동감사 결과
- 릴리즈 노트

금지되는 파일:

- 전체 소스 ZIP
- `.env`, API 키, 토큰, 비밀번호
- EDD 비밀키와 고객 라이선스 원문
- 고객 주문·회원·발송 데이터
- 개발 중간 산출물과 디버그 로그

## 버전과 태그

- Semantic Versioning을 사용합니다.
- Git 태그와 GitHub Release 태그는 `v1.1.0` 형식을 사용합니다.
- Core와 애드온은 독립 버전을 가질 수 있습니다.
- 카탈로그에는 각 제품의 최소 Core 버전과 WooCommerce 요구 여부를 기록합니다.

## 릴리즈 기록 원칙

모든 정식 릴리즈는 다음 정보를 반드시 포함합니다.

1. 버전과 배포일
2. 대상 제품과 파일명
3. 신규 기능, 변경, 수정, 보안 항목
4. WordPress·WooCommerce·PHP 호환 범위
5. DB 마이그레이션 여부
6. 라이선스·카탈로그·업데이트 계약 변경 여부
7. 알려진 제한사항
8. 롤백 방법
9. 각 ZIP의 SHA-256
10. 스테이징 인수시험 결과

상세 규칙은 `RELEASE_PROCESS.md`, 버전별 이력은 `CHANGELOG.md`와 `releases/` 디렉터리에서 관리합니다.

## 자동 업데이트 흐름

```text
WordPress 관리자
  → 날라앱스 커머스 Core
  → app.nal.la 카탈로그·라이선스 확인
  → GitHub Release ZIP·SHA-256 확인
  → WordPress 표준 업데이트 화면에서 설치
```

## 보안 신고

보안 취약점은 공개 Issue로 먼저 게시하지 말고 저장소 소유자에게 비공개로 전달해야 합니다. 수정과 검증이 완료된 뒤 보안 릴리즈 노트에 영향 범위와 조치사항을 기록합니다.

## 저작권

Copyright © Eoingti Lab Inc. All rights reserved.
