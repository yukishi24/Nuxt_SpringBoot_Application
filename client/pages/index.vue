<template>
  <span>{{get_result}}</span>
</template>

<script>
export default {
  name: 'IndexPage',
  async asyncData({$axios}) {
    const url = "http://localhost:8080/"; //接続URL
    const responce = await $axios.$get(url); //GET
    return{
      get_result: responce
    };
  },
}
</script>
