<template>
  <div class="product-item">
    <div class="image text-center">
      <img :src="productInfo.image" class="mx-auto" />
    </div>
    <div class="content mt-15">
      <div class="text-center font-16">
        <span class="title font-700">
          {{ productInfo.title }}
        </span>
        <span class="barcode">
          {{ productInfo.barCode }}
        </span>
      </div>
      <div class="category text-center">
        دسته بندی :
        {{ productInfo.category }}
      </div>
      <button>
        <span class="price"> 25.000.000 </span>
        <span class="title">
          <b-icon icon="plus-circle"></b-icon>
          خرید
        </span>
      </button>
    </div>
  </div>
</template>

<script>
import "./style.css";
export default {
  props:{
    productInfo:{
      type:Object,
      default:()=>{}
    }
  },
};
</script>

<style>
</style>