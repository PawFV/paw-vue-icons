<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon lava-lamp-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M10,3L8,16H16L14,3H10M11.5,5.75A0.75,0.75 0 0,1 12.25,6.5A0.75,0.75 0 0,1 11.5,7.25A0.75,0.75 0 0,1 10.75,6.5A0.75,0.75 0 0,1 11.5,5.75M12.5,8.5A1,1 0 0,1 13.5,9.5A1,1 0 0,1 12.5,10.5A1,1 0 0,1 11.5,9.5A1,1 0 0,1 12.5,8.5M11.5,12A1.5,1.5 0 0,1 13,13.5A1.5,1.5 0 0,1 11.5,15A1.5,1.5 0 0,1 10,13.5A1.5,1.5 0 0,1 11.5,12M8,17L10,19L8,21H16L14,19L16,17H8Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "LavaLampIcon",
  props: {
    title: {
      type: String,
      default: "Lava Lamp icon"
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
