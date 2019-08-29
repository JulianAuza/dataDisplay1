<template>
  <div class="lateral-nav">
    <div class="lateral-nav-item-container" v-for="(value, x) in options" :key="x" :class="value.selected ? 'selected' : ''">
      <div class="lateral-nav-item">
         <img height="15px" src="../assets/images/logo.png"><div class="lateral-nav-text"><p>{{value.name}}</p></div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'

@Component
export default class NavBar extends Vue {
    @Prop()
    private options!: object[]
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>