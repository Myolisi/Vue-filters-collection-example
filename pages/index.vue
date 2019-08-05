<template>
  <div>
    <div>{{pCapitalize}} | {{pCapitalize | capitalize}}</div>
    <div>{{pCapitalize}} | {{pCapitalize | capitalize('first')}}</div>
    <div>{{pDecapitalize}} | {{pDecapitalize | decapitalize}}</div>
    <div>{{pEntities}} | {{pEntities | htmlEntities}}</div>
    <div>{{pCamelcase}} | {{pCamelcase | camelcase}}</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      pCapitalize: "james may",
      pDecapitalize: "JAMES MAY",
      pEntities: "Hello &quot;james&quot; may",
      pCamelcase: "astaLavistaBaby"
    };
  },
  mounted() {
    console.log(this.$options.filters.capitalize(this.name)); //JAMES MAY
    //or
    console.log(this.$capitalize("james"));
  }
};
</script>
<style scoped>
</style>
