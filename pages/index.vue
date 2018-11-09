<template>
  <div>
    <bar :should-check-stickyness="true" />
    <div class="content flex-1">
      <hero />
      <section class="container h-48">
        Hello
      </section>
      <counter />
    </div>
    <footer-bar />
  </div>
</template>

<script>
import Bar from '~/components/Bar.vue'
import Hero from '~/components/Hero.vue'
import Counter from '~/components/Counter.vue'
import FooterBar from '~/components/Footer.vue'

export default {
  components: {
    Bar,
    Hero,
    FooterBar,
    Counter
  }
}
</script>
