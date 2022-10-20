<template>
  <div class="footer__middle">
    <div class="container footer__container">
      <div class="footer__columns" data-accordion="parent" data-single>
        <div class="footer__col footer__col--01" data-accordion="element">
          <div class="footer__col-accordion-btn" data-accordion="button">
            <span class="footer__col-heading">Компания</span>
            <span class="footer__col-accordion-btn-icon">
              <svg width="14" height="14" aria-hidden="true">
                <use xlink:href="#icon-chevron-down"></use>
              </svg>
            </span>
          </div>
          <ul class="footer__col-list" data-accordion="content">
            <li class="footer__col-list-item">
              <a class="footer__col-link" href="#">История</a>
            </li>
            <li class="footer__col-list-item">
              <a class="footer__col-link" href="#">Новости</a>
            </li>
            <li class="footer__col-list-item">
              <a class="footer__col-link" href="#">Вакансии</a>
            </li>
            <li class="footer__col-list-item">
              <a class="footer__col-link" href="#">Контакты</a>
            </li>
          </ul>
        </div>
        <div class="footer__col footer__col--02" data-accordion="element">
          <div class="footer__col-accordion-btn" data-accordion="button">
            <span class="footer__col-heading">Направления</span
            ><span class="footer__col-accordion-btn-icon">
              <svg width="14" height="14" aria-hidden="true">
                <use xlink:href="#icon-chevron-down"></use>
              </svg>
            </span>
          </div>
          <ul class="footer__col-list" data-accordion="content">
            <li class="footer__col-list-item">
              <a class="footer__col-link" href="#">Снос и Демонтаж</a>
            </li>
            <li class="footer__col-list-item">
              <a class="footer__col-link" href="#">Вывоз и утилизация</a>
            </li>
            <li class="footer__col-list-item">
              <a class="footer__col-link" href="#">Строительство дорог</a>
            </li>
            <li class="footer__col-list-item">
              <a class="footer__col-link" href="#">Аренда спецтехники</a>
            </li>
          </ul>
        </div>
        <div class="footer__col footer__col--03" data-accordion="element">
          <div class="footer__col-accordion-btn" data-accordion="button">
            <span class="footer__col-heading">Блог</span
            ><span class="footer__col-accordion-btn-icon">
              <svg width="14" height="14" aria-hidden="true">
                <use xlink:href="#icon-chevron-down"></use>
              </svg>
            </span>
          </div>
          <ul class="footer__col-list" data-accordion="content">
            <li class="footer__col-list-item">
              <a class="footer__col-link" href="#">Техника</a>
            </li>
            <li class="footer__col-list-item">
              <a class="footer__col-link" href="#">Объекты</a>
            </li>
            <li class="footer__col-list-item">
              <a class="footer__col-link" href="#">Галерея</a>
            </li>
            <li class="footer__col-list-item">
              <a class="footer__col-link" href="#">Видео</a>
            </li>
          </ul>
        </div>
        <div class="footer__col footer__col--04">
          <div class="footer__subscribe subscribe-block">
            <div class="subscribe-block__wrapper">
              <div class="subscribe-block__text-wrapper">
                <p class="subscribe-block__text">
                  Подписка на&nbsp;Новости&nbsp;&amp;&nbsp;Акции:
                </p>
              </div>
              <div
                class="subscribe-block__form-wrapper"
                data-validate
                data-callback="subscribeForm"
              >
                <form class="subscribe-block__form">
                  <div
                    class="custom-input subscribe-block__form-input"
                    data-validate-type="email"
                  >
                    <label>
                      <input
                        type="email"
                        id="subscribe-email"
                        name="email_dlya_podpiski"
                        placeholder="Ваш email..."
                      />
                    </label>
                    <div class="custom-input__error">
                      Пожалуйста введите корректный email
                    </div>
                  </div>
                  <button
                    class="btn subscribe-block__form-submit"
                    type="submit"
                  >
                    <svg width="14" height="14" aria-hidden="true">
                      <use xlink:href="#icon-chevron-right"></use>
                    </svg>
                  </button>
                </form>
              </div>
            </div>
          </div>
          <div class="footer__contact-us-wrapper">
            <div class="footer__contact-us">
              <a
                class="footer__contact-us-social footer__contact-us-social--whatsapp"
                href="#"
              >
                <svg width="26" height="26" aria-hidden="true">
                  <use xlink:href="#icon-whatsapp"></use></svg></a
              ><a class="link footer__contact-us-link" href="tel:+79672117171"
                >+7 967 211-71-71</a
              >
            </div>
            <div class="footer__address">
              <span>105318, г. Москва, ул. Ибрагимова, 31</span>
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
      items: [
        {
          title: "Компания",
          href: "#",
          link1: "История",
          link2: "Новости",
          link3: "Вакансии",
          link4: "Контакты",
          classModifier: "footer__col--01",
        },
        {
          title: "Направления",
          href: "#",
          link1: "Снос и Демонтаж",
          link2: "Вывоз и утилизация",
          link3: "Строительство дорог",
          link4: "Аренда спецтехники",
          classModifier: "footer__col--02",
        },
        {
          title: "Блог",
          href: "#",
          link1: "Техника",
          link2: "Объекты",
          link3: "Галерея",
          link4: "Видео",
          classModifier: "footer__col--03",
        },
      ],
      subs: {
        title: "Подписка на Новости & Акции:",
        input: {
          inputPlaceholder: "Ваш email...",
          inputError: "Пожалуйста введите корректный email",
          inputType: "email",
          inputId: "subscribe-email",
          inputName: "email_dlya_podpiski",
        },
        btn: {
          icon: "icon-chevron-right",
          type: "submit",
        },
      },
      icon: "icon-whatsapp",
      href: "tel:+79672117171",
      text: "+7 967 211-71-71",
      address: "105318, г. Москва, ул. Ибрагимова, 31",
    };
  },
};
</script>

<style></style>
