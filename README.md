# BlockXen_Report
## 3. 공공입찰 플랫폼 ‘나라장터’에서 특정 공고와 그 첨부자료를 수집하기 위해서는 어떻게 해야 할까요? 클릭-진입-객체탐색-클릭...으로 이어지는 인간 동작을 모사한 크롤러 로직으로 구현하는 것 외의 방법이 무엇일까요?

+ 크롤러 로직으로 구현하는 것 외의 방법으로는 Anti Captcha나 2Captcha등의 API를 사용하는 것이지만, 서비스 사용에 비용이 든다는 단점이 있습니다.

+ 인간 동작을 모사하지 않은 크롤러의 경우 크롤러임이 드러나기 때문에 차단당할 위험이 있습니다.
인간 동작을 모사하지 않는, 어려울지도 모르는 방법을 찾는 것보다는 구현이 쉬운 인간 동작을 모사하는 크롤러를 만드는 것이 더 효율적일 것으로 보이기에 크롤러 로직으로 작성하였습니다.

+ Puppeteer는 간단하지만, 크로스 브라우저와 멀티플 테스트를 지원하고 여러 기능을 지원하는 Playwright를 사용하여 코드를 작성하였습니다.
(Puppeteer, Playwright 사이트 참고 https://medium.com/front-end-weekly/playwright-vs-puppeteer-choosing-the-right-browser-automation-tool-in-2024-d46d2cbadf71)
+ 구현케이스 코드는 **`Playwright.js`** 에 있습니다.

실행 결과
https://github.com/user-attachments/assets/d978c309-3af6-44cf-838f-5cc3eebe795e
웹 크롤러를 통해 Download.zip 에 공고문들을 저장합니다.

