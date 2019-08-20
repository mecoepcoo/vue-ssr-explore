<template>
  <div class="MyHeroes">
    <h1 class="title">
      My Heroes
    </h1>
    <a-list
      itemLayout="horizontal"
      :dataSource="heroes"
    >
      <a-list-item slot="renderItem" slot-scope="item, index" @click.native="selectHero(index)">
        <a-list-item-meta>
          <a slot="title"><span>{{ item.id }}. </span>{{ item.name }}</a>
        </a-list-item-meta>
      </a-list-item>
    </a-list>
  </div>
</template>

<script>
export default {
  props: ['heroes'],
  methods: {
    selectHero (index) {
      this.$emit('selectHero', index)
    }
  }
}
</script>

<style>

</style>
