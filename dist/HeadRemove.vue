<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon head-remove-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M13 3C9.2 3 6.2 5.9 6 9.7L4.1 12.2C3.9 12.5 4.1 13 4.5 13H6V16C6 17.1 6.9 18 8 18H9V21H16V16.3C18.4 15.2 20 12.8 20 10C20 6.1 16.9 3 13 3M15.1 12.5L13 10.4L10.9 12.5L9.5 11.1L11.6 9L9.5 6.9L10.9 5.5L13 7.6L15.1 5.5L16.5 6.9L14.4 9L16.5 11.1L15.1 12.5Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "HeadRemoveIcon",
  props: {
    title: {
      type: String,
      default: "Head Remove icon"
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
