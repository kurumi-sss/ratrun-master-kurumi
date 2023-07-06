<template>
  <div class="registration">
    <h1>新規会員登録</h1>
    <form>
      <div class="forms">
        <BasicInput
          text="メールアドレス"
          type="email"
          placeholder="メールアドレス"
        />
      </div>
      <div class="forms">
        <BasicInput
          text="パスワード"
          type="password"
          placeholder="パスワード"
        />
      </div>
      <div class="button">
        <BasicButton @clickSubmit="clickButton" />
      </div>
    </form>
  </div>
</template>
  
  <script>
import { BasicInput } from "../components/Atoms/Inputs";
import { BasicButton } from "../components/Atoms/Buttons";

export default {
  components: { BasicInput, BasicButton },
  setup() {
    const clickButton = () => {
      console.log("ボタンを押しました");
    };
    return { clickButton };
  },
};
</script>
  
<style lang="scss">
form {
  padding: 20px;
  .forms {
    margin: 20px 0;
  }
}

.button {
  text-align: center;
}
</style>