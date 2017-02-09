<template>
  <div class="pagination">
    <el-pagination layout="prev, pager, next" :page-size="2" :total="articleList.length" @current-change="curPageChange">
    </el-pagination>
  </div>
</template>

<script>

export default {
  name: 'pagination',
  data () {
    return {
      articleList:this.$store.state.articleList
    }
  },
   mounted: function(){
    var _this = this;
    this.$nextTick(function () {
      console.log("mounted:"+_this.articleList);
    })
  },
  watch: {
    articleList: function(){
      console.log("watch:"+this.articleList);
    }
  },
  methods:{
    curPageChange: function(currentPage){
      this.$store.state.curPage = currentPage;
      console.log(currentPage); 
      console.log();
    }
  }
}
</script>

<style>
 
</style>
