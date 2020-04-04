<template>
  <div>
    <TestComponent />
  </div>
</template>

<script>
import test from '~/articles/readme-github.md';
export default {
  components: {
    TestComponent: test.vue.component,
  },
};
</script>
