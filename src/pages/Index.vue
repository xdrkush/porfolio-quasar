<template>
  <q-page class="flex flex-center">
    <div class="row">
      <div class="col-12">
        <Header />
      </div>
      <div class="col-12">
        <Presentation />
      </div>
    </div>
  </q-page>
</template>

<script>
import Header from '../components/header'
import Presentation from '../components/home/myPresentation'

export default {
  name: 'PageIndex',
  components: {
    Header,
    Presentation
  }
}
</script>
