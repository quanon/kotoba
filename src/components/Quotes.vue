<template lang="pug">
  .quotes
    quote.quote(v-for="quote in quotes", :key="quote.id", :body="quote.body", :source="quote.source")
</template>

<script>
  import Quote from './Quote';

  export default {
    components: {
      Quote
    },
    data() {
      return {
        quotes: [
          {
            id: 1,
            body: '今冷やかに見過しているこの現在、一刻も早く去ってしまえばよいなどといらだたしく後押ししても追い払ってしまいたいこの現在が、かりにも我慢のなる程度のものならば、たとい日常平凡の現在であっても、それはあの神々しい過去のなかへ今まさに移りゆこうとしているのであって、神々しい過去のなかに繰りこまれた後には恒常不滅の光明に包まれて末ながく記憶にとどめられ、後日、ことに苦難にのぞんで、記憶がその帷をかかげるとき、切実な憧れの対象となって現われるのであろうということを、いつもいつも肝に銘じて、この現在に敬意を払うようにするがよかろう。',
            source: 'アルトゥール・ショーペンハウアー「幸福について―人生論―」より'
          },
          {
            id: 2,
            body: '人というものはあっけなく死んでしまうものだ。人の生命というのは君が考えているよりずっと脆いものなんだ。だから人は悔いの残らないように人と接するべきなんだ。公平に、できることなら誠実に。そういう努力をしないで、人が死んで簡単に泣いて後悔したりするような人間を僕は好まない。個人的に。',
            source: '村上春樹「ダンス・ダンス・ダンス」より'
          }
        ]
      };
    }
  };
</script>

<style lang="scss" scoped>
  .quotes {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .quote {
    margin: 2.0rem 0;
  }
</style>
