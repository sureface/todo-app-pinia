<template>
  <div class="action__modals" @click="$emit('close_modal', $event)">
    <div class="action__modals-card" @click.stop>
      <div class="card__wrapper">
        <div class="card__wrapper_close" @click.stop="$emit('close_modal', $event)">
          <div>X</div>
        </div>
        <div class="text-center text-secondary text-lg">
          Please Add New Employers
        </div>
        <form ref="form"  class="mb-3">
          <b-form-group
              label="Name"
              label-for="name-input"
              invalid-feedback="Name is required"
              :state="nameState"
              class="mb-2"
          >
            <b-form-input
                id="name-input"
                v-model="name"
                :state="nameState"
                required
                class="shadow-none"
            ></b-form-input>
          </b-form-group>
          <b-form-group
              label="Last Name"
              label-for="Lname-input"
              invalid-feedback="Last Name is required"
              :state="nameState"
              class="mb-2"
          >
            <b-form-input
                id="Lname-input"
                v-model="last_name"
                :state="nameState"
                required
                class="shadow-none"
            ></b-form-input>
          </b-form-group>
          <b-form-group
              label="Age"
              label-for="age-input"
              invalid-feedback="Age is required"
              :state="nameState"
              class="mb-2"
          >
            <b-form-input
                id="age-input"
                v-model="age"
                :state="nameState"
                required
                class="shadow-none"
            ></b-form-input>
          </b-form-group>
          <b-form-group
              label="Last Work Place"
              label-for="last-work-input"
              invalid-feedback="Last Work Place is required"
              :state="nameState"
          >
            <b-form-input
                id="last-work-input"
                v-model="last_work_place"
                :state="nameState"
                required
                class="shadow-none"
            ></b-form-input>
          </b-form-group>
        </form>

        <div class="mt-5 mb-5">
          <hr>
        </div>


        <div class="d-flex align-items-center justify-content-end mt-4">
          <button type="button" class="btn btn-success" @click="addNew">Add Employer</button>
        </div>

      </div>
    </div>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "modal",
  data() {
    return {
      name: '',
      last_name: '',
      age: null,
      last_work_place: '',
      nameState: null,
    }
  }
}
</script>

<style scoped>

</style>