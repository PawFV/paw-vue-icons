<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon shield-search-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M12,9A3,3 0 0,1 15,12A3,3 0 0,1 12,15A3,3 0 0,1 9,12A3,3 0 0,1 12,9M17.86,19.31C16.23,21.22 14.28,22.45 12,23C9.44,22.39 7.3,20.93 5.58,18.63C3.86,16.34 3,13.8 3,11V5L12,1L21,5V11C21,13.39 20.36,15.61 19.08,17.67L16.17,14.76C16.69,13.97 17,13 17,12A5,5 0 0,0 12,7A5,5 0 0,0 7,12A5,5 0 0,0 12,17C13,17 13.97,16.69 14.76,16.17L17.86,19.31Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "ShieldSearchIcon",
  props: {
    title: {
      type: String,
      default: "Shield Search icon"
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
