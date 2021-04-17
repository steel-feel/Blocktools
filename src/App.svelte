<script>
//	export let name;
	import Header from './Header.svelte';

	let sByte32="adasd", sRawString="" ;

	function fnCalcbyte32(){

	}

</script>

<main class="font-sans">
	<Header />

	<section class="m-auto p-6 lg:py-4 lg:px-16" >
		<p class="text-lg" >Input the String value to be converted into byte32</p>
			<div class="flex flex-col" >
				<div class="flex items-center flex-col md:flex-row " >
					<textarea bind:value={sRawString} rows="4" cols="60" class="max-w-lg shadow-sm focus:ring-indigo-500 focus:border-indigo-500 mt-1 block w-full sm:text-sm border-gray-300 rounded-md" type="text"></textarea>
					<a on:click={fnCalcbyte32} class="self-center font-bold cursor-pointer m-4 p-4 border border-transparent shadow-sm text-sm font-medium rounded-md text-white bg-indigo-600 hover:bg-indigo-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500" >
						Calculate
					</a>
				</div>
				

				
				<div class="my-8 " >
					<p class="p-6 border-solid border-2 border-indigo-500" >{sByte32}</p>
				</div>
			</div>
	</section>

</main>

<style>

</style>