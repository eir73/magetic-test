<template>
  <div class='app-main-layout'>
    <Navbar />

    <Sidebar v-model="isSidebarOpen" @toggle="toggleSidebar" />

    <main class="app-content" :class="{full : !isSidebarOpen}">
      <div class="app-page">
        <router-view />
      </div>
    </main>
  </div>
</template>

<script>
import Navbar from '@/components/Navbar'
import Sidebar from '@/components/Sidebar'

export default {
  name: 'main-layout',
  data: () => ({
    isSidebarOpen: false,
  }),
  methods: {
    toggleSidebar() {
      this.isSidebarOpen = !this.isSidebarOpen  
    },
  },
  components: {
    Navbar,
    Sidebar,
  },
}
</script>
