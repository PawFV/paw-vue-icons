<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon seat-flat-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M22,11V13H9V7H18A4,4 0 0,1 22,11M2,14V16H8V18H16V16H22V14M7.14,12.1C8.3,10.91 8.28,9 7.1,7.86C5.91,6.7 4,6.72 2.86,7.9C1.7,9.09 1.72,11 2.9,12.14C4.09,13.3 6,13.28 7.14,12.1Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "SeatFlatIcon",
  props: {
    title: {
      type: String,
      default: "Seat Flat icon"
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
