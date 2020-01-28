<template>
  <header>
    <a href="#" v-scroll-to="'#about'">About</a>
    <a href="#" v-scroll-to="'#sponsor'">Try</a>
    <a href="#" v-scroll-to="'#place'">Place</a>

  </header>
</template>

<script>
export default {
  name: 'MyHeader'
}
</script>

<style lang='scss' scoped>
@import '@/assets/styles/_color.scss';
@import '@/assets/styles/_size.scss';

header {
  width: 100%;
  text-align: center;
  background-color: white;
  box-shadow: 0 0 10px 0 rgba(0, 0, 0, 0.2);
  /* position: fixed; */
  top: 0;
  z-index: 10;
}

a {
  height: $header-height_pc;
  line-height: $header-height_pc;
  transition: all 0.3s;
  cursor: pointer;
  font-size: 18px;
  color: $text-color;
  text-decoration: none;
  width: 80px;
  display: inline-block;

  &:hover {
    background-color: darken(white, 5%);
  }

  &:link {
    color: $text-color;
  }
}
p {
  font-size: 18px;
}

.clear {
  clear: left;
}
/* タブレット */
@media (max-width: 1250px) {
  a {
    width: 30%;
    height: $header-height_tablet;
    line-height: $header-height_tablet;
  }
}

/* スマートフォン */
@media (max-width: 670px) {
  a {
    width: 20%;
    height: $header-height_sp;
    line-height: $header-height_sp;
  }
}
</style>
