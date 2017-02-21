<template>
    <div>
        <div>{{welcomeMsg}}</div>
    </div>
</template>
<style>
    body{

    }
</style>
<script>
    export default{
        props: ['whoami'],
        computed:{
         welcomeMsg:function(){
           var self = this;
           return 'wellcome '+ self.whoami + ' to Vue全家桶!!';
         }
        }
    }
</script>
