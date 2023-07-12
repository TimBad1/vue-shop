<template>
  <div class="catalog__card">
    <a class="catalog__pic" href="#">
      <img :src="img" :alt="title">
    </a>
    <h3 class="catalog__title">
      <a href="#">{{ title }}</a>
    </h3>
    <span class="catalog__price"> {{ price }} ₽</span>
    <ul class="colors colors--black">
      <li class="colors__item">
        <label class="colors__label">
          <input class="colors__radio sr-only" type="radio" value="#73B6EA" v-model="color">
          <span class="colors__value" style="background-color: #73B6EA;"></span>
        </label>
      </li>
      <li class="colors__item">
        <label class="colors__label">
          <input class="colors__radio sr-only" type="radio" value="#8BE000" v-model="color">
          <span class="colors__value" style="background-color: #8BE000;">
                  </span>
        </label>
      </li>
      <li class="colors__item">
        <label class="colors__label">
          <input class="colors__radio sr-only" type="radio" value="#222" v-model="color">
          <span class="colors__value" style="background-color: #222;"></span>
        </label>
      </li>
    </ul>
  </div>

</template>

<script>
import colors from "@/data/colors";
export default {
  data() {
    return {
      color: '#73B6EA',
    }
  },
  props: ['img', 'title', 'price'],
}
</script>