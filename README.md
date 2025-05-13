# 📰 NewsTrust Plugin

**NewsTrust**는 사용자가 뉴스 제목을 우클릭하면 NewsAPI를 활용하여 관련 기사의 출처 수와 키워드 유사도를 분석해 **신뢰도를 %로 계산**해주는 Chrome 확장 프로그램입니다.

---

## 주요 기능

- 뉴스 제목을 우클릭하면 관련 기사들을 검색
- 다양한 출처에서 동일 주제를 다룰수록 높은 신뢰도 평가
- 신뢰도를 %로 계산하여 팝업으로 표시
- 확장 아이콘 클릭으로 플러그인 ON/OFF 전환 가능

---

## 설치 방법 (개발자 모드)

1. Chrome 브라우저 주소창에 `chrome://extensions/` 입력
2. 우측 상단 **[개발자 모드]** 활성화
3. **[압축해제된 확장 프로그램 로드]** 클릭 후 프로젝트 폴더 선택
4. 브라우저 우측 상단에 확장 아이콘이 표시되면 설치 완료

---

## 사용법

1. 확장 아이콘을 클릭하여 플러그인을 **켜짐 상태(파란색)**로 전환
2. 웹페이지에서 뉴스 제목을 **마우스로 드래그 후 우클릭**
3. "이 뉴스의 신뢰도 확인하기" 메뉴를 클릭
4. 신뢰도 결과가 팝업(alert)으로 표시됨

---

## 신뢰도 계산 공식

```
신뢰도 (%) = min(100, (관련 기사 수 / 20) × 50 + (출처 수 / 10) × 50)
```

- 20개 이상의 기사, 10개 이상의 출처에서 다룰 경우 신뢰도는 100%
- 관련 기사가 없으면 "관련 뉴스를 찾지 못했습니다" 메시지 출력

---

## 기술 스택

- JavaScript
- Chrome Extensions API (Manifest v3)
- [NewsAPI.org](https://newsapi.org)

---

## 라이선스 및 주의사항

### News API 사용 관련 주의사항
- 본 확장은 [NewsAPI.org](https://newsapi.org)의 API를 이용합니다.
- NewsAPI는 비상업적 용도로만 무료 제공되며, **웹 클라이언트에서 직접 호출은 권장되지 않습니다.**
- **API Key 노출 금지!** 반드시 `background.js`에만 저장하고 공개 저장소에 업로드하지 마세요.
- 자세한 라이선스와 이용 조건은 [NewsAPI 이용 약관](https://newsapi.org/terms)을 참고하세요.

### Chrome Web Store 정책
- 이 플러그인은 Google Chrome 확장 개발자 가이드 및 [Chrome Web Store 정책](https://developer.chrome.com/docs/webstore/program_policies/)을 준수합니다.
- 확장 아이콘, 기능 설명 등은 사용자가 오해하지 않도록 명확하게 표현되어야 합니다.

---

## 아이콘

- `icon-on.png`, `icon-off.png`: 자체 제작 아이콘

---

## Developer

- 개발자 : wooclic 
- GitHub: [https://github.com/wooclik](https://github.com/wooclik)

---

## 기여 방법

PR은 언제든 환영합니다!  
버그 제보, 기능 제안은 [Issues](https://github.com/wooclik/RealNewsPlugin/issues)에 남겨주세요.
