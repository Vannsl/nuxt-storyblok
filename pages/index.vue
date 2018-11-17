<template>
  <div>
    <bar :should-check-stickyness="true" />
    <div class="content flex-1">
      <hero />
      <section class="container mx-auto p-8 my-16">
        <div class="flex flex-wrap flex-row-reverse">
          <div
            class="flex-1 max-w-full px-4"
            style="min-width: 300px;"
          >
            <div class="circular-image" />
          </div>
          <div
            class="flex-1 px-4 max-w-full text-xl leading-tight"
            style="min-width: 300px;"
          >
            <div class="mb-8">
              Hallo,<br><br>
              wir sind Ben und Vanessa und bald findest du hier die Episoden unseres Podcasts <strong>Ausbaufähig</strong>. Jede Woche (ist zumindest der Plan) werden wir einen Wein zu einem bestimmten Thema (z.B. wie aktuell die Forum Vini 2018, oder ein spezifisches Land, Region etc.) trinken und über ihn reden. Wir sind keine ausgebildeten Sommeliers, sondern genießen einfach sehr gerne guten Wein und fanden es schade, dass es so wenig deutsche Podcasts über Wein gibt. Denn schließlich ist es nicht immer leicht, einen spannenden neuen Wein zu finden. Üblicherweise kosten unsere Weine zwischen 6,50 und 30 €, der Hauptanteil wird bei 15 € liegen. Also! Bald geht es los, wir freuen uns auf drauf!
              <br><br>
              Du wartest ganz gespannt auf die erste Episode? Folge uns einfach auf unserem <a href="https://twitter.com/ausbaufahig" target="_blank">Twitter-Account</a>, da werden wir tweeten, sobald neue Revisionen zur Verfügung stehen!
              <br><br>
              Hast du Fragen? Dann schreibe uns gerne an <a href="mailto:mail@vannsl.io">mail@vannsl.io</a>.
            </div>
          </div>
        </div>
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
  },
  head() {
    return {
      title: 'Ausbaufähig - der Wein-Podcast',
      meta: [
        // hid is used as unique identifier. Do not use `vmid` for it as it will not work
        { hid: 'description', name: 'description', content: 'Beim Wein-Podcast Ausbaufähig von Ben und Vanessa werden verschiedenste Weine aus der ganzen Welt getrunken und besprochen. Weder Ben noch Vanessa sind ausgebildete Sommeliers, sie trinken einfach nur gern Wein! Und wie Wein erstmal im Fass ausgebaut werden muss, bevor er gut wird, ist ihr Wissen daher auch eher "ausbaufähig", aber sie trinken trotzdem gerne!' },
        { hid: 'author', name: 'author', content: 'Vannsl.io, Vanessa Böhner'}
      ]
    }
  },
}
</script>

<style lang="scss" scoped>
.circular-image {
  margin: 48px auto;
  border-radius: 150px;
  max-width: 300px;
  width: 300px;
  height: 300px;
  background: url('~assets/img/ben_und_vanessa.jpg');
  background-position: 30%;
  background-size: cover;
  box-shadow: 0px 0px 50px -10px rgba(0, 0, 0, 0.75);
}
</style>
