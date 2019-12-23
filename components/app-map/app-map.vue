<template>
  <div class="map">
    <div ref="map" class="map__background"></div>
    <div class="map__contacts">
      <h2 class="map__heading"><img alt="" src="./svg-house.svg" class="map__icon" /> Наш адрес:</h2>
      <div>Республика Беларусь,</div>
      <div>Гродненская область,</div>
      <div>Щучинский район,</div>
      <div>д. Обруб, 19</div>
    </div>
  </div>
</template>
<script>
import YandexMap from 'ymaps'

export default {
  mounted () {
    YandexMap
      .load('https://api-maps.yandex.ru/2.1/?lang=ru_RU')
      .then(maps => {
        const map = new maps.Map(this.$refs.map, {
          center: [53.719484, 24.508379],
          zoom: 13
        })
        const placemark = new maps.Placemark([53.719484, 24.498379], {
          balloonContent: 'Республика Беларусь, Гродненская область, Щучинский район, д. Обруб, 19'
        }, {preset: 'islands#darkGreenVegetationIcon'})
        map.geoObjects.add(placemark)
        map.behaviors.disable('scrollZoom')
      })
      .catch(error => console.log('Failed to load Yandex Maps', error))
  }
}
</script>
<style src="./app-map.scss" lang="scss"/>
