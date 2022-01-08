<template>
  <header class="header">
    <div class="container">
      <div class="logo__area">
        <img :src="logo" />
      </div>
      <div class="left__">
        <ul class="navabar__wrapper">
          <li v-for="navbar in navbarItems" :key="navbar.id">
              <router-link :to="navbar.path" exact-active-class="active">
                  {{ navbar.name }}
              </router-link>
          </li>
        </ul>
        <div class="cart">
          <span>
            <img :src="cartIcon"/>
          </span>
          <p class="font-600">
            کارت
          </p>
        </div>
        <div class="user">
          <span>
            <img :src="userAccountIcon"/>
          </span>
          <p class="mb-0 font-600">
            صفحه کاربری
          </p>
        </div>  
      </div>
    </div>
  </header>
</template>
<script>
import "./style.css";
export default {
  data() {
    return {
      logo: require("../../assets/image/logo.svg"),
      cartIcon: require("../../assets/icon/cart.svg"),
      userAccountIcon:require("../../assets/icon/account.svg"),
      navbarItems: [
        {
          id: 1,
          name: "صفحه اصلی",
          path: "/",
        },
        {
          id: 2,
          name: "اطراف من",
          path: "/1",
        },
        {
          id: 3,
          name: "همگردی",
          path: "/2",
        },
        {
          id: 4,
          name: "همبودشو",
          path: "/3",
        },
        {
          id: 5,
          name: "ژورنال",
          path: "/4",
        },
        {
          id: 5,
          name: "کسب و کارها",
          path: "/5",
        },
      ],
    };
  },
};
</script>