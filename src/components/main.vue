<template>
	<top></top>
</template>

<script>

import top from '@/components/top'
export default {
  name: 'main',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      visible: false 
    }
  },
  components: {
		top
	}
}
</script>