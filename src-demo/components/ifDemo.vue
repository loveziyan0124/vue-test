<template>
    <h3>条件渲染</h3>
    <!-- v-if 是的判断 有较高的切换开销，在最初为假不会被渲染-->
    <div v-if="flag">flag为真，你能看见我</div>
    <!-- v-else 否则判断 -->
    <div v-else="flag">flag为假，那你看不见我</div>
    <!-- v-else-if 多个判断-->
    <div v-if="type === 'A'">选项A</div>
    <div v-else-if="type === 'B'">选项B</div>
    <div v-else-if="type === 'C'">选项C</div>
    <div v-else="type === 'D'">非A/B/C</div>
    <!-- v-show 是的判断 有较高的初始开销，在最初无论真假都会被渲染 -->
    <div v-show="flag">flag为真，你能看见我</div>
</template>
<script>
export default{
    data(){
        return{
            flag:false,
            type:"D"
        }
    }
}
</script>