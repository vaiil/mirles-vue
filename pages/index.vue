<template>
  <!-- <logo /> -->
  <div>
    <header class="header typography__font-Norms">
      <div class="header__wrapper wrapper">
        <div class="header__logo">
          <img src="~assets/img/logo.png" alt="Логотип Лес Мир">
        </div>
        <div class="header__info">
          <div class="header__left">
            <h2 class="header__description">Питомник туй в Беларусии</h2>
            <h3 class="header__offer">
              <span>Спецпредложение на весну 2020 года</span>
            </h3>
          </div>
          <div class="header__right">
            <a href="tel:+74951201631">+7(495)120-16-31</a>
            <button class="header__callback callback-button" @click="openModal">Заказать звонок</button>
            <a href="mailto:les-mir@yandex.ru" class="header__email">les-mir@yandex.ru</a>
          </div>
        </div>
      </div>
    </header>

    <main class="main typography__font-Roboto">
      <div class="main__wrapper wrapper">
        <section class="main__visual">
          <h2 class="typography__tuia">ТУЯ ЗАПАДНАЯ 'СМАРАГД' (ПРЕМИУМ)</h2>
          <h3 class="typography__tuia typography__tuia_sub">Thuja occidentalis 'Smaragd'</h3>
          <div class="main__gallery">
            <img src="~assets/img/gallery/gallery_bg.png" class="main__gallery-bg">

            <!-- img-container - if you wanned link instead of div -->
            <div class="main__img-container"><img src="~assets/img/gallery/sam/sam_1.png" alt=""></div>
            <div class="main__img-container"><img src="~assets/img/gallery/sam/sam_2.png" alt=""></div>
            <div class="main__img-container"><img src="~assets/img/gallery/sam/sam_3.png" alt=""></div>
            <div class="main__img-container"><img src="~assets/img/gallery/sam/sam_4.png" alt=""></div>
          </div>
        </section>
        <aside class="main__info">
          <table class="main__table">
            <thead>
            <tr>
              <td rowspan="2">Высота, м.</td>
              <td colspan="3">Количество, шт.</td>
            </tr>
            <tr>
              <td>от 100</td>
              <td>от 300</td>
              <td>от 500</td>
            </tr>
            </thead>
            <tbody>
            <tr>
              <th>1,4-1,6</th>
              <td>2 100 р.</td>
              <td>1 970 р.</td>
              <td>1 897 р.</td>
            </tr>
            <tr>
              <th>1,6-1,8</th>
              <td>2 870 р.</td>
              <td>2 697 р.</td>
              <td>2 550 р.</td>
            </tr>
            <tr>
              <th>1,8-2,0</th>
              <td>3 950 р.</td>
              <td>3 770 р.</td>
              <td>3 550 р.</td>
            </tr>
            <tr>
              <th>2,0-2,2</th>
              <td>4 750 р.</td>
              <td>4 497 р.</td>
              <td>4 299 р.</td>
            </tr>
            </tbody>
          </table>

          <div class="main__links-wrapper">
            <button class="callback-button" @click="openModal">Получить дополнительную скидку</button>
            <a href="tel:74951201631" class="icon-phone">+7 (495) 120-16-31</a>
          </div>
        </aside>
      </div>

      <div class="main__wrapper wrapper">
        <section class="main__visual">
          <h2 class="typography__tuia">ТУЯ ЗАПАДНАЯ 'БРАБАНТ' (ПРЕМИУМ)</h2>
          <h3 class="typography__tuia typography__tuia_sub">Thuja occidentalis 'BRABANT'</h3>
          <div class="main__gallery">
            <img src="~assets/img/gallery/gallery_bg.png" class="main__gallery-bg">

            <div class="main__img-container"><img src="~assets/img/gallery/brab/brab_1.png" alt=""></div>
            <div class="main__img-container"><img src="~assets/img/gallery/brab/brab_2.png" alt=""></div>
            <div class="main__img-container"><img src="~assets/img/gallery/brab/brab_3.png" alt=""></div>
            <div class="main__img-container"><img src="~assets/img/gallery/brab/brab_4.png" alt=""></div>
          </div>
        </section>
        <aside class="main__info">
          <table class="main__table">
            <thead>
            <tr>
              <td rowspan="2">Высота, м.</td>
              <td colspan="3">Количество, шт.</td>
            </tr>
            <tr>
              <td>от 100</td>
              <td>от 300</td>
              <td>от 500</td>
            </tr>
            </thead>
            <tbody>
            <tr>
              <th>1,4-1,6</th>
              <td>1 990 р.</td>
              <td>1 890 р.</td>
              <td>1 790 р.</td>
            </tr>
            <tr>
              <th>1,6-1,8</th>
              <td>2 750 р.</td>
              <td>2 599 р.</td>
              <td>2 470 р.</td>
            </tr>
            <tr>
              <th>1,8-2,0</th>
              <td>3 599 р.</td>
              <td>3 390 р.</td>
              <td>3 270 р.</td>
            </tr>
            <tr>
              <th>2,0-2,2</th>
              <td>3 870 р.</td>
              <td>3 670 р.</td>
              <td>3 499 р.</td>
            </tr>
            <tr>
              <th>2,2-2,4</th>
              <td>3 990 р.</td>
              <td>3 790 р.</td>
              <td>3 599 р.</td>
            </tr>
            </tbody>
          </table>

          <div class="main__links-wrapper">
            <button class="callback-button" @click="openModal">Получить дополнительную скидку</button>
            <a href="tel:74951201631" class="icon-phone">+7 (495) 120-16-31</a>
          </div>
        </aside>
      </div>
    </main>

    <footer>
      <app-map/>
    </footer>

    <vue-modal :visible="showForm" @hide="closeModal"
               bg-overlay="rgba(255, 255, 255, 0.7)"
               bg-panel="white"
               animation-panel="modal-slide-top"
               class="callback-modal"
    >
      <form class="form">
        <h2 class="form__heading">
          Оставьте ваши контакты и мы вам перезвоним
        </h2>
        <div class="form__line">
          <label>
            <input type="text" placeholder="Ваше имя" class="form__input"/>
          </label>
        </div>
        <div class="form__line">
          <label>
            <input type="text" placeholder="Ваш телефон" class="form__input"/>
          </label>
        </div>
        <div class="form__line">
          <button class="callback-button form__button" type="submit">Заказать звонок</button>
        </div>
      </form>
    </vue-modal>
  </div>
</template>

<script>
import VueModal from '../components/vue-modal/vue-modal'
import AppMap from '../components/app-map/app-map'

export default {
  data () {
    return {
      showForm: false
    }
  },
  components: {
    VueModal,
    AppMap
  },
  methods: {
    openModal () {
      this.showForm = true
    },
    closeModal () {
      this.showForm = false
    }
  }
}
</script>
