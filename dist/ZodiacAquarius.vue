<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon zodiac-aquarius-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M15,12.41L12,9.41L9,12.41L6,9.41L3.71,11.71L2.29,10.29L6,6.59L9,9.59L12,6.59L15,9.59L18,6.59L21.71,10.29L20.29,11.71L18,9.41L15,12.41M18,15.41L20.29,17.71L21.71,16.29L18,12.59L15,15.59L12,12.59L9,15.59L6,12.59L2.29,16.29L3.71,17.71L6,15.41L9,18.41L12,15.41L15,18.41L18,15.41Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "ZodiacAquariusIcon",
  props: {
    title: {
      type: String,
      default: "Zodiac Aquarius icon"
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
