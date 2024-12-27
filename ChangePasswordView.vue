<template>
  <div class="change-password-container">
    <h2>修改密码</h2>
    <form @submit.prevent="handleSubmit">
      <div>
        <label for="currentPassword">当前密码：</label>
        <input type="password" id="currentPassword" v-model="currentPassword" required />
      </div>
      <div>
        <label for="newPassword">新密码：</label>
        <input type="password" id="newPassword" v-model="newPassword" required />
      </div>
      <div>
        <label for="confirmNewPassword">确认新密码：</label>
        <input type="password" id="confirmNewPassword" v-model="confirmNewPassword" required />
      </div>
      <button type="submit">修改密码</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      currentPassword: '',
      newPassword: '',
      confirmNewPassword: ''
    };
  },
  methods: {
    handleSubmit() {
      // 处理修改密码逻辑
      if (this.newPassword !== this.confirmNewPassword) {
        alert('新密码和确认新密码不一致');
        return;
      }
      console.log('Change password submitted:', this.currentPassword, this.newPassword);
    }
  }
};
</script>

<style scoped>
.change-password-container {
  max-width: 300px;
  margin: 0 auto;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 5px;
  background-color: #fff;
}

form div {
  margin-bottom: 15px;
}

label {
  display: block;
  margin-bottom: 5px;
}

input {
  width: 100%;
  padding: 8px;
  box-sizing: border-box;
}

button {
  width: 100%;
  padding: 10px;
  background-color: #42b983;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  background-color: #348868;
}
</style>