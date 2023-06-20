<template>
    <h3>key属性添加到v-for中</h3>
    <P v-for="(item,index) of names" :key="index">{{ item }}</P>
    <div v-for="item of result" :key="item.id">
        <p>{{ item.title }}</p>
        <img :src="item.avator" alt="">
    </div>
</template>
<script>

export default {
    data(){
        return{
            names:["HTML","CSS","JAVASCRIPT"],
            result:[
                {
                    "id":22654351,
                    "title":"许昌 | 感受一座城市的璀璨夜景",
                    "avator":"https://pic.q"
                },
                {
                    "id":22658921,
                    "title":"郑州 | 感受一座城市的璀璨夜景",
                    "avator":"https://pic.q"
                },
                {
                    "id":22653451,
                    "title":"开封 | 感受一座城市的璀璨夜景",
                    "avator":"https://pic.q"
                },
            ]
        }
    }
}


</script>