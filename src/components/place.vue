<template>
  <section class="location-section">
    <div class="location-text-overlay">
      <h2 class="section-title">Наше местоположение</h2>
      <p class="section-subtitle">Тобыл, ул.Механизаторов 5</p>
    </div>

    <div class="map-container">
      <iframe
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2390.2386208844046!2d63.6904704!3d53.1956366!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x43cc8b1b20b125f7%3A0xa2b779d49c405ccf!2z0JrRgNC10L_RkdC2INCh0YLRgNC-0Lk!5e0!3m2!1sru!2skz!4v1751120128561!5m2!1sru!2skz"
        width="100%"
        height="400"
        style="border:0; border-radius: 10px;"
        allowfullscreen=""
        loading="lazy"
        referrerpolicy="no-referrer-when-downgrade"
      ></iframe>
    </div>

    <div class="photo-row">
      <img
        v-for="(img, idx) in images"
        :key="idx"
        :src="img"
        class="location-image"
        :alt="'Фото ' + (idx + 1)"
      />
    </div>
  </section>
</template>

<script>
export default {
  name: "LocationSection",
  data() {
    return {
      images: [
        "/images/photo1.jpg",
        "/images/photo2.jpeg",
        "/images/photo3.jpg"
      ]
    };
  }
};
</script>

<style scoped>
.location-section {
  text-align: center;
  padding: 40px 20px;
  font-family: Arial, sans-serif;
  background: transparent;
}

.section-title {
  font-size: 2.5rem;
  color: #fff;
  margin-bottom: 10px;
}

.section-subtitle {
  font-size: 2rem;
  color: #fff;
  margin-bottom: 30px;
}

.location-text-overlay {
  display: inline-block;
  background-color: rgba(0, 0, 0, 0.3);
  padding: 20px;
  border-radius: 12px;
  margin-bottom: 30px;
}

.section-title,
.section-subtitle {
  color: #fff;
  text-shadow: 1px 1px 4px rgba(0, 0, 0, 0.9);
}

.map-container {
  max-width: 800px;
  margin: 0 auto 40px;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.2);
}

.photo-row {
  display: flex;
  justify-content: center;
  flex-wrap: nowrap;
  gap: 20px;
  overflow-x: auto;
  padding-bottom: 20px;
}

.location-image {
  width: 400px;
  height: 300px;
  object-fit: contain; /* сохраняем пропорции */
  transition: transform 0.3s ease, border 0.3s ease;
  border: 4px solid transparent;
  border-radius: 12px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
  flex-shrink: 0;
}

.location-image:hover {
  transform: scale(1.05);
  border: 4px solid #c62828;
}

@media (max-width: 768px) {
  .location-image {
    width: 90vw;
    height: auto;
  }
}
</style>
