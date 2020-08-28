<template>
  <div class="q-pa-md">
      <div class="row">
          <div class="col-6">
            <q-img
            src="https://cdn.quasar.dev/img/parallax2.jpg"
            style="width: 100%;height:80%"
            >
            <div class="absolute-bottom text-subtitle1 text-center">
                Caption
            </div>
            </q-img>
          </div>
          <div class="col-6">
              <div class="q-ma-md">
                  <h4>{{ title }}</h4>
              </div>
              <div class="q-ma-md">
                  <p>{{ lorem }}</p>
              </div>
          </div>
      </div>
      <div class='row q-pa-lg' >
        <div class="col-3 q-pa-md" :key="n" v-for="n in 8">
          <q-card  s="my-card">
            <q-img src="https://cdn.quasar.dev/img/parallax2.jpg">
              <div class="absolute-bottom">
                <div class="text-h6">Our Changing Planet</div>
                <div class="text-subtitle2">by John Doe</div>
              </div>
            </q-img>

            <q-card-actions>
              <q-btn flat>Action 1</q-btn>
              <q-btn flat>Action 2</q-btn>
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
      lorem: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Itaque voluptatem totam, architecto cupiditate officia rerum, error dignissimos praesentium libero ab nemo.'
    }
  }
}
</script>
