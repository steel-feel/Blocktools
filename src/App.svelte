<script>
//	export let name;
	import {web3} from 'svelte-web3'
	import Header from './Header.svelte';

	let sByte32="", sRawString="" ;

	function fnCalcbyte32(){
		// console.log(Object.keys($web3))
		sByte32 = $web3.utils.utf8ToHex(sRawString).padEnd(66, "0");
	}

	////Web3.utils.hexToNumberString('0x989680')

</script>
<!-- TODO: bg color mintcream-->
<main class="overflow-hidden  font-sans">
	<Header />

	<section class="overflow-x-hidden md:m-auto md:max-w-2/3 p-6 lg:py-4 lg:px-16" >
		<div class="flex items-center gap-8">
			<label class="inline-flex items-center">
				<input type="radio" name="v" class="h-5 w-5 text-red-600"/>
					<span class="ml-2 text-gray-700">
						String to byte32
					</span>
				</label>
				<label class="inline-flex items-center">
					<input type="radio" name="v" class="h-5 w-5 text-red-600"/>
						<span class="ml-2 text-gray-700">
						byte32 to String
						</span>
					</label>
				</div>
		<p class="text-lg" >Input the String value to be converted into byte32</p>
			<div class="flex flex-col" >
				<div class="flex items-center flex-col md:flex-row " >
					<textarea bind:value={sRawString} rows="4" cols="60" class="max-w-lg shadow-sm focus:ring-indigo-500 focus:border-indigo-500 mt-1 block w-full sm:text-sm border-gray-300 rounded-md" type="text"></textarea>
					<a on:click={fnCalcbyte32} class="self-center text-lg font-bold cursor-pointer m-4 p-4 border border-transparent shadow-sm rounded-md text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500" >
						Calculate
					</a>
				</div>
					


				<!-- {#if sByte32} -->
				<!-- <div class="my-8 uppercase text-lg font-bold" >
						
					<p class="break-words font-normal p-6 border-solid border-2 border-indigo-500" >{sByte32}</p>
				</div> -->



				


				


				<!-- {/if} -->
			</div>
			<!-- <div class="flex max-w-lg bg-white shadow-lg rounded-lg overflow-hidden">
				<div class="p-4">
					<h1 class="text-gray-900 font-bold text-2xl">
						byte32 String
					</h1>

					<p class="overflow-hidden break-words mt-2 text-gray-600 text-md">
						{sByte32}
					</p>
				</div>
			</div> -->



			<div class="max-w-lg bg-white shadow-lg rounded-lg overflow-hidden p-6" >
				<h1 class="text-gray-900 font-bold text-2xl">
					byte32 String
				</h1>	
				<p class="break-words font-normal p-6" >{sByte32}</p>
			</div>

			
	</section>

</main>

<style>

</style>