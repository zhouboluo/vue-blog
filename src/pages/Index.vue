<template>
  <div class="index">
  	<el-row>
  		<el-col :span="16">
  			<div class="index-left">
  				<carousel></carousel>
  				<articles></articles>
          <pagination></pagination>
  			</div>
  		</el-col>
  		<el-col :span="8">
  			<div class="index-right">
  				
  			</div>
  		</el-col>
	</el-row>
  </div>
</template>

<script>

import Vue from 'vue'
import Carousel from 'components/Carousel'
import Articles from 'components/Articles'
import Pagination from 'components/Pagination'
import store from 'store'

export default {
  name: 'index',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  components:{
  	Carousel,Articles,Pagination
  }
}
</script>

<style>
  .index-left {
  	width: 100%;
  }  
</style>
