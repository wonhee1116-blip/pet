# PetBridge MVP 프로토타입

## 파일 구조

```
PetBridge/
├── home.html              # 홈 화면
├── diagnosis.html         # 문제행동 진단 (2단계)
├── video-upload.html      # 영상 업로드
├── diagnosis-result.html  # 진단 결과
├── request.html           # 훈련 의뢰 등록
├── bid-list.html          # 받은 견적 목록
├── bid-compare.html       # 견적 비교
├── trainer-select.html    # 훈련사 선택 완료
└── README.md
```

## 실행 방법

### 방법 1 — VS Code Live Server (권장)
1. VS Code에서 폴더 열기
2. `home.html` 우클릭 → **Open with Live Server**
3. 브라우저에서 자동 실행

### 방법 2 — 브라우저에서 직접 열기
1. `home.html` 파일을 Chrome/Safari에서 더블클릭
2. 페이지 이동 링크로 전체 플로우 탐색 가능

## 화면 흐름

```
home.html
  └─ diagnosis.html          반려견 정보 입력 + 문제행동 선택
       └─ video-upload.html  영상 업로드 (선택사항)
            └─ diagnosis-result.html  진단 결과 + 심각도 점수 + 추천 훈련
                 └─ request.html      훈련 의뢰 등록
                      └─ bid-list.html       받은 견적 (정렬·비교·채팅)
                           ├─ bid-compare.html    선택 훈련사 2인 비교
                           └─ trainer-select.html 선택 완료 + 채팅 시작
```

## 디자인 시스템

| 항목 | 값 |
|------|-----|
| Primary | `#FF7A00` |
| Secondary | `#FF9A3D` |
| Background | `#F8FAFC` |
| Text | `#111827` |
| Font | Pretendard (CDN) |
| 화면 기준 | 390px (iPhone 기준) |

## 참고 사항
- 모든 CSS/JS가 각 HTML 내부에 포함되어 있어 파일 하나만 열어도 동작합니다
- 페이지 간 데이터는 `localStorage`로 전달됩니다
- 별도 서버·빌드 도구 불필요
