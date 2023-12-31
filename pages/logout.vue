<template>
  <div>Logging out...</div>
</template>

<script>
export default {
  mounted() {
    let isLoggedIn = useCookie("isLoggedIn");
    isLoggedIn.value = null;

    let userId = useCookie("userId");
    userId.value = null;

    let name = useCookie("name");
    name.value = null;

    let email = useCookie("email");
    email.value = null;

    this.$router.push("/login");
  },
};
</script>
