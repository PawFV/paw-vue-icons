<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon billboard-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M20 22H18V17H20M6 22H4V17H6M23 4V13A2 2 0 0 1 21 15H3A2 2 0 0 1 1 13V4A2 2 0 0 1 3 2H21A2 2 0 0 1 23 4M21 4H3V13H21M20 6H15V8H20M18 9H15V11H18M14 11H4L6.73 7.36L8.73 10.09L9.46 9.55L8.2 7.82L9.91 5.55Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "BillboardIcon",
  props: {
    title: {
      type: String,
      default: "Billboard icon"
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
