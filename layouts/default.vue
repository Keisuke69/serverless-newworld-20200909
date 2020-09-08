<template>
  <div>
    <header id="blog-title">
      <NuxtLink to="/"><h1 id="title">新時代のサーバーレスブログ</h1></NuxtLink>
    </header>
    <hr />
    <Nuxt />
  </div>
</template>

<style>
#blog-title {
  height: 120px;
}

#title {
  font-size: 44px;
}
</style>
