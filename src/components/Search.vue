<template>
  <div class="hello">
    <input @change="onInputSearchChange"  v-model="searchText"/>
  </div>
</template>

<script>
    export default {
      name: 'HelloWorld',
      props: {
        msg: String
      },
      methods: {
        onInputSearchChange(){
          this.$emit('search',this.searchText)
        }
      },
      data() {
        return {
          searchText: ''  
        };
}
    }

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
