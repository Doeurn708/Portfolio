<template>
  <div class="min-h-screen  bg-gradient-to-r from-blue-900 to-black text-white pt-24 px-4 sm:px-6 lg:px-8">
    <div class="max-w-6xl mx-auto py-12">
      
      <div class="mb-12">
        <h1 class="text-3xl font-bold inline-block border-b-4 border-cyan-400 pb-2">
          Contact Me
        </h1>
      </div>

      <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
        
        <div class="space-y-6">
          
          <div class="bg-[#0b1329] border border-slate-800 rounded-xl p-8 flex flex-col items-center justify-center min-h-[160px] transition-all hover:border-cyan-500/50">
            <div class="bg-blue-600 p-3 rounded-xl mb-3 flex items-center justify-center">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 002-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
              </svg>
            </div>
            <a href="mailto:kimsothearith20007@gmail.com" class="text-slate-300 hover:text-cyan-400 transition-colors break-all text-center">
              kimsothearith20007@gmail.com
            </a>
          </div>

          <div class="bg-[#0b1329] border border-slate-800 rounded-xl p-8 flex flex-col items-center justify-center min-h-[160px] transition-all hover:border-cyan-500/50">
            <div class="bg-indigo-600 p-3 rounded-xl mb-3 flex items-center justify-center">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-white" fill="currentColor" viewBox="0 0 24 24">
                <path fill-rule="evenodd" clip-rule="evenodd" d="M12 2C6.477 2 2 6.477 2 12c0 4.42 2.865 8.166 6.839 9.489.5.092.682-.217.682-.482 0-.237-.008-.866-.013-1.7-2.782.603-3.369-1.34-3.369-1.34-.454-1.156-1.11-1.464-1.11-1.464-.908-.62.069-.608.069-.608 1.003.07 1.531 1.03 1.531 1.03.892 1.529 2.341 1.087 2.91.831.092-.646.35-1.086.636-1.336-2.22-.253-4.555-1.11-4.555-4.943 0-1.091.39-1.984 1.029-2.683-.103-.253-.446-1.27.098-2.647 0 0 .84-.269 2.75 1.025A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.294 2.747-1.025 2.747-1.025.546 1.377.203 2.394.1 2.647.64.699 1.028 1.592 1.028 2.683 0 3.842-2.339 4.687-4.566 4.935.359.309.678.919.678 1.852 0 1.336-.012 2.415-.012 2.743 0 .267.18.579.688.481C19.138 20.161 22 16.416 22 12c0-5.523-4.477-10-10-10z" />
              </svg>
            </div>
            <a href="https://github.com/RithCoding" target="_blank" class="text-slate-300 hover:text-cyan-400 transition-colors break-all text-center">
              github.com/RithCoding
            </a>
          </div>

        </div>

        <div class="bg-[#0b1329]/50 border border-slate-800 rounded-xl p-8 transition-all hover:border-slate-700">
          <form @submit.prevent="handleSubmit" class="space-y-6">
            
            <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
              <div>
                <input 
                  v-model="formData.firstName"
                  type="text" 
                  placeholder="First Name" 
                  class="w-full bg-[#0b1329] border border-slate-800 rounded-lg px-4 py-3 text-slate-300 placeholder-slate-500 focus:outline-none focus:border-cyan-500 focus:ring-1 focus:ring-cyan-500 transition-all"
                  required
                />
              </div>
              <div>
                <input 
                  v-model="formData.lastName"
                  type="text" 
                  placeholder="Last Name" 
                  class="w-full bg-[#0b1329] border border-slate-800 rounded-lg px-4 py-3 text-slate-300 placeholder-slate-500 focus:outline-none focus:border-cyan-500 focus:ring-1 focus:ring-cyan-500 transition-all"
                  required
                />
              </div>
            </div>

            <div>
              <input 
                v-model="formData.email"
                type="email" 
                placeholder="Email" 
                class="w-full bg-[#0b1329] border border-slate-800 rounded-lg px-4 py-3 text-slate-300 placeholder-slate-500 focus:outline-none focus:border-cyan-500 focus:ring-1 focus:ring-cyan-500 transition-all"
                required
              />
            </div>

            <div>
              <textarea 
                v-model="formData.message"
                rows="5" 
                placeholder="Message" 
                class="w-full bg-[#0b1329] border border-slate-800 rounded-lg px-4 py-3 text-slate-300 placeholder-slate-500 focus:outline-none focus:border-cyan-500 focus:ring-1 focus:ring-cyan-500 transition-all resize-none"
                required
              ></textarea>
            </div>

            <div>
              <button 
                type="submit" 
                class="w-full bg-gradient-to-r from-blue-600 to-cyan-400 hover:from-blue-500 hover:to-cyan-300 text-white font-bold py-3 px-6 rounded-lg shadow-lg hover:shadow-cyan-500/20 active:scale-[0.99] transition-all tracking-wider uppercase text-sm"
              >
                Send Message
              </button>
            </div>

          </form>
        </div>

      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

// បង្កើត Reactive Object សម្រាប់ផ្ទុកទិន្នន័យពី Form
const formData = ref({
  firstName: '',
  lastName: '',
  email: '',
  message: ''
})

// Function សម្រាប់ដំណើរការនៅពេលចុច Send Message
const handleSubmit = () => {
  console.log('ទិន្នន័យដែលបានផ្ញើ៖', formData.value)
  alert('សាររបស់អ្នកត្រូវបានផ្ញើដោយជោគជ័យ!')
  
  // សម្អាត Form ឡើងវិញបន្ទាប់ពីផ្ញើរួច
  formData.value = {
    firstName: '',
    lastName: '',
    email: '',
    message: ''
  }
}
</script>