<script>
	let count = 0;

	function increment() {
		count += 1;
	}
</script>

<main>
	<div class="center-stage">
		<h1 class="count">{count}</h1>
	</div>

	<button on:click={increment}>
		Increment
	</button>
</main>

<style>
	/* Resetting body defaults to ensure full screen dark mode */
	:global(body) {
		margin: 0;
		padding: 0;
		background-color: #0f0f0f;
		color: #e0e0e0;
		font-family: system-ui, -apple-system, sans-serif;
	}

	main {
		height: 100vh; /* Full viewport height */
		display: flex;
		flex-direction: column;
		align-items: center;
		overflow: hidden;
	}

	.center-stage {
		flex: 1; /* Takes up all available vertical space */
		display: flex;
		align-items: center;
		justify-content: center;
		width: 100%;
	}

	.count {
		font-size: 12rem; /* Very large number */
		font-weight: 200;
		margin: 0;
		user-select: none; /* Prevents highlighting text when clicking fast */
		font-variant-numeric: tabular-nums; /* Prevents jitter as numbers change width */
	}

	button {
		margin-bottom: 3rem; /* Distance from the bottom edge */
		padding: 1rem 3rem;
		font-size: 1.25rem;
		background-color: #1f1f1f;
		color: #ffffff;
		border: 1px solid #333;
		border-radius: 8px;
		cursor: pointer;
		transition: all 0.2s ease;
		user-select: none;
	}

	button:hover {
		background-color: #2a2a2a;
		border-color: #555;
		transform: translateY(-2px);
		box-shadow: 0 4px 12px rgba(0, 0, 0, 0.5);
	}

	button:active {
		transform: translateY(0);
		background-color: #151515;
	}
</style>