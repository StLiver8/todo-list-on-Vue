<template>
  <div class="home">
    <CreateEditForm :task="newTask" :formType="addNew"></CreateEditForm>
  </div>
</template>

<script>
  import CreateEditForm from '@/components/CreateEditForm.vue'
  import { mapState } from 'vuex';

  export default {
    name: 'home',
    components: {
      CreateEditForm
    },
    data () {
      return {
        addNew: "addNew"
      }
    },
    computed: {
      ...mapState(['newTask'])
    }
  }
</script>
