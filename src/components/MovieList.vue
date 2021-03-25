<template>
<div class="wrapper">
  <div class="products">
    <div class="product" v-for="product in products" :key="product.id">
      <div class="info">
           <!-- "id": 2,
    "title": "God's Gun",
    "genre": "Western",
    "poster": "http://dummyimage.com/200x200.png/cc0000/ffffff",
    "show-time": "11:58 AM",
    "cost": 10.6 -->
        <h1>{{product.title}}</h1>
        <p>{{product.genre}}</p>
      </div>
      <div class="image">
        <!-- <img :src="product.poster"> -->
                <!-- <img :src="https://dummyimage.com/600x400/bd24bd/41479c&text={{title with + for space}}hello+there"> -->

        <img :src= "dummyimage.com/600x400/bd24bd/41479c&text=" + {{product.title}}>
      </div>
      <div class="price">
        <h2>{{product.show-time}}</h2>
        <button class="auto" @click="addToTickets(product)">Buy a Ticket</button>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'ProductList',
  props: {
    products: Array
  },
  methods: {
      addToTickets(product) {
        this.$root.$data.cart.push(product)
      }
  }
}
</script>

<style scoped>
.wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
}

.products {
  margin-top: 20px;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}

.product {
  margin: 10px;
  margin-top: 50px;
  width: 200px;
}

.product img {
  border: 2px solid #333;
  height: 250px;
  width: 200px;
  object-fit: cover;
}

.product .image {
  display: flex;
  justify-content: center;
  margin-bottom: 5px;
}

.info {
  background: #F2921D;
  color: #000;
  padding: 10px 30px;
  height: 80px;
}

.info h1 {
  font-size: 16px;
}

.info h2 {
  font-size: 14px;
}

.info p {
  margin: 0px;
  font-size: 10px;
}


.price {
  display: flex;
}

button {
  height: 50px;
  background: #000;
  color: white;
  border: none;
}

.auto {
  margin-left: auto;
}
</style>