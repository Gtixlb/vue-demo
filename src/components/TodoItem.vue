<template>
  <li @click="clickDelete">{{content}}</li>
</template>

<script>
export default {
  props: ['content', 'index'],
  methods: {
    clickDelete () {
      this.$emit('delete', this.index)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
