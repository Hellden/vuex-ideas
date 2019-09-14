<template>
  <div>
    <h1>Welcome Ideas.io</h1>
    <IdeaCreate />
    <Ideas />
  </div>
</template>

<script>
import IdeaCreate from "@/components/IdeaCreate.vue";
import Ideas from "@/components/Ideas.vue";

export default {
  components: {
    IdeaCreate,
    Ideas
  }
};
</script>

<style lang="scss" scoped></style>
