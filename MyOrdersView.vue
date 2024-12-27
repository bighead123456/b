<template>
  <div class="my-orders-container">
    <h2>我的订单</h2>
    <ul>
      <li v-for="(order, index) in orders" :key="index">
        订单号: {{ order.id }} - 金额: {{ order.amount }} - 状态: {{ order.status }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      orders: [
        { id: '1', amount: '100.00', status: '已完成' },
        { id: '2', amount: '200.00', status: '待支付' }
      ]
    };
  }
};
</script>

<style scoped>
.my-orders-container {
  max-width: 300px;
  margin: 0 auto;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 5px;
  background-color: #fff;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  margin-bottom: 10px;
  padding: 10px;
  border: 1px solid #ddd;
  border-radius: 5px;
}
</style>