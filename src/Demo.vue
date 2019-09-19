<template>
  <div>
    <input v-model="inputValue" />
    <button @click="clickSubmit">提交</button>
    <ul v-for="(item,index) in list":key="index">
      <li>{{item}}</li>
    </ul>
  </div>
</template>

<script>

export default {
  //sssss
  //data : function () {
  data () {
     return {
      inputValue: '',
      list: []
     }
  },
  methods: {
    clickSubmit () {
      this.list.push(this.inputValue)
      this.inputValue = ''
    }
  }
}
</script>

<style>

</style>
