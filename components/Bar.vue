<template>
  <div
    ref="sticky"
    :class="{
      'bg-transparent': !sticky,
      'text-grey-lighter': !sticky,
      'py-8': !sticky,
      'text-2xl': !sticky,
      'py-2': sticky,
      'text-xl': sticky,
      'sticky-bar': sticky,
      'text-black': sticky,
      'bg-grey-lighter': sticky
    }"
    class="bar w-full fixed pin-x pin-t h-auto z-10"
  >
    <div class="flex justify-between px-8 py-2">
      <div class="self-center">
        <nuxt-link to="/">
          Ausbaufähig
        </nuxt-link>
      </div>
      <social />
    </div>
  </div>
</template>

<script>
import toggleStickyness from '~/mixins/toggle-stickyness'
import Social from '~/components/Social.vue'

export default {
  name: 'Bar',
  components: {
    Social
  },
  mixins: [toggleStickyness]
}
</script>

<style lang="scss">
.bar {
  transform: translateZ(2px);
  transition: all 1s ease;
}

.sticky-bar {
  box-shadow: 0 3px 10px 0 rgba(255, 255, 255, 0.1);
}

.sticky-bar .twitter {
  color: #1da1f2;

  &:hover {
    color: darken(#1da1f2, 10%);
  }
}

.sticky-bar .instagram {
  color: #e1306c;

  &:hover {
    color: darken(#e1306c, 10%);
  }
}

.sticky-bar + .content {
  padding-top: 42px;
}
</style>
