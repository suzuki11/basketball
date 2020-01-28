<template>
  <section id="place" class="about-wrapper">
    <pageTitle title="Place" />
    <!-- <img alt="Vue logo" src="../assets/place_1.png" class="image_1"> -->
  </section>
</template>

<script>
import pageTitle from '@/components/pageTitle'

export default {
  name: 'Place',
  components: {
    pageTitle
  },
  data() {
    return {

    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '@/assets/styles/_color.scss';
@import '@/assets/styles/_mixin.scss';


.about-wrapper {
  @include section;
}

.box-wrapper {
  @include box-wrapper;
  color: $text-color;

  table {
    text-align: left;
  }

  th {
    padding-right: 20px;
    font-weight: normal;
    color: $sub-text-color;
  }

  td {
    font-size: 20px;
    padding: 5px 8px 5px 0;
  }
}

a {
  text-decoration: none;
}

/*スマートフォン*/
@media (max-width: 670px) {
  .box-wrapper {
    td {
      display: block;
      font-size: 16px;
      width: 100%;
      padding: 5px 0;
      border-bottom: none;
    }
  }
  .image_1 {
  	width: 100%;
    height: 100%;
  }
}
</style>
