<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon car-seat-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M7 18C7 18 4 10 4 6S6 2 6 2H7C7 2 8 2 8 3S7 4 7 6 10 10 10 13 7 18 7 18M12 17C11 17 8 19.5 8 19.5C7.7 19.7 7.8 20 8 20.3C8 20.3 9 22.1 11 22.1H17C18.1 22.1 19 21.2 19 20.1V19.1C19 18 18.1 17.1 17 17.1H12Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "CarSeatIcon",
  props: {
    title: {
      type: String,
      default: "Car Seat icon"
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
