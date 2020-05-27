<template>
  <nuxt-content :document="doc" />
</template>

<script>
export default {
  name: 'PagesSlug',
  async asyncData({$content, params}) {
    console.log(params);
    const doc = await $content(params.slug || 'index').fetch();
    return {doc};
  }
}
</script>
