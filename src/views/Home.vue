<template>
  <div class="home">
    <b-container>
      <Category />
      <div class="filters-product">
        <div class="right___">
          <h5>انتخاب دسته بندی</h5>
          <SelectBox class="selectbox-product" />
        </div>
        <div class="left__">
          <TextField placeholder="جستجو">
            <span slot="icon" class="icon">
              <img :src="searchIcon" />
            </span>
          </TextField>
        </div>
      </div>
      <div class="products">
        <h2 class="text-center font-22 mb-50">خرید محصولات پر فروش</h2>
        <carousel
          :items="4"
          :margin="15"
          :dots="false"
          :navText="navText"
          ref="carousel"
          :responsive="respansiveOwlCarousel"
        >
          <div v-for="item in productsItems" :key="item.id">
            <Product :productInfo="item" />
          </div>
        </carousel>
      </div>
      <Banner class="mt-40" />
      <div class="bar-social">
        <span class="d-block">
          <b-icon icon="instagram"></b-icon>
        </span>
        <span class="d-block">
          <b-icon icon="facebook"></b-icon>
        </span>
        <span class="d-block">
          <b-icon icon="twitter"></b-icon>
        </span>
        <span class="d-block">
          <b-icon icon="linkedin"></b-icon>
        </span>
      </div>
    </b-container>
  </div>
</template>

<script>
import "./style.css";
import Product from "../components/product";
import Banner from "../components/Banner";
import Category from "../components/Catgeory";
import carousel from "vue-owl-carousel";
import TextField from "../components/TextField/index.vue";
import SelectBox from "../components/SelectBox/index.vue";
export default {
  name: "Home",
  components: {
    Product,
    carousel,
    Banner,
    Category,
    TextField,
    SelectBox,
  },
  data() {
    return {
      respansiveOwlCarousel: {
        0: {
          items: 1,
        },
        400: {
          items: 2,
        },
        600: {
          items: 3,
        },
        1200: {
          items: 4,
        },
      },
      searchIcon: require("../assets/icon/searchIcon.svg"),
      productsItems: [
        {
          image: require("../assets/image/product.png"),
          title: "کیک شکلاتی",
          barCode: "#65232",
          category: "کیک",
        },
        {
          image: require("../assets/image/product.png"),
          title: "کیک شکلاتی",
          barCode: "#65232",
          category: "کیک",
        },
        {
          image: require("../assets/image/product.png"),
          title: "کیک شکلاتی",
          barCode: "#65232",
          category: "کیک",
        },
        {
          image: require("../assets/image/product.png"),
          title: "کیک شکلاتی",
          barCode: "#65232",
          category: "کیک",
        },
        {
          image: require("../assets/image/product.png"),
          title: "کیک شکلاتی",
          barCode: "#65232",
          category: "کیک",
        },
        {
          image: require("../assets/image/product.png"),
          title: "کیک شکلاتی",
          barCode: "#65232",
          category: "کیک",
        },
        {
          image: require("../assets/image/product.png"),
          title: "کیک شکلاتی",
          barCode: "#65232",
          category: "کیک",
        },
      ],
    };
  },
  computed: {
    navText() {
      const first = `<svg viewBox="0 0 16 16" width="1em" height="1em" focusable="false" role="img" aria-label="chevron left" xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="bi-chevron-left mx-auto b-icon bi" data-v-41be6633=""><g data-v-41be6633=""><path fill-rule="evenodd" d="M11.354 1.646a.5.5 0 0 1 0 .708L5.707 8l5.647 5.646a.5.5 0 0 1-.708.708l-6-6a.5.5 0 0 1 0-.708l6-6a.5.5 0 0 1 .708 0z"></path></g></svg>`;
      const last = `<svg viewBox="0 0 16 16" width="1em" height="1em" focusable="false" role="img" aria-label="chevron right" xmlns="http://www.w3.org/2000/svg" fill="currentColor" class="bi-chevron-right mx-auto b-icon bi" data-v-41be6633=""><g data-v-41be6633=""><path fill-rule="evenodd" d="M4.646 1.646a.5.5 0 0 1 .708 0l6 6a.5.5 0 0 1 0 .708l-6 6a.5.5 0 0 1-.708-.708L10.293 8 4.646 2.354a.5.5 0 0 1 0-.708z"></path></g></svg>`;
      return [first, last];
    },
  },
};
</script>
