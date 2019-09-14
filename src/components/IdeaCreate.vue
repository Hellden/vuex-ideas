<template>
  <div>
    <h2>Create Idea</h2>
    <form @submit.prevent="create">
      <label for="idea-title">Idea's title</label><br />
      <input type="text" id="idea-title" v-model="title" />
      <button type="submit">Create</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: ""
    };
  },
  methods: {
    create() {
      const idea = {
        createAt: new Date(),
        title: this.title
      };
      // this.$store.commit("CREATE_IDEAS", idea);
      this.$store.dispatch("createIdea", idea);
      this.title = "";
    }
  }
};
</script>

<style lang="scss" scoped></style>
