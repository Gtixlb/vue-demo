<template>
  <div>
   <div>
     <input v-model="inputValue" />
     <button @click="clickSubmit">提交</button>
   </div>
    <ul>
      <todo-item
        v-for="(item,index) of list"
        :index="index"
        :content="item"
      ></todo-item>
    </ul>
  </div>
</template>

<script>

import TodoItem from './components/TodoItem'

export default {
  //comments
  components: {
    'todo-item': TodoItem
  },
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
