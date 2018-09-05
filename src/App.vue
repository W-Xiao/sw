<template>
  <div id="app">
    <Navgatior />
    <Index />
    <Project v-if=" change == index " @click="nav(index)"/>
    <Enterprise v-else-if=" change == index " @click="nav(index)"/>
    <Discounts v-else-if=" change == index " @click="nav(index)"/>
    <Contact v-else-if=" change == index " @click="nav(index)"/>
  </div>
</template>

<script>
import Navgatior from './components/Navgatior'
import Index from './pages/Index.vue'
import Project from './pages/Project.vue'
import Enterprise from './pages/Enterprise'
import Discounts from './pages/Discounts'
import Contact from './pages/Contact'
export default {
  name: 'app',
  data() {
    return {
      index: 0
    }
  },
  components: {
    Navgatior,
    Index,
    Project,
    Enterprise,
    Discounts,
    Contact
  },
  methods: {
    nav(index) {
      this.index = index
    }
  }
}
</script>

<style>
 @import './css/App.css';
</style>
