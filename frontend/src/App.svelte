<script lang="ts">
  import logo from './assets/images/logo-universal.png';
  import { Greet } from '../wailsjs/go/main/App.js';

  let resultText: string = "Please enter your name below 👇";
  let name: string;

  function greet(): void {
    Greet(name).then(result => resultText = result);
  }
</script>

<main class="flex flex-col items-center justify-center h-screen bg-gray-100 p-4">
  <img alt="Wails logo" id="logo" src="{logo}" class="w-32 h-32 mb-6" />

  <div class="result text-xl text-gray-700 font-semibold mb-4" id="result">{resultText}</div>

  <div class="input-box flex flex-col items-center space-y-4" id="input">
    <input
            autocomplete="off"
            bind:value="{name}"
            class="input w-64 p-2 border border-gray-300 rounded-lg shadow-sm focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-transparent"
            id="name"
            type="text"
            placeholder="Enter your name"
    />
    <button class="btn w-32 bg-blue-500 text-white py-2 px-4 rounded-lg hover:bg-blue-600 transition duration-200" on:click="{greet}">
      Greet
    </button>
  </div>
</main>
