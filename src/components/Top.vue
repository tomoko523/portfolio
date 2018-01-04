<template>
  <div>
    <section>
      <v-parallax :src="imgUrl.topFirst" height="600">
        <v-layout
          column
          align-center
          justify-center
          class="white--text"
        >
          <h1 class="white--text mb-2 display-3 text-xl-center">Tomoko Hirata Portfolio</h1>
          <div class="subheading mb-3 text-xs-center">Since Jan. 5, 2018</div>
        </v-layout>
      </v-parallax>
    </section>

    <section>
      <v-layout
        column
        wrap
        class="my-5"
        align-center
      >
        <v-flex xs12 sm4 class="my-3">
          <div class="text-xs-center">
            <img v-bind:src="imgUrl.logo" width="100%" alt="logo">
          </div>
        </v-flex>
        <v-flex xs12>
          <v-container grid-list-xl>
            <v-layout row wrap align-center>
              <v-flex xs12 md4>
                <v-card class="elevation-0 transparent">
                  <v-card-text class="text-xs-center">
                    <v-icon x-large class="red--text text--lighten-2">mood</v-icon>
                  </v-card-text>
                  <v-card-title primary-title class="layout justify-center">
                    <div class="headline text-xs-center">わたしのこと</div>
                  </v-card-title>
                  <v-card-text>{{ message.aboutMe }}</v-card-text>
                </v-card>
              </v-flex>
              <v-flex xs12 md4>
                <v-card class="elevation-0 transparent">
                  <v-card-text class="text-xs-center">
                    <v-icon x-large class="red--text text--lighten-2">build</v-icon>
                  </v-card-text>
                  <v-card-title primary-title class="layout justify-center">
                    <div class="headline">できること</div>
                  </v-card-title>
                  <v-card-text>{{ message.skills }}</v-card-text>
                </v-card>
              </v-flex>
              <v-flex xs12 md4>
                <v-card class="elevation-0 transparent">
                  <v-card-text class="text-xs-center">
                    <v-icon x-large class="red--text text--lighten-2">favorite</v-icon>
                  </v-card-text>
                  <v-card-title primary-title class="layout justify-center">
                    <div class="headline text-xs-center">心がけていること</div>
                  </v-card-title>
                  <v-card-text>{{ message.mind }}</v-card-text>
                </v-card>
              </v-flex>
            </v-layout>
          </v-container>
        </v-flex>
      </v-layout>
    </section>

    <section>
      <v-parallax :src="imgUrl.topSecond" height="380">
        <v-layout column align-center justify-center>
          <div class="headline white--text mb-3 text-xs-center">I'll keep studying, and work with my best!</div>
            <v-btn class="red lighten-2 mt-5" dark large href="https://github.com/tomoko523/portfolio">
              View on Github this Site
            </v-btn>
        </v-layout>
      </v-parallax>
    </section>

    <section>
      <v-container grid-list-xl>
        <v-layout row wrap justify-center class="my-5">
          <v-flex xs12 sm4>
            <v-card class="elevation-0 transparent">
              <v-card-title primary-title class="layout justify-center">
                <div class="headline">このサイトについて</div>
              </v-card-title>
              <v-card-text>
                このサイトはProgressive Web Appに対応しています。
                Androidの方は「ホーム画面に追加」から保存すると、ショートカットからアプリのように起動できるようになります。
                <v-spacer></v-spacer>
                vue-cliの<a href="https://github.com/vuejs-templates/pwa" target="_blank">pwa template</a>と
                vuetifyの<a href="https://github.com/vuetifyjs/parallax-starter" target="_blank">parallax template</a>を使用しています。
              </v-card-text>
            </v-card>
          </v-flex>
          <v-flex xs12 sm4 offset-sm1>
            <v-card class="elevation-0 transparent">
              <v-card-title primary-title class="layout justify-center">
                <div class="headline">外部リンク</div>
              </v-card-title>
              <v-list class="transparent">
                <v-list-tile>
                  <v-list-tile-action>
                    <v-icon class="red--text text--lighten-2">fa-github</v-icon>
                  </v-list-tile-action>
                  <v-list-tile-content>
                    <v-list-tile-title><a href="https://github.com/tomoko523" target="_blank">tomoko523</a></v-list-tile-title>
                  </v-list-tile-content>
                </v-list-tile>
                <v-list-tile>
                  <v-list-tile-action>
                    <v-icon class="red--text text--lighten-2">fa-facebook</v-icon>
                  </v-list-tile-action>
                  <v-list-tile-content>
                    <v-list-tile-title>
                      <a href="https://www.facebook.com/hirata.tomoko" target="_blank">hirata.tomoko</a>
                    </v-list-tile-title>
                  </v-list-tile-content>
                </v-list-tile>
                <v-list-tile>
                  <v-list-tile-action>
                    <v-icon class="red--text text--lighten-2">fa-medium</v-icon>
                  </v-list-tile-action>
                  <v-list-tile-content>
                    <v-list-tile-title>準備中...</v-list-tile-title>
                  </v-list-tile-content>
                </v-list-tile>
              </v-list>
            </v-card>
          </v-flex>
        </v-layout>
      </v-container>
    </section>
  </div>
</template>

<script>
import MESSAGE from '@/data/topMessage'
import IMGURL from '@/data/imgUrl'

export default {
  name: 'top',
  data () {
    return {
      message: MESSAGE,
      imgUrl: IMGURL
    }
  }
}
</script>
