<template>
  <div></div>
</template>

<script>
export default {
  data() {
    return {};
  },
  mounted() {
    let isLoggedIn = useCookie("isLoggedIn");

    if (!isLoggedIn.value) {
      this.$router.push("/login");
    }
  },
};
</script>
