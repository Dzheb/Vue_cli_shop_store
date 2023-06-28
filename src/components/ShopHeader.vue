<template>
  <div>
    <header class="header">
      <div class="header__left">
        <img src="../assets/img/Logo.svg" alt="Logo" />
        <h3>Interno</h3>
      </div>
      <nav class="header__right">
        <a
          @click="currentPageChange(page)"
          v-for="page in shopPages"
          :key="page.id"
        >
          {{ page }}
        </a>
      </nav>
    </header>
  </div>
</template>

<script>
export default {
  name: 'ShopHeader',

  props: {
    curPage: {
      type: String,
      default() {
        return '';
      },
    },
    shopPages: {
      type: Array,
      default() {
        return [];
      },
    },
  },
  data() {
    return {};
  },
  methods: {
    currentPageChange(page) {
      this.$emit('currentPageChange', page);
    },
  },
};
</script>

<style lang="css" scoped>
a {
  text-decoration: none;
  color: rgba(77, 80, 83, 1);
  cursor: pointer;
}
header {
  color: rgba(41, 47, 54, 1);
  font-family: Jost;
  font-size: 20px;
  font-weight: 400;
  line-height: 25px;
  letter-spacing: 0em;
  text-align: center;
  margin: 53px 0;
  display: flex;
  justify-content: space-between;
  align-items: baseline;
}
.header__left {
  display: flex;
  align-items: baseline;
  gap: 4px;
}
.header__right {
  display: flex;
  align-items: baseline;
  gap: 40px;
}
.header__right a {
  text-decoration: none;
}
</style>
