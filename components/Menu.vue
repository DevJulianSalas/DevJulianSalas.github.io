<template>
  <div class="menu">
    <ul v-for="(item, index) in navItems" :key="index">
      <li><a href="#">{{ item }}</a></li>
    </ul>
  </div>
</template>
<script>
export default {
  data: function() {
    return {
      navItems: [
        'About',
        'Services',
        'Projects',
        'Experience',
        'Blog',
        'Contact'
      ]
    }
  }
}
</script>
<style scoped>
.menu {
  display: flex;
  justify-content: flex-end;
  width: 95%;
}
</style>
