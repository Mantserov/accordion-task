<script setup>
import { items } from '~/vars/items';
</script>

<template>
  <div class="container">
    <div class="header">
      <Icon class="mr-2" name="mage:question-mark-circle" size="1.5em" />
      <p>FAQs</p>
    </div>
    
  <UAccordion class="mt-5" multiple :items="items">
    <template #default="{item, index, open }">
      <UButton color="gray" variant="ghost" class="mb-3 items-start flex flex-col text-left p-4 border bg-white rounded-md hover:bg-white hover:border-black transition duration-100 ease-linear">
        <div class="flex justify-between w-full">
          <span class="text-black">{{ item.label }}</span>
          <UIcon
              name="i-heroicons-chevron-down-20-solid"
              class="w-5 h-5 transform transition-transform duration-200"
              :class="[open && 'rotate-180']"
          />
        </div>
      <template v-if="open">
        <p class="mt-4 pt-3 text-slate-600 font-normal bg-white border-t">
          {{ item.description }}
        </p>
      </template>
      </UButton>
    </template>
  </UAccordion>
  </div>
</template>

<style>
.header {
  color: #333;
  display: flex;
  font-weight: bold;
  font-size: 18px;
}

.container {
  box-shadow: 0 0 2px rgba(0, 0, 0, 0.3);
  background-color: #fbfbfb;
  padding: 30px 40px 30px 40px;
  max-width: 95%;
  margin: 25px auto;
}
</style>
