<template>
  <!-- 分页组件 -->
  <el-pagination
    :background="true"
    :current-page="pageable.pageNum"
    :page-size="pageable.pageSize"
    :page-sizes="[10, 25, 50, 100]"
    :total="pageable.total"
    layout="total, sizes, prev, pager, next, jumper"
    @size-change="handleSizeChange"
    @current-change="handleCurrentChange"
  ></el-pagination>
</template>

<script setup name="Pagination">
defineProps({
  handleSizeChange: {
    type: Function,
    default: () => {},
    required: true
  },
  handleCurrentChange: {
    type: Function,
    default: () => {},
    required: true
  },
  pageable: {
    type: Object,
    default: () => {
      return {
        pageNum: 1,
        pageSize: 10,
        total: 0
      };
    },
    required: true
  }
});
</script>
