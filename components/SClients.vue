<template>
  <div class="c-clients">
    <a
      :href="client.link"
      target="_blank"
      rel="noopener"
      class="c-client"
      v-for="client in clients"
      :key="client.name"
      v-html="client.logo_markup"
    />
  </div>
</template>

<script lang="ts">
import { defineComponent } from '@vue/composition-api'

export default defineComponent({
  name: 'SClients',

  props: {
    clients: {
      type: Array,
      required: true
    }
  }
})
</script>
