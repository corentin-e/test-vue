<template>
  <div>
    <AddToolField/>
    <ToolsList/>
  </div>
</template>

<script>
// @ is an alias to /src
import AddToolField from '@/components/AddToolField.vue';
import ToolsList from '@/components/ToolsList.vue'

export default {
  name: 'HomeView',
  components: {
    AddToolField,
    ToolsList
}
}
</script>
