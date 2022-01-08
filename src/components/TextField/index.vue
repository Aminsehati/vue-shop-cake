<template>
  <div class="form__group">
    <input
      :type="type"
      class="form__control"
      :placeholder="placeholder"
      :value="value"
      @change="updateValue($event)"
    />
    <slot name="icon"/>
  </div>
</template>
<script>
import './style.css'
export default {
  props: {
    type: {
      type: String,
      default: "text",
    },
    placeholder: {
      type: String,
      default: "",
    },
    value:{
        type:String,
        default:""
    }
  },
};
</script>