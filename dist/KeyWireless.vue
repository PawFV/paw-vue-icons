<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon key-wireless-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M4.93 5.92L6.34 7.33A8 8 0 0 1 17.66 7.33L19.07 5.92A10 10 0 0 0 4.93 5.92M7.76 8.75L9.17 10.16A4 4 0 0 1 14.83 10.16L16.24 8.75A6 6 0 0 0 7.76 8.75M10.76 15A4.5 4.5 0 1 0 10.76 18H15V21H18V18H22V15M6.5 18A1.5 1.5 0 1 1 8 16.5A1.5 1.5 0 0 1 6.5 18Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "KeyWirelessIcon",
  props: {
    title: {
      type: String,
      default: "Key Wireless icon"
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
