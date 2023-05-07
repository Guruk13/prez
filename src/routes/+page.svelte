<script>

	let salutation = "Bonjour"
	let nom = "City School"; 

    let newItem ;	
    let todoList = []
	
	function proposerUnNombre() {

		if(newItem == "patate"){
			alert('Rien de tel qu\'une bonne purée!');
		}


		if(parseInt(newItem,10)){
			//à modifier pour gérer ✅ 🟰
			todoList = [...todoList, {text: newItem, emoji : "❌"}];
			


			// fin des modifs 
			newItem = '';

		}


	}
	
</script>

<div class="wrapper">
<h1>{salutation+" "+nom}</h1>

<input bind:value={newItem} type="text" placeholder="">
<button on:click={proposerUnNombre}>Proposer</button>

<br/>

{#each todoList as item, index}
	<div class="proposition">	
	<span >{item.text}</span>
	<span >{item.emoji}</span>
	<br/>
	</div>
{/each} 
</div>

<style> 
.wrapper{
	flex-direction:column;
	min-height:100vh;
	min-width:100vw;
	display:flex;
	align-items:center;
	justify-items:center;
}
button{
	position:relative;
	left:150px;
	top: -23px;
}

</style> 