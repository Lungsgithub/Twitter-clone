<template>
  <q-page>
    <div class="q-py-lg q-px-md">
    <q-input bottom-slots v-model="newTweetContent" placeholder="What's happening?" counter maxlength="256">
        <template v-slot:before>
          <q-avatar>
            <img src="https://cdn.quasar.dev/img/avatar5.jpg">
          </q-avatar>
        </template>

        <template v-slot:append>
          <q-icon v-if="text !== ''" name="close" @click="text = ''" class="cursor-pointer" />
          <q-icon name="schedule" />
        </template>

        <template v-slot:hint>
          Field hint
        </template>

        <template v-slot:after>
          <q-btn round dense flat icon="send" />
        </template>
      </q-input>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'PageHome'
})

</script>
