//my.vue
<template>
    <div>
        <div class='my-hide'>
            <div class='my-logo'></div>
            <span class='my-name'>summerpen</span>
        </div>
        <div class='my-detail'>
            github：<a href='https://github.com/summerpen/'>https://github.com/summerpen/</a><br><br>
        </div>
    </div>
</template>
<script>
export default {
  name: 'my',
  components:{
    
  },
  created(){
    //用vuex设置状态，改变class;
     this.$store.dispatch("inMy");
  }
}
</script>
<style lang='less'>
    .my-hide{
        width:100%;
        height:180px;
        background:url("./../assets/images/bg1.png") no-repeat;
        background-size:cover;
        position:relative;
        .my-logo{
            width:80px;
            height:80px;
            background:url("./../assets/images/logo.jpg") no-repeat;
            background-size:100%;
            border-radius:50%;
            position:absolute;
            top:60px;
            left:0;
            right:0;
            margin:0 auto;
        }
        .my-name{
            position:absolute;
            bottom:10px;
            color:#fff;
            left:0;
            right:0;
            margin:0 auto;
            display:block;
            text-align:center;
        }
    }
    .my-detail{
            margin:10px 10px;
        }
</style>