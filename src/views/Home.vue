<template>
  <el-table :data="tableData" style="width: 100%" highlight-current-row @current-change="handleCurrentChange" :row-class-name="tableRowClassName">
    <el-table-column fixed prop="code" label="基金编号" min-width="80"></el-table-column>
    <el-table-column prop="name" label="基金名称" min-width="120"></el-table-column>
    <el-table-column prop="province" label="成本价" min-width="120"></el-table-column>
    <el-table-column prop="city" label="估算净值" min-width="120"></el-table-column>
    <el-table-column prop="city" label="持有份额" min-width="120"></el-table-column>
    <el-table-column prop="address" label="基金总价值" min-width="300"></el-table-column>
    <el-table-column prop="zip" label="持有收益率" min-width="120"></el-table-column>
    <el-table-column prop="zip" label="持有收益" min-width="120"></el-table-column>
    <el-table-column prop="zip" label="涨跌幅" min-width="120"></el-table-column>
    <el-table-column prop="zip" label="估算收益" min-width="120"></el-table-column>
    <el-table-column prop="date" label="更新时间" min-width="120"></el-table-column>
  </el-table>
</template>

<style lang="stylus">
.el-table
  th
    text-align center
  .success-row
    background #f0f9eb
  .warning-row
    background oldlace
</style>
<script>
export default {
  methods: {
    tableRowClassName({row, rowIndex}) {
      if (rowIndex === 1) {
        return 'success-row';
      } else if (rowIndex === 2) {
        return 'warning-row';
      }
      return '';
    },
    setCurrent(row) {
      this.$refs.singleTable.setCurrentRow(row);
    },
    handleCurrentChange(val) {
      this.currentRow = val;
    }
  },
  data() {
    return {
      tableData: [{
        code: '001006',
        date: '2016-05-03',
        name: '王小虎',
        province: '上海',
        city: '普陀区',
        address: '上海市普陀区金沙江路 1518 弄',
        zip: 200333
      }, {
        date: '2016-05-02',
        name: '王小虎',
        province: '上海',
        city: '普陀区',
        address: '上海市普陀区金沙江路 1518 弄',
        zip: 200333
      }, {
        date: '2016-05-04',
        name: '王小虎',
        province: '上海',
        city: '普陀区',
        address: '上海市普陀区金沙江路 1518 弄',
        zip: 200333
      }, {
        date: '2016-05-01',
        name: '王小虎',
        province: '上海',
        city: '普陀区',
        address: '上海市普陀区金沙江路 1518 弄',
        zip: 200333
      }, {
        date: '2016-05-08',
        name: '王小虎',
        province: '上海',
        city: '普陀区',
        address: '上海市普陀区金沙江路 1518 弄',
        zip: 200333
      }, {
        date: '2016-05-06',
        name: '王小虎',
        province: '上海',
        city: '普陀区',
        address: '上海市普陀区金沙江路 1518 弄',
        zip: 200333
      }, {
        date: '2016-05-07',
        name: '王小虎',
        province: '上海',
        city: '普陀区',
        address: '上海市普陀区金沙江路 1518 弄',
        zip: 200333
      }]
    }
  }
}
</script>
