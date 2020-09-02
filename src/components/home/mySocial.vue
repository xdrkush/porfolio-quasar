<template>
  <div class="q-pa-md">
      <div class="row">
          <div class="col-6 col-xs-12">
            <q-img
            transition="scale"
            src="https://www.tmncorp.com/wp-content/uploads/2016/06/social_media_marketing.washington.dc_.marketing.firm_.png"
            style="width: 100%;height:45vh"
            >
            <div class="absolute-bottom text-subtitle1 text-center text-bold">
                Rejoignez-moi
            </div>
            </q-img>
          </div>
          <div class="col-6 col-xs-12">
              <div class="q-ma-md text-grey-4">
                  <h4><u>{{ title }}</u></h4>
              </div>
              <div class="q-ma-md text-grey-10 text-bold">
                  <p>{{ lorem }}</p>
              </div>
          </div>
      </div>
      <div class='row q-pa-lg justify-evenly' >
        <div class="col-3 col-md-3 col-lg-2 col-sm-4 col-xs-6"
          :key="soc" v-for="soc in social"
        >
          <q-card  class="my-card">
            <q-img :src="soc.img" height="30vh">
              <div class="absolute-bottom">
                <div class="text-h6">{{ soc.name }}</div>
              </div>
            </q-img>

            <q-card-actions>
              <q-btn type="a" :href='soc.link' target="_blank" flat><q-icon class="q-ma-xs" name="visibility"/>View</q-btn>
              <q-btn flat><q-icon class="q-ma-xs" name="person_add_alt_1"/>Follow</q-btn>
            </q-card-actions>
          </q-card>
        </div>
      </div>

  </div>
</template>

<script>
export default {
  data () {
    return {
      title: 'mes réseaux ,',
      lorem: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Itaque voluptatem totam, architecto cupiditate officia rerum, error dignissimos praesentium libero ab nemo.',
      social: [
        {
          name: 'Twitter',
          link: 'https://twitter.com/',
          img: 'https://upload.wikimedia.org/wikipedia/fr/thumb/c/c8/Twitter_Bird.svg/738px-Twitter_Bird.svg.png'
        },
        {
          name: 'Facebuk',
          link: 'https://mastodon.social/about',
          img: 'https://pngimg.com/uploads/telegram/telegram_PNG19.png'
        },
        {
          name: 'Framasphere',
          link: 'https://framasphere.org/',
          img: 'data:image/png;base64,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'
        },
        {
          name: 'Mastodon',
          link: 'https://mastodon.social/about',
          img: 'https://upload.wikimedia.org/wikipedia/commons/thumb/4/48/Mastodon_Logotype_%28Simple%29.svg/953px-Mastodon_Logotype_%28Simple%29.svg.png'
        },
        {
          name: 'Linkedin',
          link: 'https://fr.linkedin.com/',
          img: 'data:image/png;base64,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'
        }
      ]
    }
  }
}
</script>
