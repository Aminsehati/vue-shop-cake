<template>
  <button :class="clesses">
    <slot />
  </button>
</template>
<script>
import './style.css'
export default {
    props:{
        priamry:{
            type:Boolean,
            default:false,
        },
        lg:{
            type:Boolean,
            default:false,
        }
    },
    computed:{
        clesses(){
            return {
                'btn btn__primary':this.priamry,
                'btn-lg':this.lg,
            }
        }
    }
}
</script>