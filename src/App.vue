<template>
  <div class="container">
    <h1>{{ message }}</h1>
    <button @click="generateMessage">產生一句話</button>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      message: '點擊按鈕產生一句話！',
      quotes: [
        '學海無涯，回頭是岸。',
        '機會是留給準備好的人。',
        '每天進步一點點。',
        '不怕慢，只怕站。',
        '失敗為成功母。'
      ]
    }
  },
  methods: {
    generateMessage() {
      const randomIndex = Math.floor(Math.random() * this.quotes.length);
      this.message = this.quotes[randomIndex];
    }
  }
}
</script>

<style>
.container {
  text-align: center;
  margin-top: 100px;
  font-family: Arial, sans-serif;
}

button {
  margin-top: 20px;
  padding: 10px 20px;
  font-size: 18px;
  cursor: pointer;
}
</style>
