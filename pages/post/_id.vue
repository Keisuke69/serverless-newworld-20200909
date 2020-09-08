<template>
  <div>
    <div id="entry_title">{{ post.title }}</div>
    <div v-html="post.content" />
  </div>
</template>

<script>
export default {
  async asyncData({ $axios, params }) {
    console.log(params.id);
    const url =
      "https://public-api.wordpress.com/rest/v1.1/sites/keisuke69.wordpress.com/posts/" +
      params.id;
    const response = await $axios.$get(url);

    return {
      post: response,
    };
  },
};
</script>

<style>
#entry_title {
  font-size: 30px;
  padding: 5px 5px 5px 5px;
}
</style>
