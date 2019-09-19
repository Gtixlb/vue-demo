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
        :key="index"
        @delete="handleDelete"
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
    },
    //子组件传值父组件进行删除
    handleDelete (index) {
      this.list.splice(index, 1)
    }
  }
}
</script>

<style>

</style>
