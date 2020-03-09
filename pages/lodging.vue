<template>
  <div class="Lodging">
    <h2 class="Lodging-Heading">
      宿泊事業者の皆さまへ
    </h2>
    <div v-for="(item, i) in items" :key="i">
      <TextCard :title="item.title" :body="item.body" />
    </div>
  </div>
</template>
<script lang="ts">
import TextCard from '@/components/TextCard.vue'
export default {
  components: {
    TextCard
  },
  data() {
    return {
      items: [
        {
          title: '宿泊施設における新型コロナウイルス感染症への対応',
          body:
            '宿泊施設における新型コロナウイルス感染症への対応は、下記をご確認ください。<br><a href="https://www.pref.gifu.lg.jp/kurashi/dobutsu/seikatsu-eisei/11222/ryokan_shingata_corona.html" target="_blank" rel="noopener">・旅館業法による宿泊施設（旅館、ホテル）</a><br /><a href="https://www.pref.gifu.lg.jp/kurashi/dobutsu/seikatsu-eisei/11222/portal.html" target="_blank" rel="noopener">・住宅宿泊事業法による宿泊施設（民泊）</a>'
        }
      ]
    }
  },
  head() {
    return {
      title: '事業者の皆さまへ'
    }
  }
}
</script>
<style lang="scss">
.Lodging {
  &-Heading {
    @include font-size(30);
    font-weight: normal;
    color: $gray-2;
    margin-bottom: 12px;
  }
}
a {
  @include text-link();
}
</style>
