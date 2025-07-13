<template>
  <section class="working-hours">
    <div class="content-wrapper">
      <div class="contact-text-overlay">
        <h2 class="section-title">График работы</h2>
      </div>
      <div class="hours-block">
        <p><strong>Будние дни:</strong> 8:15 – 18:00</p>
        <p><strong>Суббота, Воскресенье:</strong> 8:15 – 17:00</p>
        <p class="note">Без выходных</p>
      </div>
    </div>
  </section>
</template>


<script>
export default {
  name: "WorkingHours"
};
</script>

<style scoped>
.working-hours {
  text-align: center;
  padding: 40px 20px;
  font-family: Arial, sans-serif;
  border-radius: 12px;
  color: #fff;
}

.section-title {
  font-size: 2.5rem;
  color: #fff;
  margin-bottom: 15px;
}

.hours-block {
  font-size: 1.4rem;
  color: #fff;
  line-height: 1.6;
  border: 2px solid #fff;
  background-color: #c62828;
  display: inline-block;
  padding: 20px 30px;
  border-radius: 12px;
  transition: all 0.3s ease;
}

.hours-block:hover {
  background-color: #8b1a1a;
}

.note {
  margin-top: 10px;
  font-style: italic;
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
.content-wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 20px;
}
</style>
