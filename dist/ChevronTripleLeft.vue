<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon chevron-triple-left-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M9.42,7.41L4.83,12L9.42,16.59L8,18L2,12L8,6L9.42,7.41M15.42,7.41L10.83,12L15.42,16.59L14,18L8,12L14,6L15.42,7.41M21.42,7.41L16.83,12L21.42,16.59L20,18L14,12L20,6L21.42,7.41Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "ChevronTripleLeftIcon",
  props: {
    title: {
      type: String,
      default: "Chevron Triple Left icon"
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
