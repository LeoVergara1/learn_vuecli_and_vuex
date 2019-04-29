<template>
<body class="text-center">
    <form class="form-signin">
      <img class="mb-4" src="https://getbootstrap.com/docs/4.0/assets/brand/bootstrap-solid.svg" alt="" width="72" height="72">
      <h1 class="h3 mb-3 font-weight-normal">Please sign in</h1>
      <label for="inputEmail" class="sr-only">Email address</label>
      <input type="text" id="inputEmail" class="form-control" placeholder="Email address" required="" autofocus="" v-model="user.name">
      <label for="inputPassword" class="sr-only">Password</label>
      <input type="password" id="inputPassword" class="form-control" placeholder="Password" required="" v-model="user.password">
      <div class="checkbox mb-3">
        <label>
          <input type="checkbox" value="remember-me"> Remember me
        </label>
      </div>
      <button class="btn btn-lg btn-primary btn-block" @click="send_login">Sign in</button>
      <p class="mt-5 mb-3 text-muted">© 2017-2018</p>
    </form>
</body>
</template>
<script>
export default {
		name: 'Login',
    data () {
      return {
				user: {
					name: "",
					password: ""
				}
			}
		},
	  methods: {
			send_login: function() {
				console.log(this.$store.state.count)
				this.$store.state.count = 10;
			}
		},
}
</script>

<style scope>
body{
	  padding-left: 30%;
    padding-right: 30%;
}
</style>
