<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon roller-skate-off-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M20.84 22.73L18.73 20.62C18.32 21.43 17.5 22 16.5 22C15.12 22 14 20.88 14 19.5C14 18.5 14.57 17.68 15.38 17.27L14.11 16H4V5.89L1.11 3L2.39 1.73L22.11 21.46L20.84 22.73M19 15C19 10 14 10 14 10H13.2L18.72 15.5C19 15.27 19 15 19 15M11.64 7.5L11.43 6H9.24V4.5H11.21L11 3H6.2L10.7 7.5H11.64M6.5 17C5.12 17 4 18.12 4 19.5S5.12 22 6.5 22 9 20.88 9 19.5 7.88 17 6.5 17Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "RollerSkateOffIcon",
  props: {
    title: {
      type: String,
      default: "Roller Skate Off icon"
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
