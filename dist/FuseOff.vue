<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon fuse-off-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M15 11.8L10.2 7H15V11.8M16 6V2C16 1.45 15.55 1 15 1H8C7.45 1 7 1.45 7 2V3.8L9.2 6H16M2.39 1.73L1.11 3L8 9.89V17H15.11L20.84 22.73L22.11 21.46L2.39 1.73M7 22C7 22.55 7.45 23 8 23H15C15.55 23 16 22.55 16 22V18H7V22Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "FuseOffIcon",
  props: {
    title: {
      type: String,
      default: "Fuse Off icon"
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
