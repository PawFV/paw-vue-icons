<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon tilde-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M2,15C2,15 2,9 8,9C12,9 12.5,12.5 15.5,12.5C19.5,12.5 19.5,9 19.5,9H22C22,9 22,15 16,15C12,15 10.5,11.5 8.5,11.5C4.5,11.5 4.5,15 4.5,15H2">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "TildeIcon",
  props: {
    title: {
      type: String,
      default: "Tilde icon"
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
