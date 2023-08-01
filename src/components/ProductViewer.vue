```javascript
<template>
  <div class="product-viewer">
    <div class="product-images">
      <img v-for="(image, index) in images" :key="index" :src="image" :class="{ active: index === activeIndex }" />
    </div>
    <div class="controls">
      <button @click="prevImage">Prev</button>
      <button @click="nextImage">Next</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      images: [
        require('@/assets/images/product1.jpg'),
        require('@/assets/images/product2.jpg'),
        require('@/assets/images/product3.jpg'),
        require('@/assets/images/product4.jpg'),
        require('@/assets/images/product5.jpg'),
        require('@/assets/images/product6.jpg'),
        require('@/assets/images/product7.jpg'),
        require('@/assets/images/product8.jpg'),
        require('@/assets/images/product9.jpg'),
        require('@/assets/images/product10.jpg'),
        require('@/assets/images/product11.jpg'),
        require('@/assets/images/product12.jpg'),
        require('@/assets/images/product13.jpg'),
        require('@/assets/images/product14.jpg'),
        require('@/assets/images/product15.jpg'),
        require('@/assets/images/product16.jpg'),
        require('@/assets/images/product17.jpg'),
        require('@/assets/images/product18.jpg'),
        require('@/assets/images/product19.jpg'),
        require('@/assets/images/product20.jpg'),
        require('@/assets/images/product21.jpg'),
        require('@/assets/images/product22.jpg'),
        require('@/assets/images/product23.jpg'),
        require('@/assets/images/product24.jpg'),
        require('@/assets/images/product25.jpg'),
        require('@/assets/images/product26.jpg'),
        require('@/assets/images/product27.jpg'),
        require('@/assets/images/product28.jpg'),
        require('@/assets/images/product29.jpg'),
        require('@/assets/images/product30.jpg'),
        require('@/assets/images/product31.jpg'),
        require('@/assets/images/product32.jpg'),
        require('@/assets/images/product33.jpg'),
        require('@/assets/images/product34.jpg'),
        require('@/assets/images/product35.jpg'),
        require('@/assets/images/product36.jpg')
      ],
      activeIndex: 0
    };
  },
  methods: {
    prevImage() {
      this.activeIndex = (this.activeIndex - 1 + this.images.length) % this.images.length;
    },
    nextImage() {
      this.activeIndex = (this.activeIndex + 1) % this.images.length;
    }
  }
};
</script>

<style scoped>
.product-viewer {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.product-images {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 400px;
  overflow: hidden;
}

.product-images img {
  width: 100%;
  height: 100%;
  object-fit: contain;
  opacity: 0;
  transition: opacity 0.3s ease-in-out;
}

.product-images img.active {
  opacity: 1;
}

.controls {
  display: flex;
  justify-content: center;
  margin-top: 16px;
}

button {
  margin: 0 8px;
  padding: 8px 16px;
  border: none;
  border-radius: 4px;
  background-color: #333;
  color: #fff;
  cursor: pointer;
}

button:hover {
  background-color: #555;
}
</style>
```