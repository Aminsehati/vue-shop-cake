<template>
  <div class="banner-wrapper">
    <div class="banner-content position-relative">
      <div class="banner-content-right">
        <h2 class="text-right font-25 text-white">
          بهترین محصولات کیک و شیرینی خود را در فروشگاه ما دنبال کنید
        </h2>
        <div class="text-right w-100 mt-20">
          <Button priamry lg> همین حالا خرید کنید </Button>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import "./style.css";
import Button from "../Button/index.vue";
export default {
  components: { Button },
};
</script>