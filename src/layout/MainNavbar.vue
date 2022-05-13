<template>
  <md-toolbar>
    <div class="md-toolbar-row">
      <div class="md-toolbar-section-start">
        <h3 class="md-title">Brand</h3>
      </div>
      <div class="md-toolbar-section-end">
        <md-button class="md-just-icon md-simple md-toolbar-toggle">
          <span class="icon-bar"></span>
          <span class="icon-bar"></span>
          <span class="icon-bar"></span>
        </md-button>

        <div class="md-collapse">
          <md-list>
            <md-list-item href="#dashboard">
              <i class="material-icons">dashboard</i>
              <p class="hidden-lg hidden-md">Dashboard</p>
            </md-list-item>

            <md-list-item href="#user">
              <i class="material-icons">person</i>
              <p class="hidden-lg hidden-md">Profile</p>
            </md-list-item>
          </md-list>
        </div>
      </div>
    </div>

  </md-toolbar>
</template>

<script>

</script>

<style scoped lang="scss">
  .md-list {
    flex-flow: row nowrap;
  }

  .md-toolbar {
    min-height: auto;
    padding-left: 15px;
    padding-right: 15px;

    .md-toolbar-row {
      margin: auto;
      max-width: 1140px;
    }
  }

  

</style>
