<template>
  <div class="home col">
    <div class="home-line"></div>
    <div class="home-content content row">
      <div class="content-item col col-5">
        <div class="content-item-wrap">
          <div class="content-heading">
            <h4 class="content-title">Activity</h4>
            <select class="content-select form-control form-control-sm">
              <option>All updates</option>
              <option>Some updates</option>
              <option>Big updates</option>
              <option>Popular updates</option>
            </select>
          </div>
          <div class="content-data"></div>
        </div>
      </div>
      <div class="content-item col col-7">
        <div class="content-item-wrap">
          <div class="content-heading">
            <h4 class="content-title">Vehicles</h4>
            <div class="content-options">
              <div 
                class="content-option" 
                :class="{active : activeTab == 1}"
                @click="setActiveTab(1)"
              >
                <span class="material-icons">list</span>
              </div>
              <div 
                class="content-option"
                :class="{active : activeTab == 2}"
                @click="setActiveTab(2)"
              >
                <span class="material-icons">outlined_flag</span>
              </div>
            </div>
          </div>
          <div class="content-data"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    activeTab: 1
  }),
  methods: {
    setActiveTab(tabNumber) {
      this.activeTab = tabNumber;
    }
  }
}
</script>
