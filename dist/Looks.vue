<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon looks-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M12,6A11,11 0 0,0 1,17H3C3,12.04 7.04,8 12,8C16.96,8 21,12.04 21,17H23A11,11 0 0,0 12,6M12,10C8.14,10 5,13.14 5,17H7A5,5 0 0,1 12,12A5,5 0 0,1 17,17H19C19,13.14 15.86,10 12,10Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "LooksIcon",
  props: {
    title: {
      type: String,
      default: "Looks icon"
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
