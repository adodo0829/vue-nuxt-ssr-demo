<template>
  <div>
    <h2>新闻的主页</h2>
    <p>NewsID:{{$route.query.id}}</p>
    <nuxt-link :to="{name: 'index'}">home</nuxt-link>
    <button @click="getValue">get a value</button>
    <hr>
    <ul>
      <li><nuxt-link :to="{name: 'news-id', params: {id: 123, title: 'huhua 的 blog'}}">new 1111</nuxt-link></li>
      <li><nuxt-link :to="{name: 'news-id', params: {id: 456, title: 'huhua 的 blog'}}">new 2222</nuxt-link></li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      ids: 1111
    }
  },
  methods: {
    getValue() {
      console.log(1111, this.$route.params.id);
    }
  },
}
</script>