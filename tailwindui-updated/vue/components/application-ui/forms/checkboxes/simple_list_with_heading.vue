<!--
  This example requires some changes to your config:
  
  ```
  // tailwind.config.js
  module.exports = {
    // ...
    plugins: [
      // ...
      require('@tailwindcss/forms'),
    ],
  }
  ```
-->
<template>
  <fieldset>
    <legend class="text-lg font-medium text-gray-900">Members</legend>
    <div class="mt-4 divide-y divide-gray-200 border-t border-b border-gray-200">
      <div v-for="(person, personIdx) in people" :key="personIdx" class="relative flex items-start py-4">
        <div class="min-w-0 flex-1 text-sm">
          <label :for="`person-${person.id}`" class="select-none font-medium text-gray-700">{{ person.name }}</label>
        </div>
        <div class="ml-3 flex h-5 items-center">
          <input :id="`person-${person.id}`" :name="`person-${person.id}`" type="checkbox" class="h-4 w-4 rounded border-gray-300 text-indigo-600 focus:ring-indigo-500" />
        </div>
      </div>
    </div>
  </fieldset>
</template>

<script setup>
const people = [
  { id: 1, name: 'Annette Black' },
  { id: 2, name: 'Cody Fisher' },
  { id: 3, name: 'Courtney Henry' },
  { id: 4, name: 'Kathryn Murphy' },
  { id: 5, name: 'Theresa Webb' },
]
</script>