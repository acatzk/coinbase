<template>
  <div id="app">
    <nav-bar />
  </div>
</template>

<script>
  export default {
    name: 'app',
    props: {},
    components: {
      NavBar: () => import('@/components/NavBar')
    },
    data () { return {} }
  }
</script>
