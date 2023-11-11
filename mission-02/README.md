# ✅ mission-02 이디야 로그인 페이지

## 1. HTML Markup
![markup](https://github.com/lanuioe/home-work/assets/148831765/650e4f94-79c8-4c7a-95c1-65b9bdc4510b)

<br />

## 2. 동적 클래스 추가 결과 확인

![validation1](https://github.com/lanuioe/home-work/assets/148831765/c10e759d-7a0d-4d26-a977-f77a8aeb3792)

- <strong>input이 focus되었을 때, is-focus 클래스를 추가</strong><br />
→ label이 위로 올라가며 input의 placeholder가 보임

  <details>
  <summary>css 확인</summary>
  <div markdown="1">
  
    ```
    .login-container .is-focus {
      top: 0px;
      left: 0;
      font-size: 1.3rem;
      transition: all 0.3s;
    }
    ```
  
  </div>
  </details>

<br />

![validation2](https://github.com/lanuioe/home-work/assets/148831765/1b29045a-2f09-45f5-8fcd-d5cb5ba6fc90)

- <strong>input이 올바르게 작성되지 않았을 때, is-invalid 클래스를 추가</strong><br />
→ 유효성 검사 warning 아이콘 표시 (email, password 동일)<br />
→ 경고 텍스트 표시

- <strong>input이 올바르게 작성되었을 때, is-valid 클래스를 추가</strong><br />
→ 유효성 검사 check 아이콘 표시 (email, password 동일)

<br />

- <strong>input password에 작성을 시작했을 때, is-invisible 클래스를 추가</strong><br />
→ 비밀번호 보기(눈 뜬 모양) 아이콘 활성화: 작성시 기본으로 비밀번호가 보이지 않음

- <strong>눈 모양 아이콘을 클릭했을 때, is-invisible 클래스를 추가</strong><br />
→ 작성 중인 비밀번호가 보이며,<br />
비밀번호 보지 않기(눈 감고 있는 모양) 아이콘 활성화: 다시 클릭할 경우 비밀번호가 보이지 않음(토글)

  <details>
  <summary>유효성 검사 css 확인</summary>
  <div markdown="1">
  
  - 유효성 아이콘 공통 클래스 (위치 지정)
    ```
    .validation {
      display: inline-block;
      position: absolute;
      bottom: 5px;
      right: 8px;
      width: 16px;
      height: 16px;
      border: 0;
      background: transparent;
    }
    
    .is-valid ~ .validation.eye-icon,
    .is-invalid ~ .validation.eye-icon {
      right: 33px;
    }
    ```
  
  
  - 동적 클래스 추가에 따라 이미지 변경
    ```
    .is-valid ~ .validation.valid-icon {
      background: url("../images/icon-valid-check.svg") 0 0 / cover;
    }
    
    .is-visible ~ .validation.eye-icon {
      background: url("../images/icon-pwd-eye.svg") 16px 0 / cover;
    }
    
    .is-invisible ~ .validation.eye-icon {
      background: url("../images/icon-pwd-eye.svg") 0 0 / cover;
    }
    
    .is-invalid ~ .validation.valid-icon {
      background: url("../images/icon-valid-check.svg") 16px 0 / cover;
    }
    ```

  - is-invalid일 경우 제공되는 텍스트
    ```
    .warn-text {
      display: none;
      position: absolute;
      margin-left: 8px;
      top: 50px;
      font-size: 1.2rem;
    }
    
    .is-invalid ~ .warn-text {
      display: block;
    }
    ```

  </div>
  </details>

<br />

- <strong>로그인 폼 유효성 검사가 모두 올바를 경우, 로그인 버튼에 is-valid 클래스를 추가</strong><br />
→ 로그인 버튼 활성화
  
  <details>
  <summary>css 확인</summary>
  <div markdown="1">
  
    ```
    .sign-in-container.is-valid {
      color: var(--color-primary-blue);
    
      & .sign-in {
        opacity: 1;
      }
    }
    ```
  
  </div>
  </details>


<br />

## 3. 반응형 확인
|Mobile (max width: 600px)|Desktop (min width: 600px)|
|------|---|
|![ediya-mobile](https://github.com/lanuioe/home-work/assets/148831765/ce575601-40af-4124-973c-be521baaf111)|![ediya-desktop](https://github.com/lanuioe/home-work/assets/148831765/98eff127-30e9-4e83-99cb-a7dddbf37702)|

  <details>
  <summary>css 확인</summary>
  <div markdown="1">

  - 미디어 쿼리 사용
    ```
    @media (min-width: 600px) {
    .  login-container {
        padding-top: 145px;
        width: 540px;
      }
  
      .sign-container {
        margin-top: 60px;
        flex-direction: row;
        justify-content: space-between;
        column-gap: 20px; 
      }
      
      .sign-in-container, .sign-up-container {
        flex-grow: 1;
      }
    ```
  
  </div>
  </details>
