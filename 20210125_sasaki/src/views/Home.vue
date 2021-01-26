<template>
  <div class="home">
    <div class="input-code">
      <label>郵便番号を入力(ハイフンなし)</label>
      <input type="text" v-model="code" placeholder="1234567" />
      <button @click="getCode">住所検索</button>
    </div>
    <div class="result-address">
      <p>住所：{{ resultData }}</p>
    </div>
  </div>
</template>

<script>
import axios from "axios"
export default {
  data() {
    return {
      code: "",
      resultData: ""
    };
  },
  methods: {
    getCode() {
      axios.get(`https://apis.postcode-jp.com/api/v4/postcodes/${this.code}?fields=allAddress&apiKey=6Q2P3Um7HhU5rzhOCIhB6YxpBtiDQlROFME12mh`)
      .then((res) => (this.resultData = res.data[0].allAddress))
    }
  },
};
</script>