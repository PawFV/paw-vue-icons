<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon syllabary-hangul-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M8 4V6H4V8H6.39C5.55 8.74 5 9.8 5 11C5 13.2 6.8 15 9 15C11.2 15 13 13.2 13 11C13 9.8 12.45 8.74 11.61 8H14V6H10V4M15 4V16H17V11H20V9H17V4M9 9C10.12 9 11 9.88 11 11C11 12.12 10.12 13 9 13C7.88 13 7 12.12 7 11C7 9.88 7.88 9 9 9M7 16V20H17V18H9V16Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "SyllabaryHangulIcon",
  props: {
    title: {
      type: String,
      default: "Syllabary Hangul icon"
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
