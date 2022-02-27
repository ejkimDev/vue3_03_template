<template>
  <h1>{{ count }}</h1>
</template>

<script>
export default {
  data() {
    return {
      count: 2
    }
  },
  /*
  * 라이프사이클 (작성 순서는 상관X)
  * beforeCreate : 컴포넌트가 생성되기 직전에 실행, 활용도가 적다.
  * created : App.vue라는 컴포넌트를 초기화하는 과정에서 컴포넌트가 생성된 직후에 실행
  * beforeMount : 컴포넌트가 HTML 구조에 연결되기 전
  * mounted : 컴포넌트가 HTML 구조에 연결된 후. 화면에 컴포넌트가 출력된 후 실행
   */
  beforeCreate() {
    console.log('beforeCreate', this.count);
  },
  created() {   
    console.log('Created', this.count);
  },
  beforeMount() {
    console.log('beforeMount');
    console.log(document.querySelector('h1'));
  },
  mounted() {
    console.log('Mounted');
    console.log(document.querySelector('h1'));
  }
}
</script>
