<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon thermometer-plus-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M19 11V8H17V11H14V13H17V16H19V13H22V11M11 13V5C11 3.34 9.66 2 8 2S5 3.34 5 5V13C2.79 14.66 2.34 17.79 4 20S8.79 22.66 11 21 13.66 16.21 12 14C11.72 13.62 11.38 13.28 11 13M8 4C8.55 4 9 4.45 9 5V8H7V5C7 4.45 7.45 4 8 4Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "ThermometerPlusIcon",
  props: {
    title: {
      type: String,
      default: "Thermometer Plus icon"
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
