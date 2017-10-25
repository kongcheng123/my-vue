<template>
  <div class="p_type">
      qweqwe
  <div class="test_type">
    123
  </div>
  </div>
</template>

<script>
import {myfun} from '../../static/js/test.js' //注意路径
export default {
  name: 'test',
  data () {
    return {
        num1: 1
      };
  },
  methods: {
    handleChange(value) {
      console.log(value);
    }
  },
  created: function(){
    myfun()
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import '/static/css/test.css';
  @media only screen and (min-width: 1025px) {
    .p_type{
      float: left;
    }
  }
  @media only screen and (max-width: 1024px) {
    .p_type{
      text-align: center;
    }
  }

</style>
