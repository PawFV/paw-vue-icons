<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon movie-filter-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M18 4L20 7H17L15 4H13L15 7H12L10 4H8L10 7H7L5 4H4C2.9 4 2 4.9 2 6L2 18C2 19.1 2.9 20 4 20H20C21.1 20 22 19.1 22 18V4H18M11.25 15.25L10 18L8.75 15.25L6 14L8.75 12.75L10 10L11.25 12.75L14 14L11.25 15.25M16.94 11.94L16 14L15.06 11.94L13 11L15.06 10.06L16 8L16.94 10.06L19 11L16.94 11.94Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "MovieFilterIcon",
  props: {
    title: {
      type: String,
      default: "Movie Filter icon"
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
