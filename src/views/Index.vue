<template>
  <div id="index">
    <button @click=openDialog>
        Button
    </button>
    <div>
        <custom-dialog 
            v-bind:isOpen="isOpen"
            v-on:closeDialog="closeDialog"/>
    </div>
  </div>
</template>

<script>

import CustomDialog from './CustomDialog';

export default {
  name: 'Index',
  components: { CustomDialog },
  data() {
      return {
          isOpen: false
      }
  },
  methods: {
      openDialog(){
        this.isOpen = true;
      },
      closeDialog() {
          this.isOpen = false;
      }
  }
}
</script>