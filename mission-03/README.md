# ✅ mission-03 넷플릭스 프로모션 페이지

## 1. HTML Markup
![markup](https://github.com/lanuioe/home-work/assets/148831765/7c19cb1e-224e-4c71-afa0-e2263e8b468b)

- validate 검사 완료
  <details>
  <summary>html 확인</summary>
  <div markdown="1">
  
    ```
    <div class="wrap">
        <div class="bg-wrap">
          <header class="header">
            <h1 class="logo">
              <a href="#"><img src="/images/svg/logo.svg" alt="Netflix"></a>
            </h1>
            <div class="header-btn">
              <div class="lang" role="combobox" tabindex="0" aria-expanded="false">
                <span class="selected-option">한국어</span>
                <ul class="option-container" role="listbox">
                  <li class="option ko" tabindex="0">한국어</li>
                  <li class="option en" tabindex="0">English</li>
                </ul>
              </div>
              <a href="#" class="login-btn">로그인</a>
            </div>
          </header>
          <main class="main">
            <h2 class="promotion-title">영화, TV 프로그램을 무제한으로.</h2>
            <em>다양한 디바이스에서 시청하세요. 언제든 해지하실 수 있습니다.</em>
            <p>시청할 준비가 되셨나요? 멤버십을 등록하거나 재시작하려면 이메일 주소를 입력하세요.</p>
            <form action="#" class="promotion-form">
              <label for="user-email" class="user-email-label">이메일 주소</label>
              <input type="email" class="user-email" id="user-email" required name="user-email" placeholder="yamoo9@euid.dev">
              <p class="warn-text">정확한 이메일 주소를 입력하세요.</p>
              <button type="submit" class="free-btn">30일 무료 이용</button>
            </form>
            <p>신규 회원만 이 프로모션을 이용하실 수 있습니다.</p>
          </main>
        </div>
        <footer class="footer">
          <p class="contact-info">
            <span>질문이 있으신가요?</span>
            <span>문의 전화: <a href="tel:+8203083210058">00-308-321-0058</a></span>
          </p>
          <nav class="footer-nav">
            <ul>
              <li><a href="#">자주 묻는 질문</a></li>
              <li><a href="#">고객센터</a></li>
              <li><a href="#">계정</a></li>
              <li><a href="#">미디어 센터</a></li>
              <li><a href="#">투자 정보&#40;IR&#41;</a></li>
              <li><a href="#">입사 정보</a></li>
              <li><a href="#">Netflix 지원 디바이스</a></li>
              <li><a href="#">이용 약관</a></li>
              <li><a href="#">개인정보</a></li>
              <li><a href="#">쿠키 설정</a></li>
              <li><a href="#">회사 정보</a></li>
              <li><a href="#">문의하기</a></li>
              <li><a href="#">속도 테스트</a></li>
              <li><a href="#">법적 고지</a></li>
              <li><a href="#">Netflix 오리지널</a></li>
            </ul>
          </nav>
          <div class="lang" role="combobox" tabindex="0" aria-expanded="false">
            <span class="selected-option">한국어</span>
            <ul class="option-container" role="listbox">
              <li class="option ko" tabindex="0">한국어</li>
              <li class="option en" tabindex="0">English</li>
            </ul>
          </div>
          <address class="address">
            <strong class="compnay">Netflix 대한민국</strong>
            <div class="company-details">
              <p>넷플릭스서비시스코리아 유한회사</p>
              <p>통신판매업신고번호: 제2018-서울종로-0426호</p>
              <p>전화번호: <a href="tel:+8203083210058">00-308-321-0058</a></p>
              <p>대표: 레지널드 숀 톰프슨</p>
              <p>이메일 주소: <a href="mailto:korea@netflix.com">korea@netflix.com</a></p>
              <p>주소: 대한민국 서울특별시 종로구 우정국로 26, 센트로폴리스 A동 20층 우편번호 03161</p>
              <p>사업자 등록번호: 165-87-00119</p>
              <p>클라우드 호스팅: Amazon Web Services Inc.</p>
              <p><a href="https://www.ftc.go.kr/bizCommPopView.do" target="_blank">공정거래위원회 웹사이트</a></p>
            </div>
          </address>
        </footer>
      </div>
    ```
  
  </div>
  </details>

<br />


## 2. 반응형 확인
|Mobile (max width: 768px)|Desktop (min width: 768px)|
|------|---|
|![mobile](https://github.com/lanuioe/home-work/assets/148831765/d455fc4f-7991-4851-bd67-a5ed4d222d55)|![desktop](https://github.com/lanuioe/home-work/assets/148831765/4bd51a49-d1da-4117-ba28-fe9c9ab07ff9)|

<br />

## 3. 동적 클래스 추가 결과 확인

|3-1. select|
|------|
|![select-state](https://github.com/lanuioe/home-work/assets/148831765/e36a4743-7bbc-4c09-965f-5551e28e36ae)|

|3-2. input|
|------|
|![input-state](https://github.com/lanuioe/home-work/assets/148831765/4c47c815-a435-43fa-aaff-8ca670842daf)|

<br />

## 4. 궁금한 점

- ```select```를 사용했을 때 ```option``` 스타일링에 한계가 있어서 custom을 했는데, 마크업을 어떻게 짜는 것이 좋을 지 헷갈립니다.<br />
  **```select``` 태그를 쓰지 않고 만들었을 때, ```select```와 비슷한 역할을 부여하려면** ```role```과 ```aria```를 어떻게 주어야 하는지..<br />
  눌렀을 때 동작하는 거니까 ```div```에 ```role```을 주는 것보다는 ```button```을 쓰는 것이 나을까요?
```
  <div class="lang" role="combobox" tabindex="0" aria-expanded="false">
    <span class="selected-option">한국어</span>
    <ul class="option-container" role="listbox">
      <li class="option ko" tabindex="0">한국어</li>
      <li class="option en" tabindex="0">English</li>
    </ul>
  </div>
```
