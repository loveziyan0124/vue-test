<template>
  <h3>属性绑定</h3>
  <div v-bind:class="dynamicClass" v-bind:id="dynamicId" v-bind:title="dynamicTitle">测试</div>
  <!-- 一次绑定多个属性 -->
  <div v-bind="objectofAttrs">多个属性</div>
  <!-- 布尔类型 -->
  <button :disabled="isButtonDisabled">Button</button>
  <!-- 简写 直接不写v-bind 写个：-->
  <div :class="dynamicClass">测试</div>
</template>
<script>
  export default {
    data(){
      return{
        dynamicClass:"appclass",
        dynamicId:"appid",
        dynamicTitle:null,
        isButtonDisabled:true,
        objectofAttrs:{
          class:"appclass",
          id:"appid"
        }
      }
    }
  }
</script>

<style>
.appclass{
  color:red;
  font-size:30px;
}
</style>

