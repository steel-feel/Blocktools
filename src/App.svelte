<script>
	import { Tabs, TabList, TabPanel, Tab } from './tabs.js';
	import KeccahHash from './KeccahHash.svelte';
	
</script>

<main class="p-4" > 
<Tabs>
	<TabList>
		<Tab>Keccak Hash</Tab>
		<!-- <Tab>two</Tab>
		<Tab>three</Tab> -->
	</TabList>

	<TabPanel>
		<KeccahHash />
	</TabPanel>

	<TabPanel>
		<h2>Second panel</h2>
	</TabPanel>

	<TabPanel>
		<h2>Third panel</h2>
	</TabPanel>
</Tabs>

</main>