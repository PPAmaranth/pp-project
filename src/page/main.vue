<template>
  <div>
    <sd-top></sd-top>
    <sd-nav></sd-nav>
    <div class="sd-router">
      <router-view/>
    </div>
    <sd-footer></sd-footer>
  </div>
  
</template>

<script>

import sdTop from '@/components/top'
import sdFooter from '@/components/footer'
import sdNav from '@/components/nav'
export default {
  name: 'home',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      visible: false 
    }
  },
  components: {
		sdTop,
    sdFooter,
    sdNav,
  }
}
</script>
<style>
.sd-router{
  
}
</style>