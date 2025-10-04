<template>
  <div>
    <h1>ewqeqeq</h1>
    <p>{{ msg }}</p>
    <div>{{ asda }}</div>
    <p>{{ number + 1 }}</p>
    <p>{{ ok ? "ok" : "not ok" }}</p>
  </div>
</template>

<!-- 	选项式API -->
<script>
export default {
  data() {
    return {
      msg: "adsadda",
      asda: "asdadsad",
      number: 10,
      ok: true,
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

<style scoped></style>
