<template>
	<div id="home">
		<h1>{{ msg }}</h1>
		<button @click="googleLogin">Googleアカウントでログイン</button>
	</div>
</template>

<script type="text/javascript">
	export default {
		name: "home",
		data() {
			return {
				msg: "welcome to markdown"
			}
		},
		methods: {
			googleLogin: function () {
				firebase.auth().signInWithRedirect(new firebase.auth.GoogleAuthProvider());
			}
		}
	};
</script>
