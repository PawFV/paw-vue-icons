<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon podium-gold-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M12,7.09L14.45,8.58L13.8,5.77L16,3.89L13.11,3.64L12,1L10.87,3.64L8,3.89L10.18,5.77L9.5,8.58L12,7.09M15,23H9V10H15V23M1,17V23H7V17H1M5,21H3V19H5V21M17,13V23H23V13H17M21,21H19V15H21V21Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "PodiumGoldIcon",
  props: {
    title: {
      type: String,
      default: "Podium Gold icon"
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
