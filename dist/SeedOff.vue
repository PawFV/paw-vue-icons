<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon seed-off-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M22.1 21.5L2.4 1.7L1.1 3L5.9 7.8C3.8 10.5 2.6 14.6 3.2 20.8C4.3 20.9 5.4 21 6.4 21C10.9 21 14.1 19.9 16.3 18.2L20.9 22.8L22.1 21.5M7 17C7 17 7 13.7 8.9 10.8L10.2 12.1C9.1 13.4 8 15 7 17M11.6 8.4L8.5 5.3C11.3 3.4 14.7 3 17.2 3C19.3 3 20.7 3.3 20.7 3.3S22.1 10.3 18.7 15.5L12.8 9.6C15.1 7.6 17 7 17 7C14.7 7 12.9 7.5 11.6 8.4Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "SeedOffIcon",
  props: {
    title: {
      type: String,
      default: "Seed Off icon"
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
