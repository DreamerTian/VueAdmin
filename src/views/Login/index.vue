<template>
    <div id="login">
        <div class="login-wrap">
            <ul class="menu-tab">
                <li v-for="item in menuTab" :key="item.id" @click="currentTab(item)" :class="{'current' : item.current}">{{item.name}}</li>
            </ul>
        </div>
    </div>
</template>
<script>
export default {
    name: "Login",
    data(){
        return{
            menuTab:[
                {'name':'登录','current':true},
                {'name':'注册','current':false},
            ]
        }
    },
    created() {
    },
    mounted() {
    },
    methods:{
        currentTab(item){
            this.menuTab.forEach(ele=>{
                ele.current = false
            })
            item.current = true
        }
    }
}
</script>
<style lang="scss" scoped>
    #login{

    }
    .login-wrap{
        width: 300px;
        margin: auto;
    }
    .menu-tab{
        text-align: center;
        li{
            display: inline-block;
            width: 88px;
            line-height: 36px;
            color: #f7f7f7;
            background-color: aqua;
            border-radius: 4px;
            cursor:pointer;
        }
        li:last-child{
            margin-left: 2px;
        }
        .current{
            background-color: blue;
        }
    }
</style>

