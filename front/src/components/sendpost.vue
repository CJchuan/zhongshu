<template>
    <div class="sendpost">
      <div class="header2">
            <i class="iconfont" @click="gob">&#xe647;</i>
            <h2>发表帖子</h2>
      </div>
      <Writecont></Writecont>
      <mt-button type="primary" @click="sendpost">发表</mt-button>
    </div>
</template>

<script>
import Writecont from "./Writecont.vue";
    export default {
        name:'sendpost',
        data(){
            return{

            }
        },
        components:{
                Writecont
        },
        methods:{
          sendpost(){
            this.$http.get("http://10.2.158.246:3000/posts/write",{userId:1,username:"yzx",word:"今天天气好！",}).then(res=>{

            })
          },
          gob(){
             this.goback();
          }
        }
    }
</script>

<style scoped>

</style>