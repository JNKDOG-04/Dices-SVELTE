<script>
	let diceLeft = "assets/images/dice1.png";
	let diceRight = "assets/images/dice2.png";
	let numberOne = 1;
	let numberTwo = 2;

	function takeDices(){
		numberOne = Math.floor(Math.random()*6)+1;
		numberTwo = Math.floor(Math.random()*6)+1;

		diceLeft = "assets/images/dice" + numberOne + ".png";
		diceRight = "assets/images/dice" + numberTwo + ".png";
	}
</script>

<main>
	<h1>Dices with SVELTE</h1>
	<div class="jumbotron text-center">
		<div class="btn btn-success lg" on:click= {takeDices}>Take Dices</div>
		<br/>
		<img src={diceLeft} alt="Dice one" class="image">
		<img src={diceRight} alt="Dice two" class="image">
		{#if numberOne == numberTwo}
		<h1><span class="badge badge-success">😎😛YOU WIN!!😛😎</span></h1>
		{/if}
	</div>
</main>

<style>
	main {
		height: 100vh;
		background-color: #e9ecef;
	}

	h1 {
		text-align: center;
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	.image {
		width: 300px;
		height: 300px;
		background-color: red;
		margin: 30px;
		border-radius: 20px;
	}

	.badge-success{
		color: #eafa06;
		background-color: #ff3e00;
	}
</style>