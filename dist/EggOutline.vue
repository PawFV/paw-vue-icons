<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon egg-outline-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M12 4C14.32 4 17.5 10.7 17.5 14.5C17.5 17.53 15.03 20 12 20S6.5 17.53 6.5 14.5C6.5 10.7 9.68 4 12 4M12 2C7.86 2 4.5 10.36 4.5 14.5C4.5 18.64 7.86 22 12 22S19.5 18.64 19.5 14.5C19.5 10.36 16.14 2 12 2Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "EggOutlineIcon",
  props: {
    title: {
      type: String,
      default: "Egg Outline icon"
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
