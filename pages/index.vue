<template>
  <div>
    <hello-world />
    <div>
      <default />
    </div>
  </div>
</template>

<script>
export default {
  components: {
    Default: () => import('@/components/Default.vue'),
    HelloWorld: () => import('@/components/HelloWorld.vue'),
  },
};
</script>
