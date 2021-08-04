<template>
	<div >
		<b-container class="b-container" fluid>
			<b-card class="card" header="ADD TODO"
                        header-text-variant="white"
                        header-tag="header"
                        header-bg-variant="dark"
                         style="max-width: 35rem " >
					<b-form>
				<b-form-textarea id="b-form-input" type="text" v-model="newTodoItem" width="100px" />
				<br>
				
				<b-button id="popover-target-1" variant="danger" @click="addNewTodoItem()">Submit</b-button>
 <b-popover target="popover-target-1" triggers="hover" placement="bottom">
 
    Add your <b>Todo</b> to list!
  </b-popover>
			</b-form>
		</b-card>
		</b-container>

	

		

	</div>
</template>

<script>
export default {
	data(){
		return{
		newTodoItem: ""
	}
	},
	methods: {
		addNewTodoItem(){
			this.$store.dispatch('addNewTodo',this.newTodoItem)
			this.newTodoItem="";
		}
	}

}
</script>

<style scoped>
.card{
  width: 30%;
  margin-left: 36%;
  position: relative;
  justify-content: center;
  background-color:rgb(235, 198, 119);
 
}
.b-container{
   margin-top: 50px;
}
</style>