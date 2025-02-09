The solution is to avoid using the `@apply` directive directly for the `display` property within the conditionally rendered component. Instead, apply the display styles directly or use a separate class that includes the display styles.  Here is an example solution in Vue.js:

```vue
<template>
  <div v-if="showComponent">
    <div class="flex items-center justify-center bg-blue-500 p-4">
      <p>This content will render correctly</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showComponent: true,
    };
  },
};
</script>
```

This approach ensures that the styles are applied consistently, regardless of conditional rendering. Applying the styles directly is often more efficient than using `@apply` for such cases.