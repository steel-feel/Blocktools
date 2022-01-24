<script>
    import { ethers } from "ethers";
    let value="";
  
    $: Hash = ethers.utils.id(value || "");

    function copytoClip(){
        navigator.clipboard.writeText(Hash);
        
    }

</script>

<div class="my-1" >
    <label class="text-gray-700" for="name">
        <textarea
            class="flex-1 appearance-none border border-gray-300 py-2 px-4 bg-white text-gray-700 placeholder-gray-400 rounded-lg text-base focus:outline-none focus:ring-2 focus:ring-purple-600 focus:border-transparent"
            id="comment"
            placeholder="Enter Text"
            name="comment"
            rows="5"
            cols="40"
            bind:value 
        />
    </label>
   
    <div class="flex flex-row">
     <div class="m-2">{Hash}</div>
   
     <button on:click="{copytoClip}" type="button" class="py-2 px-4 flex justify-center items-center  hover:bg-blue-700 focus:ring-blue-500 focus:ring-offset-blue-200 text-white w-full transition ease-in duration-200 text-center text-base font-semibold shadow-md focus:outline-none focus:ring-2 focus:ring-offset-2  w-12 h-12 rounded-lg ">
        <svg class="svg-icon" viewBox="0 0 20 20">
            <path d="M15.475,6.692l-4.084-4.083C11.32,2.538,11.223,2.5,11.125,2.5h-6c-0.413,0-0.75,0.337-0.75,0.75v13.5c0,0.412,0.337,0.75,0.75,0.75h9.75c0.412,0,0.75-0.338,0.75-0.75V6.94C15.609,6.839,15.554,6.771,15.475,6.692 M11.5,3.779l2.843,2.846H11.5V3.779z M14.875,16.75h-9.75V3.25h5.625V7c0,0.206,0.168,0.375,0.375,0.375h3.75V16.75z"></path>
        </svg>
    </button>
</div>




</div>
