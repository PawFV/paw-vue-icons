<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon oar-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M20.23,15.21C18.77,13.75 14.97,10.2 12.77,11.27L4.5,3L3,4.5L11.28,12.79C10.3,15 13.88,18.62 15.35,20.08C17.11,21.84 18.26,20.92 19.61,19.57C21.1,18.08 21.61,16.61 20.23,15.21Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "OarIcon",
  props: {
    title: {
      type: String,
      default: "Oar icon"
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
