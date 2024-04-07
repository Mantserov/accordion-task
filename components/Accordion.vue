<script setup>
import { items } from '~/vars/items';
</script>

<template>
  <div class="container">
    <div class="header">
      <Icon class="mr-2" name="mage:question-mark-circle" size="1.5em" />
      <p>FAQs</p>
    </div>
    <UAccordion
      class="accordion"
      variant="solid"
      size="xl"
      color="white"
      multiple
      :items="items"
    />
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
.accordion {
  margin-top: 20px;
}
</style>
