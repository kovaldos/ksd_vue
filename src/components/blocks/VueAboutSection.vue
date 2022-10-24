<template>
  <section class="section about-company">
    <div class="container about-company__container">
      <div class="about-company__cols">
        <div class="about-company__col about-company__col--01">
          <h2 class="title title--h2 about-company__title">{{ title }}</h2>
          <h3 class="title title--h3 about-company__subtitle">
            {{ subtitle }}
          </h3>
          <div class="about-company__pic-wrap">
            <img
              src="@/assets/img/content/about-company-img-1.jpg"
              srcset="@/assets/img/content/about-company-img-1@2x.jpg 2x"
              alt="Экскаватор-разрушитель работает"
            />
          </div>
        </div>
        <div class="about-company__col about-company__col--02">
          <p class="text about-company__desc">
            {{ desc }}
          </p>
          <p class="text about-company__text">
            {{ text }}
          </p>
          <ul class="about-company__list">
            <li
              class="text text--sm about-company__list-item"
              v-for="(item, i) in items"
              :key="i"
            >
              {{ item }}
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      title: "ГК 'КСД'",
      subtitle: "О компании",
      desc: "Мы — молодая, быстро растущая компания, предоставляем большой перечень услуг, связанных со строительством и сносом объектов.",
      text: "В июле 2015 года в Москве начала свою производственную деятельность компания «Конструктив-СД». Основные задачи, которые мы перед собой поставили, были четко сформулированы в нашем названии",
      items: [
        "Конструктив означает отношение к работе — только конструктивное, т. е. созидающее, основополагающее и плодотворное.",
        "С — строительство, разное, например, дорог из вторичного щебня, автомобильных стоянок, спортивных площадок, благоустройство парков и скверов и многих других объектов.",
        "Д — демонтаж сложных сооружений и заводов, жилых домов, срок жизни которых закончился, освобождение территорий и подготовка площадок под новое строительство.",
      ],
    };
  },
};
</script>

<style></style>
