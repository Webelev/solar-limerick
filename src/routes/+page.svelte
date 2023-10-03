<!-- YOU CAN DELETE EVERYTHING IN THIS PAGE -->
<script>
	let Dråbe = '';
	let lov = '';
	let håbe = '';
	let håbeSkygge = '';
	let tingDerSkalKomme = '';
	let tingFarve = '';
	let rotering = '';

	let showLimerick = false;

	function generateLimerick() {
		showLimerick = !showLimerick;
		// Your limerick logic here
	}
</script>

<div class="container mx-auto">
	<div class="flex flex-col items-center">
		{#if showLimerick}
			<div>
				<p class="text-lg text-white">
					Som et strejf af en <span class="text-{Dråbe}-500 font-bold">Dråbe</span>
				</p>
				<p class="text-lg text-white">
					Har vi <span class="text-red-500 font-{lov}">lov</span> at
					<span class="text-{håbe}-{håbeSkygge} font-bold">Håbe</span>,
				</p>
				<p class="text-{tingDerSkalKomme}xl text-{tingFarve}-500">
					På de ting der skal <span class="font-bold">Komme</span>,
				</p>
				<p class="text-lg text-white rotate-{rotering}">
					Inden <span class="text-orange-500 font-thin">Livet</span> er
					<span class="text-indigo-500 font-bold">omme</span>.
				</p>
			</div>
		{/if}
		<section class="p-4">
			<label for="adjective">Farve:</label>
			<input
				type="text"
				on:input={() => (showLimerick = false)}
				bind:value={Dråbe}
				class="border rounded p-2 focus:ring focus:ring-blue-500 text-black"
			/>
			<label for="noun">Bogstavstørrelse:</label>
			<input
				type="text"
				on:input={() => (showLimerick = false)}
				bind:value={lov}
				
				class="border rounded p-2 focus:ring focus:ring-blue-500 text-black"
			/>
			<label for="noun">Farve:</label>
			<input
				type="text"
				on:input={() => (showLimerick = false)}
				bind:value={håbe}
				class="border rounded p-2 focus:ring focus:ring-blue-500 text-black"
			/>
			<label for="noun">Farvestyrke:</label>
			<input
				type="text"
				on:input={() => (showLimerick = false)}
				bind:value={håbeSkygge}
				class="border rounded p-2 focus:ring focus:ring-blue-500 text-black"
			/>
			<label for="noun">Skriftstørrelse:</label>
			<input
				type="text"
				on:input={() => (showLimerick = false)}
				bind:value={tingDerSkalKomme}
				class="border rounded p-2 focus:ring focus:ring-blue-500 text-black"
			/>
			<label for="noun">Linjefarve:</label>
			<input
				type="text"
				on:input={() => (showLimerick = false)}
				bind:value={tingFarve}
				class="border rounded p-2 focus:ring focus:ring-blue-500 text-black"
			/>
			<label for="noun">Rotation:</label>
			<input
				type="text"
				on:input={() => (showLimerick = false)}
				bind:value={rotering}
				class="border rounded p-2 focus:ring focus:ring-blue-500 text-black"
			/>

			<!-- Similar input fields for other words -->
		</section>
		<button
			on:click={generateLimerick}
			class="bg-blue-500 text-white p-2 rounded hover:bg-blue-700 focus:outline-none focus:ring focus:ring-blue-500"
			>Generate Limerick</button
		>
	</div>
</div>
