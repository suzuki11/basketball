<template>
  <section id="sponsor" class="about-wrapper">
    <pageTitle title="Sponsor" />
    <div class="box-wrapper">
      <table>
        <tbody>
          <tr v-for="(contact, index) in contacts" :key="index">
            <th>{{ contact.key }}</th>
            <td v-if="contact.url" class="last-td">
              <a :href="contact.url" target="_blank" rel="noopener noreferrer">
                {{ contact.value }}
              </a>
            </td>
            <td v-else class="last-td">
              {{ contact.value }}
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </section>
</template>

<script>
import pageTitle from '@/components/pageTitle'

export default {
  name: 'Sponsor',
  components: {
    pageTitle
  },
  data() {
    return {
      contacts: [
        { key: 'Gold', value: '京都信用金庫', url: '' },
        { key: 'Silver', value: 'softdevice', url: '' },
        {
          key: 'Partner',
          value: '紫野高校',
          url: ''
        }
      ]
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
}
</style>
