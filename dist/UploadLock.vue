<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon upload-lock-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M22 22H17C16.5 22 16 21.5 16 21V17C16 16.5 16.5 16 17 16V14.5C17 13.1 18.1 12 19.5 12C20.9 12 22 13.1 22 14.5V16C22.5 16 23 16.5 23 17V21C23 21.5 22.5 22 22 22M14 20H5V18H14V20M21 16V14.5C21 13.7 20.3 13 19.5 13C18.7 13 18 13.7 18 14.5V16H21M15 16H9V10H5L12 3L19 10H15V16Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "UploadLockIcon",
  props: {
    title: {
      type: String,
      default: "Upload Lock icon"
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
