<template>
  <el-row>
    <el-col :span="20">
      <receipt-list />
    </el-col>
    <el-col :span="4">
      <el-button
        type="primary"
        icon="el-icon-plus"
        @click="openForm"
      >
        Create
      </el-button>
    </el-col>

    <receipt-form
      ref="form"
    />
  </el-row>
  
</template>

<script>
import ReceiptForm from './Form'
import ReceiptList from './List'

export default {
  components: {
    ReceiptForm,
    ReceiptList
  },

  methods: {
    openForm() {
      this.$refs.form.openDialog()
    }
  }
}
</script>