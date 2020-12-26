<template>
  <div id="app">
    <header />
  </div>
</template>

<script>
  export default {
    name: 'app',
    props: {},
    components: {
      Header: () => import('@/components/Header')
    },
    data () { return {} }
  }
</script>
