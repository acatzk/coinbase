<template>
  <div id="app" class="font-sans">
    <head-bar />
  </div>
</template>

<script>
  export default {
    name: 'app',
    props: {},
    components: {
      HeadBar: () => import('@/components/Header')
    },
    data () { return {} }
  }
</script>
