<template>
  <div class="selector" v-focus>
    <SelectorInput
      :placeholder="placeholder"
    />
  </div>
</template>

<script>

import SelectorInput from './input.vue';
import focus from '../../../directive/focus';

export default {
  name: 'Selector',
  components:{
    SelectorInput
  },
  props:{
    placeholder: String
  },
  directives:{
    focus
  }
}

</script>

<style scoped>

.selector{
  width: 300px;
  position: relative;
}

</style>
