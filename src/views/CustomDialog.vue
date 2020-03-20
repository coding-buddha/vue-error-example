<template>
  <div id="customDialog">
    <el-dialog title="Error Dialog Test By pasudo123" :visible.sync="computedIsOpen">
        IE 에서는 다이얼로그가 처음 까맣게 나타난다.
    </el-dialog>
  </div>
</template>

<script>

export default {
  name: 'CustomDialog',
  props: {
    isOpen: {
        type: Boolean,
        required: true,
        default: () => false
    }
  },
  computed: {
    computedIsOpen:{
        get(){
            return this.isOpen;
        },
        set(){
            this.close();
        }
    }
  },
  methods:{
      close(){
          this.$emit('closeDialog');
      }
  }
}
</script>