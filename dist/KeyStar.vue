<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon key-star-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M6.5 3C4 3 2 5 2 7.5S4 12 6.5 12C8.46 12 10.13 10.75 10.74 9H15V12H18V9H22V6H10.74C10.13 4.25 8.46 3 6.5 3M6.5 6C7.33 6 8 6.67 8 7.5S7.33 9 6.5 9 5 8.33 5 7.5 5.67 6 6.5 6M12 14L10.87 16.64L8 16.89L10.18 18.77L9.5 21.58L12 20.09L14.45 21.58L13.8 18.77L16 16.89L13.11 16.64Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "KeyStarIcon",
  props: {
    title: {
      type: String,
      default: "Key Star icon"
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
