<template>
  <footer class="footer">
    <div class="container">
      <div class="top">
        <div class="footer-about">
          <div class="logo">
            <img :src="logo" class="mx-auto" />
          </div>
          <p>این متن تست است</p>
        </div>
        <div
          class="footer-item"
          v-for="footerItem in footerItems"
          :key="footerItem.id"
        >
          <h4 class="text-center">
            {{ footerItem.name }}
          </h4>
          <div
            v-for="item in footerItem.items"
            :key="item.id"
            class="text-right footer-sub-item"
          >
            <span class="block w-100 text-right">
              {{ item.name }}
            </span>
          </div>
        </div>
        <div class="footer-social">
          <h4 class="text-center">شبکه های اجتماعی</h4>
          <div class="text-center">
            <a
              :href="item.link"
              v-for="item in socialItems"
              :key="item.id"
              target="_blank"
            >
              <img :src="item.icon" />
            </a>
          </div>
        </div>
      </div>
      <div class="bottom">
        <p class="mb-0 text-center">copyright @shop 2022. All rights reserved.</p>
      </div>
    </div>
  </footer>
</template>
<script>
import "./style.css";
export default {
  data() {
    return {
      logo: require("../../assets/image/logo.svg"),
      footerItems: [
        {
          id: 1,
          name: "لینک سریع",
          items: [
            {
              id: "12",
              name: "لینک سریع",
            },
            {
              id: "13",
              name: "لینک سریع",
            },
            {
              id: "14",
              name: "لینک سریع",
            },
            {
              id: "15",
              name: "لینک سریع",
            },
          ],
        },
        {
          id: 2,
          name: "لینک سریع",
          items: [
            {
              id: "22",
              name: "لینک سریع",
            },
            {
              id: "23",
              name: "لینک سریع",
            },
            {
              id: "24",
              name: "لینک سریع",
            },
            {
              id: "25",
              name: "لینک سریع",
            },
          ],
        },
        {
          id: 3,
          name: "لینک سریع",
          items: [
            {
              id: "32",
              name: "لینک سریع",
            },
            {
              id: "33",
              name: "لینک سریع",
            },
            {
              id: "34",
              name: "لینک سریع",
            },
            {
              id: "35",
              name: "لینک سریع",
            },
          ],
        },
      ],
      socialItems: [
        {
          id: 1,
          icon: require("../../assets/icon/twittericon.svg"),
          link: "https://twitter.com/",
        },
        {
          id: 2,
          icon: require("../../assets/icon/whatsappIcon.svg"),
          link: "https://web.whatsapp.com/",
        },
        {
          id: 3,
          icon: require("../../assets/icon/instagramIcon.svg"),
          link: "https://www.instagram.com/accounts/login/",
        },
      ],
    };
  },
};
</script>