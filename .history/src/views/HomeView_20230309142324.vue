<template>
  <!-- <div>
    <TodoList/>
  </div> -->
  <div>
    <AddToolField/>
    <ToolsList @resetChange="resetTodoList"/>
    <AddSiretFieldInput/>
    <SelectCountry/>
  </div>
</template>

<script>
// @ is an alias to /src
/* import TodoList from '@/components/TodoList.vue' */
import AddToolField from '@/components/AddToolField.vue'
import AddSiretFieldInput from '@/components/AddSiretFieldInput.vue'
import SelectCountry from '@/components/SelectCountry.vue'
import ToolsList from '@/components/ToolsList.vue'
import { mapActions, mapMutations } from 'vuex'
import SelectCountry from '@/components/SelectCountry.vue'

export default {
  name: 'HomeView',
/* components: {
  TodoList
} */
methods: {
  ...mapMutations({
    resetTodoList: "todo/TODO_LIST_SET"
  }),
  ...mapActions("todo", [ "resetList"]),
},
components: {
  SelectCountry,
  AddToolField,
  AddSiretFieldInput,
  ToolsList,
  SelectCountry
}
}
</script>
