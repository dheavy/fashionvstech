<template>
  <nuxt-content :document="doc" />
</template>

<script>
export default {
  name: 'PageSlug',
  async asyncData({$content, params}) {
    const doc = await $content(params.slug || 'index').fetch();
    return {doc};
  }
}
</script>
