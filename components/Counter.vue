<template>
  <div class="gradient bg-red-dark">
    <div class="container-md flex justify-around py-32">
      <icon-counter
        :count="3"
        title="Podcasts"
      >
        <podcast />
      </icon-counter>
      <icon-counter
        :count="10"
        title="Länder"
      >
        <earth />
      </icon-counter>
      <icon-counter
        :count="20"
        title="Flaschen"
      >
        <bottle />
      </icon-counter>
      <icon-counter
        :count="80"
        title="Gläser"
      >
        <glass />
      </icon-counter>
    </div>
  </div>
</template>

<script>
import Earth from '~/components/icons/Earth.vue'
import Glass from '~/components/icons/Glass.vue'
import Bottle from '~/components/icons/Bottle.vue'
import Podcast from '~/components/icons/Podcast.vue'
import IconCounter from '~/components/IconCounter.vue'

export default {
  name: 'Counter',
  components: {
    Glass,
    Bottle,
    Podcast,
    Earth,
    IconCounter
  }
}
</script>

<style lang="scss" scoped>
.gradient {
  background: linear-gradient(20deg, #621b18, #ef5753 90%);
}
</style>
