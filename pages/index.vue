<template>
  <section class="container">
    <div>
      <h1 class="title">
        nuxt-ssr-demo
      </h1>
      <ul>
        <!-- <li><a href="/">home</a></li>
        <li><a href="/about">关于我们</a></li>
        <li><a href="/news">新闻事件</a></li> -->
        <li>
          <nuxt-link :to="{name: 'index'}">home</nuxt-link>
          <nuxt-link :to="{name: 'about'}">关于我们</nuxt-link>
          <nuxt-link :to="{name: 'news', query: {id:1}}">新闻事件</nuxt-link>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
import AppLogo from '~/components/AppLogo.vue'

export default {
  components: {
    AppLogo
  }
}
</script>

<style>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>

