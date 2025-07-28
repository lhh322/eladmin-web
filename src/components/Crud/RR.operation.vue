<!--搜索与重置-->
<template>
  <span>
    <el-button class="filter-item" size="mini" type="success" icon="el-icon-search" @click="crud.toQuery(isArticle)">{{ searchText }}</el-button>
    <el-button v-if="crud.optShow.reset" class="filter-item" size="mini" type="warning" icon="el-icon-refresh-left" @click="crud.resetQuery()">{{ resetText }}</el-button>
  </span>
</template>
<script>
import { crud } from '@crud/crud'
export default {
  mixins: [crud()],
  props: {
    itemClass: {
      type: String,
      required: false,
      default: ''
    },
    searchText: {
      type: String,
      default: '搜索'
    },
    resetText: {
      type: String,
      default: '重置'
    },
    isArticle: {
      type: String,
      default: 'N'
    }
  }
}
</script>
