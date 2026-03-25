<!-- stack-sticky 在 Vue 中的示例 -->
<template>
  <div class="stack-sticky">
    <h1 class="position-sticky">Header 1</h1>
    <div class="placeholder">Content 1</div>
    <h1 class="position-sticky">Header 2</h1>
    <div class="placeholder">Content 2</div>
    <h1 class="position-sticky">Header 3</h1>
    <div class="placeholder">Content 3</div>
    <h1 class="position-sticky">Header 4</h1>
    <div class="placeholder">Content 4</div>
  </div>
</template>

<script>
import { stackSticky } from 'stack-sticky'

export default {
  name: 'StackSticky',
  mounted() {
    stackSticky()
  }
}
</script>

<style lang="scss" scoped>
.stack-sticky {
  display: flex;
  flex-direction: column;
  gap: 10px;
  padding: 20px;

  .position-sticky {
    position: sticky;
    background-color: #fff;
    padding: 10px;
    border: 1px solid #ddd;
    border-radius: 8px;
    z-index: 10;
  }

  .placeholder {
    height: 200px;
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: #f5f5f5;
    margin-top: 10px;
    border: 1px dashed #bbb;
    color: #999;
    border-radius: 8px;
  }
}
</style>
