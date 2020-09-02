<template>
  <div class="q-pa-md">
      <div class="row">
          <div class="col-6 col-md-6 col-xs-12">
            <q-img
            transition="jump-up"
            src="https://cdn.pixabay.com/photo/2018/06/08/00/48/developer-3461405_960_720.png"
            style="width: 100%;height:45vh"
            >
            <div class="absolute-bottom text-subtitle1 text-center text-bold">
                skill
            </div>
            </q-img>
          </div>
          <div class="col-6 col-md-6 col-xs-12">
              <div class="q-ma-md text-grey-4">
                  <h4><u>{{ title }}</u></h4>
              </div>
              <div class="q-ma-md text-grey-10 text-bold">
                  <p>{{ lorem }}</p>
              </div>
          </div>
      </div>
      <div class='row q-pa-lg' >
        <div class="col-2 col-md-2 col-xs-6" :key="n" v-for="n in 6">
          <q-card class="my-card text-center">
            <q-circular-progress
              show-value
              font-size="10px"
              class="q-ma-md"
              :value="value"
              size="100px"
              :thickness="0.25"
              color="primary"
              track-color="grey-3"
            >
              <q-avatar size="60px">
                <img src="https://cdn.quasar.dev/logo/svg/quasar-logo.svg">
              </q-avatar>
            </q-circular-progress>

            <q-card-actions class="justify-center">
              <q-btn flat class="">Quasar</q-btn>
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
      title: 'mes compétences,',
      value: 50,
      lorem: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Itaque voluptatem totam, architecto cupiditate officia rerum, error dignissimos praesentium libero ab nemo.'
    }
  }
}
</script>
