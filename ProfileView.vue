<template>
  <div class="profile-container">
    <h2>个人中心</h2>
    <div>
      <img src="@/assets/logo.png" alt="个人头像" class="avatar" />
      <p>用户名: {{ username }}</p>
      <router-link to="/change-password">修改密码</router-link>
      <router-link to="/my-orders">我的订单</router-link>
      <!-- 新增: 跳转到购物车的链接 -->
      <router-link to="/shopcart">购物车</router-link>
      <!-- 新增: 跳转到商品列表的链接 -->
      <router-link to="/goods-list">商品列表</router-link>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      username: '郭哲漩' // 这里可以替换为从后端获取的实际用户名
    };
  }
};
</script>

<style scoped>
.profile-container {
  max-width: 300px;
  margin: 0 auto;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 5px;
  background-color: #fff;
}

.avatar {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  margin-bottom: 20px;
}

a {
  display: block;
  margin-bottom: 10px;
  color: #42b983;
  text-decoration: none;
}

a:hover {
  color: #348868;
}
</style>