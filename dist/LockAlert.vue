<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon lock-alert-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M6 7C6 4.79 7.79 3 10 3C12.21 3 14 4.79 14 7V9H15C16.11 9 17 9.9 17 11V19C17 20.11 16.11 21 15 21H5C3.9 21 3 20.11 3 19V11C3 9.9 3.9 9 5 9H6V7M12 9V7C12 5.9 11.11 5 10 5C8.9 5 8 5.9 8 7V9H12M19 9H21V14H19V9M19 16H21V18H19V16M10 13C8.9 13 8 13.9 8 15C8 16.11 8.9 17 10 17C11.11 17 12 16.11 12 15C12 13.9 11.11 13 10 13Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "LockAlertIcon",
  props: {
    title: {
      type: String,
      default: "Lock Alert icon"
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
