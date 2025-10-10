<template>
  <div class="mobanyufa">
    <H3>模板语法</H3>
    <h1>ewqeqeq</h1>
    <p>{{ msg }}</p>
    <div>{{ asda }}</div>
    <p>{{ number + 1 }}</p>
    <p>{{ ok ? "ok" : "not ok" }}</p>
    <!-- <p>{{ var a = 10 }}</p> -->
    <p>{{ msg.split('').reverse().join("") }}</p>
    <p>{{ rawHtml }}</p>
    <p v-html="rawHtml"></p>
    <hr>
  </div>
</template>

<!-- 	选项式API -->
<script>
export default {
  name: '1mobanyufa',
  data() {
    return {
      msg: "abcde",
      asda: "asdadsad",
      number: 10,
      ok: true,
      rawHtml: "<a href='https://www.baidu.com'>百度百度</a>"
    }
  }
}
</script>

<!-- 组合式api -->
<!-- <script setup>
import { ref } from 'vue';

const msg = ref("adsadda");
const asda = ref("asdadsad");
const number = ref(1022222222222222);
const ok = ref(true);
</script> -->

<style scoped>
.mobanyufa {
  color: green;
}
</style>
