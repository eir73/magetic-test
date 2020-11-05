<template>
  <div class="sidebar" :class="{open : value}">
    <div class="sidebar-toggler">
      <span 
        class="material-icons"
        @click="$emit('toggle')"
      >
        dashboard</span>
      <div 
        class="sidebar-opened"
        v-if="value"
      >
        <div class="sidebar-logo">
          <img src="../assets/logo.png" alt="logo">
        </div>
        <span
          class="material-icons"
          @click="$emit('toggle')"
        >
        close</span>
      </div>
    </div>
    <ul class="sidebar-sidenav sidenav">
      <li class="sidenav-item">
        <a href="#" class="sidenav-link">link 1</a>
        <span 
          class="material-icons"
          v-if="!value"
        >
          fiber_manual_record</span>
      </li>
      <li class="sidenav-item">
        <a href="#" class="sidenav-link">link 2</a>
        <span 
          class="material-icons"
          v-if="!value"
        >
          fiber_manual_record</span>
      </li>
      <li class="sidenav-item">
        <a href="#" class="sidenav-link">link 3</a>
        <span 
          class="material-icons"
          v-if="!value"
        >
          fiber_manual_record</span>
      </li>
      <li class="sidenav-item">
        <a href="#" class="sidenav-link">link 4</a>
        <span 
          class="material-icons"
          v-if="!value"
        >
          fiber_manual_record</span>
      </li>
      <li class="sidenav-item">
        <a href="#" class="sidenav-link">link 5</a>
        <span 
          class="material-icons"
          v-if="!value"
        >
          fiber_manual_record</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: ['value']
}
</script>
