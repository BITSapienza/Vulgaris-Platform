<script>
export default {
	data: function() {
		return {
			errormsg: null,
			loading: false,
			some_data: ""
		}
	},
	methods: {
        data(){
        },
	},
	async mounted(){
		this.loading = true
		try{
            let response = await this.$axios.get(`/`);
            this.some_data=response.data
        } catch(e){
			this.loading = false
            this.errormsg = e.message
        }
		this.loading = false
	}
}
</script>

<template>
	<LoadingSpinner :loading="this.loading"/>
	<div>
		{{ this.some_data }}
	</div>
	<div v-if="errormsg">
		Error:
		<ErrorMsg :msg="errormsg"></ErrorMsg>
	</div>
</template>