<template>
  <div class="Worker">
    <h2 class="Worker-Heading">
      {{ $t('企業の皆様・はたらく皆様へ') }}
    </h2>
    <div v-for="(item, i) in items" :key="i">
      <TextCard
        :title="$t(item.title)"
        :link="item.link"
        :body="$t(item.body)"
      />
    </div>
  </div>
</template>

<i18n src="./worker.i18n.json"></i18n>

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
          title: '中小企業・小規模事業者の皆様へ',
          link:
            'https://www.pref.yamagata.jp/ou/bosai/020072/kochibou/coronavirus/coronavirus.html',
          body:
            '新型コロナウイルス感染症により事業活動に影響を受けている中小企業等を対象とした相談窓口です。'
        },
        {
          title: '旅行業者の皆様へ',
          link: 'http://www.mlit.go.jp/kankocho/topics06_000253.html',
          body: '観光庁サイトのページです'
        },
        {
          title: '建設業者の皆様へ',
          link:
            'https://www.pref.yamagata.jp/ou/bosai/020072/kochibou/coronavirus/coronavirus.html',
          body: '山形県の融資・保証・助成金の窓口です'
        }
      ]
    }
  },
  head() {
    return {
      title: '企業の皆様・はたらく皆様へ'
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
