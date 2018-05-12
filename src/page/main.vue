<template>
  <div>
    <sd-top></sd-top>
    <sd-nav></sd-nav>
    <div :is="nowcomponent"></div>
    <sd-footer></sd-footer>
  </div>
  
</template>

<script>

import sdTop from '@/components/top'
import sdFooter from '@/components/footer'
import sdNav from '@/components/nav'
import erpmain from '@/page/erpmain'
import cgdd from '@/page/cgdd'
import cgkd from '@/page/cgkd'
import xskd from '@/page/xskd'
import xsdd from '@/page/xsdd'
export default {
  name: 'home',
  data () {
    return {
      nowcomponent:'erpmain',
    }
  },
  components: {
		sdTop,
    sdFooter,
    sdNav,
    erpmain,
    cgdd,
    cgkd,
    xskd,
    xsdd,
  }
}
</script>
<style>
</style>