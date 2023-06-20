<template>
  <h3>模板语法</h3>
  <p>{{ msg }}</p>
  <p>{{ num + 1 }}</p>
  <p>{{ ok ? "YES" :"NO" }}</p>
  <p>{{ message.split("").reverse().join("") }}</p>
  <p>{{ rawHtml }}</p>
  <p v-html="rawHtml"></p>
</template>

<script>
export default {
  data(){
    return{
      msg:"神奇的语法",
      num:10,
      ok:true,
      message:"大家好",
      rawHtml:"<a href='https://www.baidu.com'>百度网页链接</a>"
    }
  }
}
</script>

