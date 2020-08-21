<template>
  <v-container>
    <block-geo></block-geo>
    <block-twitter></block-twitter>
  </v-container>
</template>

<script>
  import BlockTwitter from '@/components/BlockTwitter'
  import BlockGeo from '@/components/BlockGeo'

  export default {
    name: 'Container',
    components: {
      BlockTwitter,
      BlockGeo,
    }
  }
</script>
