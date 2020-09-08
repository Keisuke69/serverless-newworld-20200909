<template>
  <div>
    <div v-html="post.content" />
  </div>
</template>

<script>
export default {
  async asyncData({ $axios,params}) {
  console.log(params.id);
    const url =
      "https://public-api.wordpress.com/rest/v1.1/sites/keisuke69.wordpress.com/posts/"+ params.id;
    const response = await $axios.$get(url);

    return {
      post: response,
    };
  },
};
</script>
