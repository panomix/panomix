# ADK 설치 및 적용 가이드

저희 **Panomix ADK**는 언론사 웹사이트의 기사 **본문(body)** 내에서 독립적으로 작동하는 레이어입니다.

따라서 **홈페이지 메인, 기사 목록 페이지 등이 아닌**, 반드시 **기사 페이지의 본문 영역**에만 스크립트를 삽입해야 합니다.

---

### ADK 설치 스크립트

아래 스크립트 기사 본문 템플릿의 `<article>` 또는 `<div class="article-body">` 내에 추가하세요.

```html
<script
  src="https://aisdk-js-fgaaagggamgjdsgm.z02.azurefd.net/scripts/adk/embed.min.js"
  data-wsid="이곳에 워크스페이스 ID가 들어갑니다"
  async
></script>
```

| 속성 | 설명 |
| --- | --- |
| `src` | SDK 스크립트 파일 경로 (고정) |
| `data-wsid` | 발급받은 워크스페이스 ID — 각 언론사별로 이메일을 통해 개별 제공 |
| `async` | 비동기 로드 방식으로, 페이지 렌더링에 영향을 주지 않음 |

---
### 📍 스크립트 삽입 위치 예시

```html
<article class="article-body">
  <p>이곳에 기사 본문 내용이 들어갑니다.</p>
  <p>...</p>

  <!-- ADK 스크립트 삽입 -->
  <script
    src="https://aisdk-js-fgaaagggamgjdsgm.z02.azurefd.net/scripts/adk/embed.min.js"
    data-wsid="이곳에 워크스페이스 ID가 들어갑니다"
    async
  ></script>
</article>
```

---

### ⚠️ 주의사항

- 위 스크립트를 홈(메인) 페이지나 기사 목록 페이지에는 삽입하지 마세요. ADK는 기사 본문 영역(body) 내에서만 작동하는 레이어입니다.  

- 발급받은 `data-wsid` 값(워크스페이스 ID)은 외부에 **절대 공유하지 마세요.**  
  이 값이 제3자에게 공유되거나 노출될 경우 **여러 보안 문제가 발생할 수 있습니다.**  문제가 발생할 경우 ADK 사용이 **일시 중단될 수 있으니**, 반드시 내부 담당자만 접근하도록 관리해 주세요.  

- `async` 로 스크립트를 비동기로 로드하므로, 별도 로딩 최적화 작업은 필요하지 않습니다.

---
## **문의하기** ##

관련 질문이나 궁금한 점, 또는 스크립트 작동에 문제가 있을 경우 info@panomix.io 로 문의해 주세요. 신속하게 확인 후 안내해 드리겠습니다.

