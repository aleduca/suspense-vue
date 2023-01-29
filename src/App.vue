<template>
  <Suspense>
    <template #default>
      <component :is="view ? SuspenseTest : Test"></component>
      <!-- <SuspenseTest></SuspenseTest> -->
    </template>
    <template #fallback>
      <component :is="view ? SuspenseSkeleton : TestSkeleton"></component>
      <!-- <SuspenseSkeleton></SuspenseSkeleton> -->
    </template>
  </Suspense>
</template>
<script setup>
  import {ref} from 'vue';
  import SuspenseTest from './components/SuspenseTest.vue';
  import SuspenseSkeleton from './components/SuspenseSkeleton.vue';
  import TestSkeleton from './components/TestSkeleton.vue';
  import Test from './components/Test.vue';

  const view = ref(true);
</script>