<template>
  <section class="main-section">
    <div class="text-overlay">
      <h2 class="section-title">Магазин Крепёж Строй </h2>
      <p class="section-description">
        Рады предложить вам: Крепёж оптом и в розницу, строительные смеси, краски, лаки, osb, гипсокартон, цемент,
        утеплители, сантехника, электрика, электро инструмент, садовый инвентарь и многое другое по приемлемым ценам.
      </p>
          <h2 class="section-title">У нас в продаже:</h2>
    </div>
    <div class="divider"></div>

    <div class="carousel">
      <button class="arrow left" @click="prev">&#10094;</button>

      <img
        :src="images[current]"
        :alt="'Слайд ' + (current + 1)"
        class="carousel-image"
      />

      <button class="arrow right" @click="next">&#10095;</button>
    </div>
  </section>
</template>

<script>
export default {
  name: "MainSection",
  data() {
    return {
      images: [
        '/images/image1.jpeg',
        '/images/image2.jpeg',
        '/images/image3.jpeg',
        '/images/image4.jpeg',
        '/images/image5.jpeg',
        '/images/image6.jpeg',
        '/images/image7.jpeg',
        '/images/image8.jpeg',
        '/images/image9.jpeg',
        '/images/image10.jpeg',
        '/images/image11.jpeg',
        '/images/image13.jpeg',
        '/images/image14.jpeg',
        '/images/image15.jpeg',
        '/images/image16.jpeg',
        '/images/image18.jpeg',
        '/images/image19.jpeg',
        '/images/image20.jpeg',
        '/images/image21.jpeg',
        '/images/image23.jpeg',
        '/images/image24.jpeg',
        '/images/image25.jpeg',
        '/images/image26.jpeg',
        '/images/image27.jpeg',
        '/images/image28.jpeg',
        '/images/image29.jpeg',
        '/images/image31.jpeg',
        '/images/image32.jpeg'
      ],
      current: 0
    };
  },
  methods: {
    next() {
      this.current = (this.current + 1) % this.images.length;
    },
    prev() {
      this.current = (this.current - 1 + this.images.length) % this.images.length;
    }
  }
};
</script>

<style scoped>
.main-section {
  text-align: center;
  padding: 40px 20px;
  font-family: Arial, sans-serif;
}

.text-overlay {
  margin-bottom: 20px;
  background-color: rgba(0, 0, 0, 0.4); /* только затемнение */
  padding: 20px;
  border-radius: 10px;
  display: inline-block;
}

.section-title {
  font-size: 3.0rem;
  color: #fff;
  margin-bottom: 10px;
  text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.8); /* добавлена тень */
}

.section-description {
  font-size: 2.0rem;
  color: #fff;
  text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.8); /* добавлена тень */
}

.divider {
  height: 3px;
  background-color: #000;
  width: 80%;
  margin: 30px auto;
  border-radius: 2px;
}

.carousel-image {
  width: 600px;
  height: 400px;
  max-width: 90vw;
  border: 4px solid transparent;
  border-radius: 12px;
  transition: transform 0.3s ease, border 0.3s ease;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
  object-fit: contain;
}

.carousel-image:hover {
  transform: scale(1.05);
  border: 4px solid #c62828;
}

.carousel {
  position: relative;
  display: inline-block;
  max-width: 90vw;
}

/* Адаптивность */
@media (max-width: 600px) {
  .carousel-image {
    width: 100%;
    height: 250px;
  }

  .arrow.left {
    left: -20px;
  }

  .arrow.right {
    right: -20px;
  }
}

/* Стрелки */
.arrow {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  font-size: 2rem;
  background-color: rgba(255, 255, 255, 0.7);
  border: none;
  color: #c62828;
  padding: 10px;
  cursor: pointer;
  border-radius: 50%;
  user-select: none;
  transition: background 0.3s;
  z-index: 1;
}

.arrow:hover {
  background-color: rgba(255, 255, 255, 0.9);
}

.arrow.left {
  left: -40px;
}

.arrow.right {
  right: -40px;
}
</style>
