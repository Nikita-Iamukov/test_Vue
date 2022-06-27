<template>
    <v-container>
        <h1>Choose your pizza</h1>
<VueSlickCarousel v-bind="settings">
  <CardItemPizza
    v-for="piz in pizza" 
    :key="piz.id"
    :info="piz"
  />
</VueSlickCarousel>
    </v-container>
</template>
 
<script>
  import VueSlickCarousel from 'vue-slick-carousel'
  import 'vue-slick-carousel/dist/vue-slick-carousel.css'
  import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'
  import CardItemPizza from './CardItemPizza.vue'
 console.log(window.innerWidth)
  export default {
    name: 'MyComponent',
    components: { VueSlickCarousel, CardItemPizza },
    data: () => ({
      pizza: [
        {id: 1, name: 'Peperoni', price: '100'},
        {id: 2, name: 'Margarita', price: '540'},
        {id: 3, name: '4cheese', price: '700'},
        {id: 4, name: 'Proshuto', price: '1000'},
        {id: 5, name: 'Diabolo', price: '290'},
        {id: 6, name: 'PapaJons', price: '990'},
        {id: 7, name: 'Dominos', price: '390'},
        {id: 8, name: 'Dodo', price: '590'},
        {id: 9, name: 'Hot', price: '490'},
        {id: 10, name: 'Focacho', price: '770'},
      ],
      settings: {
        vertical: window.innerWidth < 700 ? true : false,
        arrows: true,
        infinite: true,
        slidesToShow: 3,
        speed: 500,
        rows: 2,
        slidesPerRow: 1
      }
  })
  }
</script> 
<style>
h1 {
    text-align: center 
}
.slick-prev:before {
    color: orange
}
.slick-next:before {
    color: orange
}
</style>