<template>
  <div class="main_type">
    <div class="test">
      {{ message }}<br>
      <input v-model="message"/>
    </div>
    <button v-on:click="reverseMessage">逆转消息</button>
    <hr/>
    <span :title="message">
      哈哈
    </span>
    <hr/>
    <p v-if="seen">
      jjj
    </p>
    <Test></Test>
    <HelloWorld></HelloWorld>
  </div>
</template>

<script>
import Test from './test'
import HelloWorld from './HelloWorld'
export default {
  name: "index",
  components:{
    Test,
    HelloWorld
  },
  data() {
    return {
      message: 'Hello Vue.js!',
      seen:true
    };
  },
  methods: {
    handleChange(value) {
      console.log(value);
    },
    reverseMessage(){
      this.message = this.message.split('').reverse().join('')
    }
  },
  created: function(){
    console.log('message is '+this.message)
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  @media only screen and (min-width: 1025px) {
    .main_type{
      text-align: center;
    }
  }
  @media only screen and (max-width: 1024px) {
    .main_type{
      float: left;
    }
  }
</style>
