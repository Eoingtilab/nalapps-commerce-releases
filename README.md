# 날라앱스 공식 통합 배포 저장소

날라앱스의 WordPress 플러그인, 커머스 애드온, 데스크톱 유틸리티와 향후 소프트웨어 제품의 고객 설치·자동 업데이트 파일을 제공하는 통합 공개 배포 저장소입니다.

> 이 저장소에는 원본 소스코드, 개발용 전체 소스 ZIP, 서버 인증정보, 고객정보를 게시하지 않습니다.

## 배포 제품군

- 날라앱스 커머스 Core 및 공식 애드온
- 독립 WordPress 플러그인
- Windows 유틸리티와 데스크톱 앱
- 향후 macOS·모바일·자동화 도구
- 교육·업무용 날라앱스 소프트웨어

`app.nal.la` 전용 EDD 브리지와 라이선스 서버 코드는 고객 배포 대상이 아니므로 공개 Release에 포함하지 않습니다.

## 저장소 역할

- GitHub Releases를 통한 설치 ZIP·EXE·MSI 등 배포
- 모든 제품의 독립 버전 카탈로그 제공
- WordPress 및 데스크톱 앱 자동 업데이트 연결
- 배포 자산별 SHA-256 무결성 정보 제공
- 제품별 릴리즈 노트와 변경이력 보존
- 긴급 롤백을 위한 이전 정식버전 자산 보존

라이선스 활성화, 도메인·기기, 만료, 무료 시리얼, 유료 권한과 Pro 권한은 `app.nal.la`의 Easy Digital Downloads 및 라이선스 계층이 담당합니다.

## 제품 식별자와 태그

모든 제품은 변경되지 않는 `product_id`를 사용합니다.

예시:

- `nalapps-commerce-core`
- `nalapps-commerce-vendorops`
- `nalapps-wp-messages`
- `nalapps-wp-easy-smtp`
- `nalapps-wp-popup-slider`
- `nalapps-file`
- `nalapps-calendar`

제품별 버전 주기가 다르므로 태그에는 제품 식별자를 포함합니다.

예시:

- `commerce-core-v1.0.0`
- `commerce-vendorops-v1.0.0`
- `wp-messages-v1.0.0`
- `utility-file-v1.0.0`

## 공개 파일 원칙

허용되는 파일:

- WordPress 플러그인 ZIP
- Windows EXE·MSI
- macOS DMG·PKG
- 제품별 또는 통합 `manifest.json`
- 릴리즈 인벤토리 JSON
- SHA-256 검증파일
- 자동감사 결과
- 릴리즈 노트

금지되는 파일:

- 전체 원본 소스 ZIP
- `.env`, API 키, 토큰, 비밀번호
- EDD 비밀키와 고객 라이선스 원문
- 고객 주문·회원·발송 데이터
- 개발 중간 산출물과 디버그 로그

## 버전과 릴리즈 기록

- Semantic Versioning을 사용합니다.
- 각 제품은 독립 버전을 가집니다.
- 모든 정식 릴리즈에는 제품 ID, 버전, 배포일, 자산명, 호환 범위, 변경사항, 알려진 제한, 롤백 방법, SHA-256과 인수시험 결과를 기록합니다.
- 플러그인 헤더·내부 상수·EDD Versions·배포 자산의 버전을 일치시킵니다.

## 자동 업데이트 흐름

```text
제품별 비공개 개발 저장소
  → 테스트·빌드·서명·해시 생성
  → Eoingtilab/nalapps-releases 제품별 GitHub Release
  → app.nal.la 라이선스·제품 카탈로그 확인
  → 고객 WordPress 또는 데스크톱 앱에서 다운로드·검증·업데이트
```

## 보안 신고

보안 취약점은 공개 Issue로 먼저 게시하지 말고 저장소 소유자에게 비공개로 전달해야 합니다. 수정과 검증이 완료된 뒤 보안 릴리즈 노트에 영향 범위와 조치사항을 기록합니다.

## 저작권

Copyright © Eoingti Lab Inc. All rights reserved.