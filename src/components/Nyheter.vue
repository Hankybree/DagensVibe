<template>
  <div class="content">
    <div class="articles" v-for="(article, index) in $store.state.articles" :key="index">
      <div v-if="article.type === 'article'">
        <img :src="article.img" :alt="article.img">
        <h2>{{ article.header }}</h2>
        <div>
          <p class="ingress">{{ article.ingress }}</p>
          <p class="body">{{ article.body }}</p>
        </div>
      </div>
      <div v-else>
        <h2>{{ article.header }}</h2>
        <youtube :video-id="article.videoId" :player-width="youtubeWidth" :playerHeight="youtubeHeight"></youtube>
      </div>
      <div class="meta">
        <div class="author">{{ article.author }}</div>
        <div class="spacer"></div>
        <div class="date">{{ article.date }}</div>
      </div>
    </div>
    <!-- <youtube video-id="_J86LFuYXMc"></youtube>
    <input type="button" @click="showData()" value="Logga data"> -->
  </div>
</template>

<script>
export default {
  name: 'Nyheter',
  computed: {
    youtubeWidth: {
      get() {
        if(screen.width >= 700) {
          return 640
        }
        return 240
      }
    },
    youtubeHeight: {
      get() {
        if(screen.width >= 700) {
          return 360
        }
        return 135
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.articles {
  border-left: solid 1px #2c3e50;
  border-right: solid 1px #2c3e50;
  border-bottom: solid 1px #2c3e50;
  display: inline-block;
  width: 100%;
}
.ingress {
  font-weight: bold;
}
.meta {
  display: flex;
  font-size: 12px;
}
.spacer {
  flex-grow: 1;
}
.author {
  text-align: left;
  margin-left: 1vw;
}
.date {
  text-align: right;
  margin-right: 1vw;
}
@media (orientation: landscape) {
  .articles {
    width: 52vw;
  }
}
@media (orientation: landscape) and (min-width: 700px) {
  .articles {
    width: 700px;
  }
}
</style>
