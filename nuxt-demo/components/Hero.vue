<template>
  <div class="MyHeroDetail">
    <h1 class="title">
      {{ hero.name }} details
    </h1>
    <a-form>
      <a-form-item
        v-bind="formItemLayout"
        label="id"
      >
        <span>
          {{ hero.id }}
        </span>
      </a-form-item>
      <a-form-item>
        <a-input
          placeholder="input name"
          v-model="hero.name"
        >
        </a-input>
      </a-form-item>
    </a-form>
  </div>
</template>

<script>
export default {
  data () {
    return {
      formItemLayout: {
        labelCol: { span: 6 },
        wrapperCol: { span: 6 }
      }
    }
  },
  props: ['hero']
}
</script>

<style>

</style>
