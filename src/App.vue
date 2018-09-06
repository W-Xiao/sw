<template>
  <div id="app">
    <Navgatior v-on:changeIndex="change" />
    <Index v-if=" 0 == index " />
    <Project v-else-if=" 1 == index "/>
    <Enterprise v-else-if=" 2 == index "/>
    <Discounts v-else-if=" 3 == index "/>
    <Contact v-else-if=" 4 == index "/>
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
    change(index) {
      this.index = index
    }
  }
}
</script>

<style>
 @import './css/App.css';
</style>
