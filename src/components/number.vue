<template>
  <section class="contact-section">
    <div class="contact-text-overlay">
      <h2 class="section-title">Контакты</h2>
      </div>
      <p class="phone-number">
        <a :href="'tel:' + phone">{{ phone }}</a>
      </p>
  </section>
</template>


<script>
export default {
  name: "ContactInfo",
  data() {
    return {
      phone: "+7 705 199 1341"
    };
  }
};
</script>

<style scoped>
.contact-section {
  text-align: center;
  padding: 40px 20px;
  color: #fff;
  border-radius: 12px;
}

.section-title {
  font-size: 2.5rem;
  color: #fff;
  margin-bottom: 15px;
}

.phone-number a {
  font-size: 1.8rem;
  color: #fff;
  text-decoration: none;
  background-color: #c62828;
  border: 2px solid #fff;
  padding: 10px 20px;
  border-radius: 12px;
  transition: all 0.3s ease;
  display: inline-block;
}

.phone-number a:hover {
  background-color: #8b1a1a;
  border-color: #fff;
  color: #fff;
}
.contact-text-overlay {
  display: inline-block;
  background-color: rgba(0, 0, 0, 0.3); /* затемнение под текстом */
  padding: 20px;
  border-radius: 12px;
}

.section-title {
  text-shadow: 1px 1px 4px rgba(0, 0, 0, 0.9); /* делает белый текст читаемым */
}
</style>
