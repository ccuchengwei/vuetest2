<template>
<button :disabled="disabled" @click="disableButton">{{title}}</button>
</template>

<script>
  export default {
    name: 'BaseButton',
    props: {
       
        title : String
    },
    data() {
     return {
        disabled:false
      }
    },
    methods: {
        disableButton: function(){
            this.disabled = true
        }
    }
    
  }
</script>