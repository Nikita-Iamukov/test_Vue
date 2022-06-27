<template>
    <v-container>
        <v-card
            class="mx-auto"
            max-width="400"
        >
    <v-img
      height="200px"
      src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQvfFH9hQNp4VUObkm5qLQ02okAfUAPSKCp2Q&usqp=CAU"
    >
    </v-img>

    <v-card-title class="pb-0">
      {{ info.name }}
    </v-card-title>
    <v-card-text class="pb-0">
      price: {{ info.price }}
    </v-card-text>
      <router-link to="/card" :props="info">
    <v-card-actions>
      <v-btn
        color="orange"
        text
        elevation="3"
        large
        block
      >
        Make order
      </v-btn>
    </v-card-actions>
    </router-link>
  </v-card>
  </v-container>
</template>
 
<script>
  export default {  
    props: {
        info: {
            type: Object,
            required: true
        }
    }  
    }
</script> 
<style></style>