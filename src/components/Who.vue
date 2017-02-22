<template>
  <div>
    <div>{{welcomeMsg}}</div>
    <div>{{feedbackListUrl}}</div>
  </div>
</template>
<style>
    body{

    }
</style>
<script>
    export default{
        data(){
          return {
            feedbackListUrl: "??"+FEEDBACK_LIST+" ??"
          }
        },
        props: ['whoami'],
        computed:{
         welcomeMsg:function(){
           var self = this;
           return 'wellcome '+ self.whoami + ' to Vue全家桶!!';
         }
        }
    }
</script>
