<template>
  <li>{{ name }}?!</li>
</template>

<script>
export default {   
  props: {
    name: {     // type이 String인 name이라는 데이터를 받는다.(데이터가 들어오지 않으면 default로 ''를 사용하겠다.)
      type: String,
      default:  ''
    }
  }

}
</script>

<style scoped lang="scss">
/* scoped : style태그는 다른 component는 영향을 미치지 않음. -> 유효범위 : 현재의 component */
  h1 {
    color:  red !important;
  }
</style>
