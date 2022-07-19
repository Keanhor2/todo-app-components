<template>
    <FriendNav/>
    <FriendForm/>
    <FriendCard/>

</template>

<script>
import FriendNav from "./components/FriendNav.vue"
import FriendForm from "./components/FriendForm.vue"
import FriendCard from './components/FriendCard.vue'

export default {
  data() {
    return {
     friends:""
    }
  },

  components: {
    FriendNav,
    FriendForm,
    FriendCard
  },
 
}
</script>

<style>
#app {
  width: 60%;
  margin: auto;
}
</style>
