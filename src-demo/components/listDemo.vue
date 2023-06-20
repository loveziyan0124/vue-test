<template>
    <h3>列表渲染</h3>
    <!-- v-for -->
    <P v-for="item in names">{{ item }}</P>
    <hr>
    <P v-for="item of names">{{ item }}</P>
    <hr>
    <P v-for="name in names">{{ name }}</P>
    <hr>
    <!-- 复杂的数据 -->
    <div v-for="item in result">
        <p>{{ item.title }}</p>
        <img :src="item.avator" alt="">
    </div>
    <hr>
    <!-- 显示下标 -->
    <p v-for="(item,index) in names">{{ item }}- {{ index }}</p>
    <hr>
    <!-- 显示一个对象的全部信息 -->
    <div>
        <p v-for="item of userInfo">{{ item }}</p>
        <p v-for="(value, key, index) of userInfo">{{ value }}-{{ key }}-{{ index }}</p>

    </div>
</template>
<script>



export default {
    data(){
        return{
            names:["HTML","CSS","JAVASRIPT"],
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
            ],
            userInfo:{
                    name:"rose",
                    age:10,
                    height:150
                }
        }
    }
}
</script>