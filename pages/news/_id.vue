<template>
  <div>
      <h2>News-Content: {{$route.params.id}}</h2>
      <p>新闻详情页</p>
      <ul>
        <li><a href="/">Home</a></li>
      </ul>
  </div>
</template>

<script>
export default {
  validate({ params }) {
    return /^\d+$/.test(params.id)
  },
  data() {
    return {
      title: this.$route.params.title
    }
  },
  // 设置独立的 head
  head() {
    return {
      title: this.title,
      meta: [
        {
          hid: 'description',
          name: 'news',
          content: 'this is content'
        }
      ]
    }
  }
}
</script>