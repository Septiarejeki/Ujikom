<template>
<div class="p-56">
  
  <div class="flex w-96 flex-col space-y-5 rounded-lg border py-10 px-5 shadow-xl mx-auto">
    <div class="mx-auto mb-2 space-y-3">
      <h1 class=" text-2xl font-bold text-gray-700" align="center">LOGIN</h1>
      <p class=" text-1xl text-gray-600">Login to access your account</p>
    </div>
  
    <div>
      <div class="relative mt-2 w-full">
        <input type="text" id="email" value="email@gmail.com" class="border-1 peer block w-full appearance-none rounded-lg border border-gray-300 bg-transparent px-2.5 pb-2.5 pt-4 text-sm text-gray-900 focus:border-blue-600 focus:outline-none focus:ring-0" placeholder=" " />
        <label for="email" class="absolute top-2 left-1 z-10 origin-[0] -translate-y-4 scale-75 transform cursor-text select-none bg-white px-2 text-sm text-gray-500 duration-300 peer-placeholder-shown:top-1/2 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:scale-100 peer-focus:top-2 peer-focus:-translate-y-4 peer-focus:scale-75 peer-focus:px-2 peer-focus:text-blue-600"> Enter Your Email </label>
      </div>
    </div>
  
    <div>
      <div class="relative mt-2 w-full">
        <input type="text" id="password" class="border-1 peer block w-full appearance-none rounded-lg border border-gray-300 bg-transparent px-2.5 pb-2.5 pt-4 text-sm text-gray-900 focus:border-blue-600 focus:outline-none focus:ring-0" placeholder=" " />
        <label for="password" class="absolute top-2 left-1 z-10 origin-[0] -translate-y-4 scale-75 transform cursor-text select-none bg-white px-2 text-sm text-gray-500 duration-300 peer-placeholder-shown:top-1/2 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:scale-100 peer-focus:top-2 peer-focus:-translate-y-4 peer-focus:scale-75 peer-focus:px-2 peer-focus:text-blue-600"> Enter Your Password</label>
      </div>
    </div>
  
    <button class="rounded-lg bg-blue-800 py-3 font-bold text-white">Login</button>
  </div>
  </div>
</template>

<script>
import { mapActions, mapGetters } from 'vuex';

export default {
    data() {
        return {
            email: '',
            password: '',
        };
    },
    computed: {
        ...mapGetters('auth',['loginError', 'isAuthenticated']),
    },
    methods: {
        ...mapActions('auth', ['login']),
        async performLogin() {
            const credentials = {
                email: this.email,
                password: this.password,
            };
            const success = await this.login(credentials);
            if (success && this.isAuthenticated) {
                // Redirect to the desired route on successful login
                this.$router.push('/');
            } else {
                if(this.loginError){
                    alert(this.loginError)
                } else{
                alert("Login Failed");
                }
            }
        },
    },
};
</script>