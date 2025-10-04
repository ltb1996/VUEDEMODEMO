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

<style scoped>
</style>
