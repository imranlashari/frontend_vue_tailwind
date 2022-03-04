<template>
  <div>
    
    <div class="grid grid-cols-3 gap-4">
        <div></div>
        
        <div class="flex w-full max-w-xs mt-4 m-auto">   
            <div>
                <p class="text-center text-xl font-bold m-2">Sign In</p>
                <form class="bg-white shadow-md rounded px-8 pt-6 pb-8 mb-4">
                    <div class="mb-4">
                    <label class="block text-gray-700 text-sm font-bold mb-2" for="phone">
                        Phone #
                    </label>
                    <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="phone" type="text" placeholder="03219876543">
                    </div>
                    <div class="mb-6">
                    <label class="block text-gray-700 text-sm font-bold mb-2" for="password">
                        Password
                    </label>
                    <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 mb-3 leading-tight focus:outline-none focus:shadow-outline" id="password" type="password" placeholder="******************">
                    </div>
                    <div class="flex items-center justify-center">
                        <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline" type="button">
                            Sign In
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