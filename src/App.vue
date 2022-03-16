

<template>
 <div class="container">
    <my-virtual-scroller :items="list" />
  </div>
</template>
<script>
import myVirtualScroller from './components/virtualScoller.vue'
// 模拟一个长列表
const list = []
for(let i=0; i<10000; i++) {
  list.push({
    id: i,
    label: `virtual-list ${i}`
  })
}
export default {
  components: {
    myVirtualScroller
  },
  data() {
    return {
      list: list
    }
  }
}
</script>


<style>
.container {
  height: 1000px;
  border: 1px solid #ccc;
}
</style>
