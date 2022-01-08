<template>
  <div class="category-item">
      <img :src="categoryInfo.icon"/>
      <h2 class="font-16 text-center font-600">
          {{
              categoryInfo.title
          }}
      </h2>
  </div>
</template>
<script>
import './style.css'
export default {
    props:{
        categoryInfo:{
            type:Object,
            default:()=>{}
        }
    }
}
</script>