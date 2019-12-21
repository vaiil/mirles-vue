<template>
      <!-- <logo /> -->
<div>
  <header class="header typography__font-Norms">
  <div class="header__wrapper wrapper">
    <div class="header__logo">
      <img src="~assets/img/logo.png" alt="Логотип Лес Мир">
    </div>
    <h1 class="header__title">“Лесной мир”</h1>
    <h2 class="header__description">Питомник туй</h2>
    <h3 class="header__offer">
      <span>Спецпредложение на весну 2020 года</span>
    </h3>
  </div>
</header>

<main class="main typography__font-Roboto">
  <div class="main__wrapper wrapper">
    <section class="main__visual">
      <h2 class="typography__tuia">ТУЯ ЗАПАДНАЯ 'СМАРАГД' (ПРЕМИУМ)</h2>
      <h3 class="typography__tuia typography__tuia_sub">Thuja occidentalis 'Smaragd'</h3>
      <div class="main__gallery">
        <img src="src/img/gallery/gallery_bg.png" class="main__gallery-bg">
        
        <!-- img-container - if you wanned link instead of div -->
        <div class="main__img-container"><img src="~assets/img/gallery/sam/sam_1.png" alt=""></div>
        <div class="main__img-container"><img src="~assets/img/gallery/sam/sam_2.png" alt=""></div>
        <div class="main__img-container"><img src="~assets/img/gallery/sam/sam_3.png" alt=""></div>
        <div class="main__img-container"><img src="~assets/img/gallery/sam/sam_4.png" alt=""></div>
      </div>
    </section>
    <aside class="main__info">
      <table class="main__table">
        <tr>
          <td rowspan="2">Высота, м.</td>
          <td colspan="3">Количество, шт.</td>
        </tr>
        <tr>
          <td>от 100</td>
          <td>от 300</td>
          <td>от 500</td>
        </tr>
        <tr>
          <td>1,4-1,6</td>
          <td>2 100 р.</td>
          <td>1 970 р.</td>
          <td>1 897 р.</td>
        </tr>
        <tr>
          <td>1,6-1,8</td>
          <td>2 870 р.</td>
          <td>2 697 р.</td>
          <td>2 550 р.</td>
        </tr>
        <tr>
          <td>1,8-2,0</td>
          <td>3 950 р.</td>
          <td>3 770 р.</td>
          <td>3 550 р.</td>
        </tr>
        <tr>
          <td>2,0-2,2</td>
          <td>4 750 р.</td>
          <td>4 497 р.</td>
          <td>4 299 р.</td>
        </tr>
      </table>

      <div class="main__links-wrapper">
        <a href="tel:74951201631" class="icon-phone">+7 (495) 120-16-31</a>
        <a href="http://lesmir.ru" target="_blank" class="icon-world">сайт: lesmir.ru</a>
      </div>      
    </aside>
  </div>

  <div class="main__wrapper wrapper">
    <section class="main__visual">
      <h2 class="typography__tuia">ТУЯ ЗАПАДНАЯ 'БРАБАНТ' (ПРЕМИУМ)</h2>
      <h3 class="typography__tuia typography__tuia_sub">Thuja occidentalis 'BRABANT'</h3>
      <div class="main__gallery">
        <img src="src/img/gallery/gallery_bg.png" class="main__gallery-bg">

        <div class="main__img-container"><img src="~assets/img/gallery/brab/brab_1.png" alt=""></div>
        <div class="main__img-container"><img src="~assets/img/gallery/brab/brab_2.png" alt=""></div>
        <div class="main__img-container"><img src="~assets/img/gallery/brab/brab_3.png" alt=""></div>
        <div class="main__img-container"><img src="~assets/img/gallery/brab/brab_4.png" alt=""></div>
      </div>
    </section>
    <aside class="main__info">
      <table class="main__table">
        <tr>
          <td rowspan="2">Высота, м.</td>
          <td colspan="3">Количество, шт.</td>
        </tr>
        <tr>
          <td>от 100</td>
          <td>от 300</td>
          <td>от 500</td>
        </tr>
        <tr>
          <td>1,4-1,6</td>
          <td>1 990 р.</td>
          <td>1 890 р.</td>
          <td>1 790 р.</td>
        </tr>
        <tr>
          <td>1,6-1,8</td>
          <td>2 750 р.</td>
          <td>2 599 р.</td>
          <td>2 470 р.</td>
        </tr>
        <tr>
          <td>1,8-2,0</td>
          <td>3 599 р.</td>
          <td>3 390 р.</td>
          <td>3 270 р.</td>
        </tr>
        <tr>
          <td>2,0-2,2</td>
          <td>3 870 р.</td>
          <td>3 670 р.</td>
          <td>3 499 р.</td>
        </tr>
        <tr>
          <td>2,2-2,4</td>
          <td>3 990 р.</td>
          <td>3 790 р.</td>
          <td>3 599 р.</td>
        </tr>
      </table>

      <!-- Кнопка заказа? -->
      <div class="main__contacts">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512" class="svg-house">
          <g>
            <path d="M256,51.2c-75.405,0-136.533,61.128-136.533,136.533S180.595,324.267,256,324.267s136.533-61.128,136.533-136.533     C392.447,112.364,331.37,51.286,256,51.2z M256,307.2c-65.98,0-119.467-53.487-119.467-119.467S190.02,68.267,256,68.267     s119.467,53.487,119.467,119.467C375.393,253.682,321.949,307.126,256,307.2z"/>
            <path d="M346.333,155.217l-79.317-57.342c-6.257-5.28-15.381-5.378-21.75-0.233l-79.075,48.692     c-2.596,1.599-4.142,4.461-4.056,7.509c0.086,3.048,1.792,5.818,4.475,7.267s5.935,1.357,8.531-0.242l12.592-7.754v94.354     c0.011,9.421,7.645,17.056,17.067,17.067h25.6c9.421-0.011,17.056-7.645,17.067-17.067v-34.133     c0.013-2.521,1.136-4.909,3.068-6.528s4.48-2.305,6.965-1.876c4.276,1.097,7.206,5.031,7.033,9.442v33.096     c0.011,9.421,7.646,17.056,17.067,17.067h25.6c9.421-0.011,17.056-7.645,17.067-17.067v-87.14l12.067,8.723     c2.471,1.793,5.711,2.129,8.498,0.883c2.786-1.247,4.695-3.887,5.005-6.924S348.81,157.001,346.333,155.217z M307.2,247.467     h-25.6v-33.096c0.166-12.738-8.774-23.783-21.267-26.275c-7.437-1.262-15.052,0.815-20.819,5.677     c-5.767,4.862-9.101,12.017-9.114,19.56v34.133h-25.6v-102.4c-0.047-0.747-0.196-1.484-0.442-2.191l50.4-31.034     c0.448-0.265,0.872-0.569,1.267-0.908c0.221,0.198,0.452,0.384,0.692,0.558l50.483,36.496V247.467z"/>
            <path d="M256,0C141.958,0,68.267,74.583,68.267,190.008c0,98.867,113.458,243.279,161.908,304.946l5.658,7.213     c4.849,6.206,12.286,9.832,20.161,9.833c7.876,0.001,15.313-3.625,20.163-9.829l5.625-7.162     c48.458-61.671,161.95-206.1,161.95-305C443.733,74.583,370.042,0,256,0z M268.358,484.463l-5.642,7.187     c-1.666,1.985-4.125,3.131-6.717,3.131c-2.592,0-5.05-1.146-6.717-3.131h-0.009l-5.683-7.242     c-43.283-55.092-158.258-201.434-158.258-294.4C85.333,62.5,173.492,17.067,256,17.067S426.667,62.5,426.667,190.008     C426.667,283.004,311.658,429.367,268.358,484.463z"/>
          </g>
        </svg>
        <h2>Наш адрес:</h2>
        <span>республика беларусь,</span>
        <span>гродненская область,</span>
        <span>щучинский район,</span>
        <span>д. обруб, 19</span>
      </div>      
    </aside>
  </div>
</main>
</div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  }
}
</script>
