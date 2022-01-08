<template>
  <div class="category-wrapper">
    <h2 class="text-center font-22 mb-25">دسته بندی محصولات</h2>
    <div class="category-content">
      <div class="category-content-wrapper">
        <div
          v-for="category in categoryItems"
          :key="category.id"
          class="category__item"
        >
          <CategoryItems :categoryInfo="category" />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import CategoryItems from "./Items";
import "./style.css";
export default {
  components: {
    CategoryItems,
  },
  data() {
    return {
      categoryItems: [
        {
          id: 1,
          title: "شیرینی",
           icon : require('../../assets/icon/cookies.svg')
        },
        {
          id: 2,
          title: "ساندویچ",
          icon : require('../../assets/icon/Sandwich.svg')
        },
        {
          id: 3,
          title: "نان",
           icon : require('../../assets/icon/bread.svg')
        },
        {
          id: 4,
          title: "کیک",
           icon : require('../../assets/icon/Cake.svg')
        },
      ],
    };
  },
};
</script>