<script lang="ts">
	export let min: number | string | undefined = undefined;
	export let max: number | string | undefined = undefined;
	export let step: number | string | undefined = undefined;
	export let value: number | string = min ?? 0;
</script>

<label class="bg-slate-100 p-2 px-4 rounded-lg">
	<span class="text-sm font-semibold"><slot /></span>
	<input
		{...$$props}
		{min}
		{max}
		{step}
		type="number"
		bind:value
		class="w-full px-3 py-2 bg-white mt-1 rounded-md"
	/>
	<input {...$$props} {min} {max} {step} type="range" bind:value class="w-full" />
</label>
