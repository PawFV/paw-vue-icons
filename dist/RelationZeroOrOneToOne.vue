<template functional>
  <div :aria-hidden="props.decorative"
        :aria-label="props.title"
        :class="[data.class, data.staticClass]"
        :style="{height: props.size + 'px', display: 'inline-block'}"
        class="material-design-icon relation-zero-or-one-to-one-icon"
        role="img"
        v-bind="data.attrs"
        v-on="listeners">
    <svg :fill="props.fillColor"
         class="material-design-icon__svg"
         :width="props.size"
         :height="props.size"
         viewBox="0 0 24 24">
      <path d="M19 15V13H17V15H13V7H9.79A2.5 2.5 0 0 0 5.21 7H5V5H3V7H2V9H3V11H5V9H5.21A2.5 2.5 0 0 0 9.79 9H11V17H17V19H19V17H22V15M7.5 9A1 1 0 1 1 8.5 8A1 1 0 0 1 7.5 9Z">
        <title>{{ props.title }}</title>
      </path>
    </svg>
  </div>
</template>

<script>
export default {
  name: "RelationZeroOrOneToOneIcon",
  props: {
    title: {
      type: String,
      default: "Relation Zero Or One To One icon"
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
