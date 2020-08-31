<template>
  <div class="q-pa-md">
      <div class="row">
          <div class="col">
            <q-img
            src="https://cdn.quasar.dev/img/parallax1.jpg"
            style="width: 100%;height:45vh"
            >
            <div class="absolute-bottom text-subtitle1 text-center text-bold">
                Caption
            </div>
            </q-img>
          </div>
          <div class="col text-center">
              <div class="q-ma-md">
                  <h4>{{ title }}</h4>
              </div>
              <div class="q-ma-md">
                  <p>{{ lorem }}</p>
              </div>
          </div>
      </div>
      <div class='row'>
          <div class="col text-center">
              <div class="q-ma-md">
                  <h4>{{ title }}</h4>
              </div>
              <div class="q-ma-md">
                  <p>{{ lorem }}</p>
              </div>
          </div>
          <div class="col">
            <q-img
            src="https://cdn.quasar.dev/img/parallax2.jpg"
            style="width: 100%;height:45vh"
            >
            <div class="absolute-bottom text-subtitle1 text-center">
                Caption
            </div>
            </q-img>
          </div>
      </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      title: 'Présentation',
      lorem: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Itaque voluptatem totam, architecto cupiditate officia rerum, error dignissimos praesentium libero ab nemo.'
    }
  }
}
</script>
