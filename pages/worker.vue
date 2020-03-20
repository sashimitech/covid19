<template>
  <div class="Worker">
    <h2 class="Worker-Heading">
      事業者の皆さまへ
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
          title: '「新型コロナウイルス関連融資相談窓口」について',
          body:
            '<a href="https://www.pref.gifu.lg.jp/event-calendar/c11363/yushisoudanmadoguti.html" target="_blank" rel="noopener">https://www.pref.gifu.lg.jp/event-calendar/c11363/yushisoudanmadoguti.html</a><br />新型コロナウイルスの影響を受ける、またはその恐れがある中小企業者・小規模事業者の資金繰りなどの相談窓口を開設しました。'
        },
        {
          title: '「新型コロナウイルスに係る県中小企業資金融資制度の改正」について',
          body:
            '<a href="https://www.pref.gifu.lg.jp/event-calendar/c11363/yushiseidokaisei.html" target="_blank" rel="noopener">https://www.pref.gifu.lg.jp/event-calendar/c11363/yushiseidokaisei.html</a><br />新型コロナウイルスによる影響を受ける県内中小企業・小規模事業者の早期支援に向けて、岐阜県中小企業資金融資制度のうち、経済変動対策資金の要件を改正します。'
        },
        {
          title: '「新型コロナウイルス感染症に伴うセーフティネット保証４号の実施」について',
          body:
            '<a href="https://www.pref.gifu.lg.jp/event-calendar/c11363/koronauirusu.html" target="_blank" rel="noopener">https://www.pref.gifu.lg.jp/event-calendar/c11363/koronauirusu.html</a><br />売上高が減少している中小企業・小規模事業者の資金繰り支援措置として、信用保証協会が一般保証と別枠で融資額の１００％を保証する制度が始まりました。'
        },
        {
          title: '「新型コロナウイルス感染症関連：経済産業省の支援策」について',
          body:
            '<a href="https://www.meti.go.jp/covid-19/" target="_blank" rel="noopener">https://www.meti.go.jp/covid-19/</a> <br />新型コロナウイルスによる企業への影響を緩和し、企業を支援するための施策をご案内します。'
        },
        {
          title: '県制度融資「新型コロナウイルス感染症対策資金」の新設と運用開始',
          body:
            '<a href="https://www.pref.gifu.lg.jp/event-calendar/c11363/saigaitaisaku.html" target="_blank" rel="noopener">https://www.pref.gifu.lg.jp/event-calendar/c11363/saigaitaisaku.html</a><br />新型コロナウイルス感染症の影響により売上等が減少している中小企業者の資金繰りを支援するため、新たに「新型コロナウイルス感染症対策資金」を設置し、３月５日から運用を開始します。'
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
.Worker {
  &-Heading {
    @include font-size(30);
    font-weight: normal;
    color: $gray-2;
    margin-bottom: 12px;
  }
}
</style>
