<template>
  <nuxt-content :document="doc"  />
</template>

<script>
export default {
  name: 'PagesSlug',
  async asyncData({$content, params}) {
    const doc = await $content('articles/' + params.slug || 'index').fetch();
    return {doc};
  }
}
</script>
