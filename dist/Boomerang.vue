<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon boomerang-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M10 2H4C2.9 2 2 2.9 2 4S2.9 6 4 6H8L10 2M18 2C20.2 2 22 3.8 22 6V12L18 14C18 9.6 14.4 6 10 6L12 2H18M18 20V16L22 14V20C22 21.1 21.1 22 20 22S18 21.1 18 20Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "BoomerangIcon",
  props: {
    title: {
      type: String,
      default: "Boomerang icon"
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
