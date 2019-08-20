<template>
  <div class="container">
    <HeroList class="herolist" :heroes="heroes" @selectHero="onSelectHero($event)" />
    <Hero class="hero" :hero="heroDetail" />
  </div>
</template>

<script>
import HeroList from '@/components/HeroList'
import Hero from '@/components/Hero'

export default {
  components: {
    HeroList,
    Hero
  },
  data () {
    return {
      heroes: [
        { id: 11, name: 'Dr Fish' },
        { id: 12, name: 'Super Dog' },
        { id: 13, name: 'Green Cat' },
        { id: 14, name: 'Pigger' },
        { id: 15, name: 'Happy Man' },
        { id: 16, name: 'NicoNicoNico' }
      ],
      heroDetail: null
    }
  },
  created () {
    this.heroDetail = this.heroes[0]
  },
  methods: {
    onSelectHero (index) {
      this.heroDetail = this.heroes[index]
    }
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.herolist {
  margin-right: 50px;
}

</style>
