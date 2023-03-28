<template>
  <q-page>
    <div class="q-py-lg q-px-md row items-end q-col-gutter-md">
      <div class="col">

        <q-input class="newTweet" autogrow bottom-slots v-model="newTweetContent" placeholder="What's happening?" counter maxlength="256">
        <template v-slot:before>
          <q-avatar size="xl">
            <img src="https://cdn.quasar.dev/img/avatar5.jpg">
          </q-avatar>
        </template>
      </q-input>

      </div>

      <div class="col col-shrink">
      <q-btn :disable="!newTweetContent"  class="q-mb-lg" unelevated rounded nocaps color="primary" label="tweet" />
      </div>
    </div>


    <q-serparator size="15px" />



  </q-page>
</template>

<script>
import { defineComponent } from 'vue'

export default{
  name: 'PageHome',
  data(){
    return{
      newTweetContent:""
    }
  }
}

</script>

<!-- I still wanna make this external -->

<style lang="sass">
.newTweet
  textarea
  font-size: 19px
  line-height: 1.4

  
</style>