<template>
  <div>
    <div class="flex flex-col justify-center min-h-full px-6 py-12 lg:px-8">
      <div class="sm:mx-auto sm:w-full sm:max-w-sm">
        <h2
          class="mt-10 text-2xl font-bold leading-9 tracking-tight text-center text-gray-900"
        >
          Create an Account
        </h2>
      </div>

      <div class="mt-10 sm:mx-auto sm:w-full sm:max-w-sm">
        <div class="space-y-6">
          <div>
            <label
              for="email"
              class="block text-sm font-medium leading-6 text-gray-900"
              >Email address</label
            >
            <div class="mt-2">
              <input
                v-model="userData.email"
                type="email"
                class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6"
              />
            </div>
          </div>

          <div>
            <div class="flex items-center justify-between">
              <label
                for="password"
                class="block text-sm font-medium leading-6 text-gray-900"
                >Password</label
              >
              <div class="text-sm">
                <a
                  href="#"
                  class="font-semibold text-indigo-600 hover:text-indigo-500"
                  >Forgot password?</a
                >
              </div>
            </div>
            <div class="mt-2">
              <input
                v-model="userData.password"
                type="password"
                class="block w-full rounded-md border-0 py-1.5 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6"
              />
            </div>
          </div>

          <div>
            <button
              @click="login()"
              class="flex w-full justify-center rounded-md bg-indigo-600 px-3 py-1.5 text-sm font-semibold leading-6 text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600"
            >
              Sign in
            </button>
          </div>
        </div>

        <p class="mt-10 text-sm text-center text-gray-500">
          Not a member?
          <NuxtLink
            to="/register"
            class="font-semibold leading-6 text-indigo-600 hover:text-indigo-500"
            >Create an Account</NuxtLink
          >
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      userData: {
        email: "",
        password: "",
      },
    };
  },
  mounted() {
    let isLoggedIn = useCookie("isLoggedIn");

    if (isLoggedIn.value && isLoggedIn.value == true) {
      this.$router.push("/profile");
    }
  },
  methods: {
    login() {
      this.$http
        .$post("/auth/login", {
          body: {
            ...this.userData,
          },
        })
        .then((res) => {
          if (res.success) {
            let isLoggedIn = useCookie("isLoggedIn");
            isLoggedIn.value = "true";

            let userId = useCookie("userId");
            userId.value = res.user.userId;

            let name = useCookie("name");
            name.value = res.user.name;

            let email = useCookie("email");
            email.value = res.user.email;

            this.$router.push("/profile");
          } else {
            alert(res.message);
          }
        });
    },
  },
};
</script>
