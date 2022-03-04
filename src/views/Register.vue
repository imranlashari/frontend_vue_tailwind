<template>
  <div>
    
    <div class="grid grid-cols-3 gap-4">
        <div></div>
        
        <div class="flex w-full max-w-xs mt-4 m-auto">   
            <div>
                <p class="text-center text-xl font-bold m-2">Sign Up</p>
                <form class="bg-white shadow-md rounded px-8 pt-6 pb-8 mb-4" id="signup_form">
                    <div class="mb-4">
                    <label class="block text-gray-700 text-sm font-bold mb-2" for="name">
                        Name
                    </label>
                    <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="name" v-model="name" type="text" placeholder="Enter Name">
                    </div>
                    <div class="mb-4">
                    <label class="block text-gray-700 text-sm font-bold mb-2" for="phone">
                        Phone #
                    </label>
                    <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="phone" v-model="phone" type="text" placeholder="03219876543">
                    </div>
                    <div class="mb-6">
                    <label class="block text-gray-700 text-sm font-bold mb-2" for="password">
                        Password
                    </label>
                    <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 mb-3 leading-tight focus:outline-none focus:shadow-outline" id="password" v-model="password" type="text" placeholder="********">
                    <p class="text-xs italic">*Please enter 8 digit password.</p>
                    </div>
                    <div class="flex items-center justify-center">
                        <button @click="signup" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline" type="button">
                            Sign Up
                        </button>
                    </div>
                </form>
                <p class="text-center text-gray-500 text-xs">
                    &copy;2022 Imran-Lashari. All rights reserved.
                </p>
            </div>
        </div>
        
        <div></div>
    </div>

  </div>
</template>

<script>
import axios from 'axios'

export default {
    name: 'Register',
    data() {
        return {
            name:'',
            phone:'',
            password:'',
        }
    },

    created() {
        
    },

    mounted() {
        
    },

    methods: {
        signup() {

            const form = {
                    name: this.name,
                    phone: this.phone,
                    password: this.password,
            }

            //=== validation
            if (form.name.length <5) 
            {
                alert('Please enter complete name');
            }
            else if (form.phone.length != 11) 
            {
                alert('Please enter 11 digits phone number');
            }
            else if (form.password.length < 8) 
            {
                alert('Please enter 8 digits password');
            }
            else
            {
                axios.post('http://localhost:8000/api/register', form).then(
                    res => {
                            this.$router.push('/login');
                            console.log(res);
                        }
                ).catch(
                    err => {
                        console.log(err);
                    }
                )
            }
        },
    },
}
</script>
