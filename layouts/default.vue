<template>
  <div class="container">
    <div class="navigation">
      <nuxt-link to="/category">
        Category Page
      </nuxt-link> |
      <nuxt-link to="/category">
        Product Page
      </nuxt-link>
    </div>
    <div class="page">
      <nuxt />
    </div>
  </div>
</template>

<style>
html {
  font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Roboto, 'Helvetica Neue', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

.container {
  margin: 0 auto;
  max-width: 1080px;
}

.navigation {
  margin-bottom: 20px;
}
</style>
