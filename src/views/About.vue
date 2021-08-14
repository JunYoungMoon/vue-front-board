<template>
  <div class="about">
    <h1>This is an about page</h1>
    <a href="javascript:;" @click="getList()">GET 방식 데이터 접근</a>
  </div>
</template>

<script>
export default {
	methods:{
		getList() {			
      this.$axios.get("http://localhost/api/board")
			.then((res)=>{
				console.log(res);
			})
			.then((err)=>{
				console.log(err);
			})
		}
	}
}
</script>
