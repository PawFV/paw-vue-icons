<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon certificate-outline-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M13 21L15 20L17 21V14H13M17 9V7L15 8L13 7V9L11 10L13 11V13L15 12L17 13V11L19 10M20 3H4A2 2 0 0 0 2 5V15A2 2 0 0 0 4 17H11V15H4V5H20V15H19V17H20A2 2 0 0 0 22 15V5A2 2 0 0 0 20 3M11 8H5V6H11M9 11H5V9H9M11 14H5V12H11Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "CertificateOutlineIcon",
  props: {
    title: {
      type: String,
      default: "Certificate Outline icon"
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
