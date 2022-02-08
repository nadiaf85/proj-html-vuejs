<template>

<section class="popular_dishes">
    <h1>Our Most Popular Dishes</h1>
    <div class="container">
        <div class="row">
            <div class="col-5">
                <ul>
                    <li v-for="(element, index) in dishes" :key="index"></li>
                </ul>
            </div>
        </div>
    </div>

</section>
  
</template>

<script>
export default {
    name: 'Main',
    data() {
      return{
        dishes: [
            {
                image: require ("../../assets/images/skin-on-fries-200x286.jpg"),
                type: "Skin On Fries",
                price: "$ 3.00-$ 6.00",
            },
            {
                type: "Choco Cookie Frappe",
                price: "$ 4.99",
            },
            {
                type: "The Donut Burger",
                price: "$ 6.99",
            }
        ]
      }
  }
}
</script>

<style lang="scss" scoped>

</style>