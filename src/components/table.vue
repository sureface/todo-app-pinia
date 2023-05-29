<template>
  <div class="container">

    <div class="text-center mt-5 mb-5 text-secondary h2 text-uppercase">
      list of Employers to Google
    </div>

    <div class="apper">

      <header class="mb-3">
        <button class="btn btn-success" @click="isOpen = !isOpen" >Add Employer</button>
      </header>

      <b-table
          hover
          :items="employers"
          :fields="fields"
          responsive="sm"
          label-sort-asc=""
          label-sort-desc=""
          label-sort-clear=""
          class="apper__item text-white"
      >
        <template v-slot:cell(actions)="{ item }" >
          <div class="d-flex align-items-center justify-content-center">
            <button
                type="button"
                class="btn btn-success me-2"
                @click="editItem(item)"
            >
              Edit
            </button>
            <button
                type="button"
                class="btn btn-danger"
                @click="deleteItem(item)"
            >
              Del
            </button>
          </div>
        </template>
      </b-table>
    </div>

  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "table",
  data() {
    return {
      isOpen: false,
      employers: [],
      fields: [
        { key: 'last_name', sortable: true},
        { key: 'first_name', sortable: true},
        { key: 'age', sortable: true },
        { key: 'last_work_place', sortable: true},
        { key: 'actions'},
      ],
    }
  },
  methods: {
    editItem(item) {
      console.log(item)
    },
    deleteItem(item) {
      console.log(item)
    }
  }
}
</script>

<style scoped>

</style>