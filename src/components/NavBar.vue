<template>
  <div class="nav-container">
    <div class="main-nav-container">
      <div class="display-flex">
        <div>
          <img height="35px" src="../assets/images/compass.png" />
        </div>
        <div class="main-nav display-flex">
          <div class="main-nav-item">
            <img height="20px" src="../assets/images/search.png"><a>SEARCH</a>
          </div>
          <div class="main-nav-item">
             <img height="20px" src="../assets/images/tool.png"><a>TOOLS</a>
          </div>
          <div class="main-nav-item">
             <img height="20px" src="../assets/images/map.png"><a>MY PROPERTIES</a>
          </div>
        </div>
      </div>
    </div>

    <div class="user-info display-flex">
      <div class="remaining-properties"> <span style="font-style: italic;opacity:.7;">Remaining Properties: &nbsp;</span> <strong>2</strong> &nbsp;&nbsp;&nbsp;| </div>
       <img class="help" height="20px" src="../assets/images/questions.png">
       <img class="user-image" height="20px" src="../assets/images/user.png">
    </div> 
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class NavBar extends Vue {
  @Prop()
  private userInitials!: string;

  @Prop()
  private menuItems!: object[];
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>