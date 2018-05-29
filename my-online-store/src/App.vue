<template>
  <div id="app" class="container my-5">
    <h1>My online store</h1>
      <div class="row">
        <div class="col-md-3" v-for="item in forSale">
          <div class="card">
            <img :src="item.image" :alt="item.name" class="card-img-top">
            <div class="card-body">
              <h4 class="card-title">{{ item.name }}</h4>
              <div class="card-text">${{ item.price / 100 }}</div>
              <div class="row justify-content-end">
                <button class="btn btn-primary">Add to cart</button>
              </div>
            </div>
          </div>
        </div>
      </div>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      forSale: [
        { invId: 1, name: 'An Item', image: '//placehold.it/200', price: 999 },   
        { invId: 2, name: 'Item 2', image: '//placehold.it/200', price: 100 },
        { invId: 3, name: 'Item 3', image: '//placehold.it/200', price: 800 },
        { invId: 4, name: 'Item 4', image: '//placehold.it/200', price: 900 },       
        ],
    };
  },
};
</script

<style>
/* nothing for now*/
</style>