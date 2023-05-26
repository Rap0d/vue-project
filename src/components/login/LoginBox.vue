<template>
  <div class="login-box">
    <div class="login-title">
      <img src="@/assets/images/maxy-BI-WH.svg" alt="maxy-bi" />
    </div>
    <div class="welcome-txt">MAXY를 통한 모바일 모니터링을 시작합니다.</div>
    <input id="userId" type="text" required placeholder="ID" />
    <input id="userPw" type="password" required placeholder="Password" />
    <span class="err-txt"></span>
    <button class="find-pw popup-op" data-op="find-pw-popup" id="btnOpenFindPwModal">
      비밀번호 찾기
    </button>
    <button id="btnLogin" type="submit" class="login-btn">LOGIN</button>
  </div>
</template>

<style lang="scss" scoped>
@import '@/assets/scss/common';

.login-box {
  width: 400px;
  position: absolute;
  top: calc(50% - 250px);
  left: calc(50% - 200px);

  background-color: white;
  padding: 3.125em;
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  align-items: center;
  box-shadow: 5px 5px 15px -1px rgba(0, 0, 0, 0.75);

  .login-title {
    position: relative;
    display: inline-flex;
    align-items: center;
    margin-bottom: 1em;

    img {
      height: 40px;
      display: inline-block;
    }
  }

  .welcome-txt {
    color: $color-sub-text;
    margin: 8px 0 3em;
  }

  input {
    width: 100%;
    margin-bottom: 1.25em;
    height: 40px;
    border-radius: 5px;
    border: 1px solid gray;
    padding: 0.8em;
    font-family: 'Inter', sans-serif;
    outline: none;

    &:focus {
      border: 1px solid $color-logo-purple-2;
      outline: none;
    }
  }

  .find-pw {
    min-width: 75px;
    margin-left: auto;
    background-color: transparent;
    border: 0;
    color: $color-sub-text;
    margin-bottom: 1.25em;

    &:hover {
      text-decoration-line: underline;
    }
  }

  .login-btn {
    width: 50%;
    padding: 0.625em;
    border-radius: 5px;
    color: white;
    background-color: $color-logo-purple-2;
    border: 1px dashed $color-logo-purple-2;
    cursor: pointer;

    &:hover {
      color: $color-logo-purple-2;
      background-color: white;
      border: 1px dashed $color-logo-purple-2;
      cursor: pointer;
      transition: 0.5s;
    }
  }

  .warning-txt {
    color: $color-sub-text;
    display: inline-block;
    position: absolute;
    bottom: 32px;
    width: 100%;
    text-align: center;
    font-size: $font-s-size;
    line-height: 16px;
  }

  .err-txt {
    display: none;
    padding-left: 0;
    text-align: left;
    width: 100%;
  }
}
</style>
