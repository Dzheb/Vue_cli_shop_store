<template>
  <div id="app">
    <ShopMain />
  </div>
</template>
<script>
import { mapActions, mapState, mapMutations } from 'vuex';
import ShopMain from './components/ShopMain.vue';
export default {
  name: 'App',
  components: {
    ShopMain,
  },
  methods: {
    ...mapMutations(['SET_PAYMENT']),
  },
  computed: {
    ...mapState(['projectList']),
    ...mapActions(['fetchData']),
  },
  created() {
    this.$store.commit('SET_PROJECTS', this.fetchData());
  },
};
</script>

