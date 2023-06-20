<template>
  <div>
    <hello-world />
  </div>
</template>

<script>
export default {
  components: {
    HelloWorld: () => import('@/components/HelloWorld.vue'),
  },
};
</script>
