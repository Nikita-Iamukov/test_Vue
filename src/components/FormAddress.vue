<template>
<v-container>
       <h1>Make order</h1>
        <h1 style="text-align: start">
        </h1>
       <h1 style="text-align: start">Address</h1>
       <v-form
    ref="form"
    v-model="valid"
    lazy-validation
  >
    <v-text-field
      v-model="street"
      label="street"
      required
    ></v-text-field>

    <v-text-field
      v-model="house"
      label="house"
      required
    ></v-text-field>

    <v-text-field
      v-model="flat"
      label="flat"
      required
    ></v-text-field>
    <v-btn
      color="warning"
      @click="selectValidation(street, house, flat)"
    >
      Reset Validation
    </v-btn>
  </v-form>
    </v-container>
</template>
<script>
export default {
  data: () => ({
    street: '',
    house: '',
    flat: '',
    valid: ''
  }),
  methods: {
    selectValidation(street, house, flat) {
      localStorage.setItem(Date.now(), `street:${street}, house:${house}, flat:${flat}`)
    }
  }
}

</script>

<style scoped>
</style>