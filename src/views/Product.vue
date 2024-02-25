<template>
  <div>
    <div v-for="(product, index) in products" :key="index" class="product-card">
      <img :src="product.image" alt="Product Image">
      <div class="description">
        <h3>{{ product.name }}</h3>
        <p>Description: {{ product.description }}</p>
        <p>Price: ${{ product.price }}</p>
        <button @click="openModal(product)">View Details</button>
      </div>
    </div>

   <!-- Modal -->
<div v-if="showModal" class="modal" ref="modal">
  <div class="modal-content">
    <span class="close" @click="closeModal">&times;</span>
    <div class="card">
      <div class="card__title">
        <div class="icon">
          <a href="#"><i class="fa fa-arrow-left"></i></a>
        </div>
        <h3>{{ selectedProduct.name }}</h3>
      </div>
      <div class="card__body">
        <div class="half">
          <div class="featured_text">
            <h1>{{ selectedProduct.name }}</h1>
            <p class="sub">Product Description</p>
            <p class="price">$ {{ selectedProduct.price }}</p>
          </div>
          <div class="image">
            <img :src="selectedProduct.image" alt="Product Image">
          </div>
        </div>
        <div class="half">
          <div class="description">
            <p>{{ selectedProduct.description }}</p>
          </div>
          <span class="stock"><i class="fa fa-pen"></i> In stock</span>
          <!-- For simplicity, we're not including the reviews section in the modal -->
        </div>
      </div>
      <div class="card__footer">
        <div class="recommend">
          <!-- We don't have a recommended by field in the selected product -->
        </div>
        <div class="action">
          <!-- You can add an action button here if needed -->
        </div>
      </div>
    </div>
  </div>
</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showModal: false,
      selectedProduct: {},
      products: [
        { id: 1, name: 'Silver Necklace', description: 'Beautiful silver necklace with pendant.', price: 50, rating: 4, image: 'https://via.placeholder.com/150' },
        { id: 2, name: 'Leather Bracelet', description: 'Stylish leather bracelet for men.', price: 30, rating: 3, image: 'https://via.placeholder.com/150' },
        { id: 3, name: 'Gold Ring', description: 'Elegant gold ring for special occasions.', price: 40, rating: 5, image: 'https://via.placeholder.com/150' },
        // Add more products as needed
      ]
    };
  },
  methods: {
    openModal(product) {
      this.selectedProduct = product;
      this.showModal = true;
      document.body.classList.add('modal-open');
    },
    closeModal() {
      this.showModal = false;
      document.body.classList.remove('modal-open');
    }
  }
}
</script>

<style>
.modal {
  display: none;
  position: fixed;
  z-index: 1;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  overflow: auto;
  background-color: rgba(0, 0, 0, 0.4);
}

.modal-content {
  background-color: #fefefe;
  margin: 10% auto;
  padding: 20px;
  border: 1px solid #888;
  width: 80%;
  border-radius: 5px;
}

.close {
  color: #aaa;
  float: right;
  font-size: 28px;
  font-weight: bold;
}

.close:hover,
.close:focus {
  color: black;
  text-decoration: none;
  cursor: pointer;
}

/* Show modal */
.modal-open {
  overflow: hidden;
}

.modal-open .modal {
  display: block;
}
</style>
