<script>
//	export let name;
	import {web3} from 'svelte-web3'
	import Header from './Header.svelte';

	let sByte32="", sRawString="" , err = false;

	function fnCalcbyte32(){
		
		try{
			err = false;
		sByte32 = btos == 2 ? $web3.utils.numberToHex(sRawString) : 
							  $web3.utils.hexToNumber(sRawString)	;			 
		}
		catch(err){
			err = true;
			sByte32 = "Enter valid Value";	
		
		}
		
							}

	let btos = 2;

</script>
<!-- TODO: bg color mintcream-->
<main class="overflow-hidden  font-sans">
	<Header />

	<section class="overflow-x-hidden md:m-auto md:max-w-2/3 p-6 lg:py-4 lg:px-16" >
		<div class="my-4 flex items-center gap-8">
		
				<label>
					<input type=radio class="h-5 w-5 text-red-600" bind:group={btos} value={1}>
						Hex to Number
				</label>

				<label>
					<input type=radio class="h-5 w-5 text-red-600" bind:group={btos} value={2}>
						Number to Hex
				</label>
				</div>
		<p class="text-lg" >
			{#if btos == 1}
			Input Hex value to be converted into Number
			{:else}
			Input Number value to be converted into Hex
			{/if}
		</p>
			<div class="flex flex-col" >
				<div class="flex items-center flex-col md:flex-row " >
					<textarea  bind:value={sRawString} rows="4" cols="60" class="border-2 border-indigo-500 max-w-lg shadow-sm focus:ring-indigo-500 focus:border-indigo-500 mt-1 block w-full sm:text-sm border-gray-300 rounded-md" type="text"></textarea>
					<a on:click={fnCalcbyte32} class="self-center text-lg font-bold cursor-pointer m-4 p-4 border border-transparent shadow-sm rounded-md text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500" >
						Calculate
					</a>
				</div>
					
			</div>

			<div class="my-2 max-w-lg bg-white shadow-lg rounded-lg overflow-hidden p-6" >
				<h1 class="text-gray-900 font-extrabold text-2xl">
					{#if btos == 2}
					Hex
					{:else}
					Number
					{/if}

				</h1>	
				<p class="break-words font-normal p-6" class:myError="{err === true }" >{sByte32}</p>
			</div>

			
	</section>

</main>

<style>
	.myError{
		font-weight: 800;
		color: red;
		font-size: 2rem;

	}
</style>