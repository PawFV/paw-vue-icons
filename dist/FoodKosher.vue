<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon food-kosher-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M1 7V9H3C3.57 9 4 9.43 4 10V17H6V10C6 8.36 4.64 7 3 7H1M7 7V14C7 15.65 8.36 17 10 17H14C15.65 17 17 15.65 17 14V7H15V14C15 14.57 14.57 15 14 15H10C9.43 15 9 14.57 9 14V13H10C11.65 13 13 11.65 13 10V7H11V10C11 10.57 10.57 11 10 11H9V7H7M18 7V9H20C20.57 9 21 9.43 21 10V14C21 14.57 20.57 15 20 15H18V17H20C21.65 17 23 15.65 23 14V10C23 8.36 21.65 7 20 7H18Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "FoodKosherIcon",
  props: {
    title: {
      type: String,
      default: "Food Kosher icon"
    },
    decorative: {
      type: Boolean,
      default: false
    },
    fillColor: {
      type: String,
      default: "currentColor"
    },
    size: {
      type: Number,
      default: 24
    }
  }
}
</script>
