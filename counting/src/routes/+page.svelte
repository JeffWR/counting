<script>
	let count = 0;

	function increment() {
		count += 1;
	}
</script>

<main>
	<h1 class="count">{count}</h1>
	
	<button on:click={increment}>
		INCREMENT
	</button>
</main>

<style>
	:global(body) {
		margin: 0;
		padding: 0;
		background-color: #0f0f0f;
		color: #e0e0e0;
		font-family: system-ui, -apple-system, sans-serif;
	}

	main {
		height: 100vh;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center; /* This centers the whole group vertically */
		gap: 2rem; /* Controls the distance between Number and Button */
		overflow: hidden;
	}

	.count {
		font-size: 12rem;
		font-weight: 200;
		line-height: 1; /* Tighter line height to reduce gap */
		margin: 0;
		user-select: none;
		font-variant-numeric: tabular-nums;
	}

	button {
		padding: 1rem 3rem;
		font-size: 1.5rem; /* Slightly larger text */
		font-weight: 900; /* "Fatter" font weight */
		letter-spacing: 1px;
		text-transform: uppercase;
		background-color: #1f1f1f;
		color: #ffffff;
		border: 2px solid #333; /* Slightly thicker border */
		border-radius: 12px;
		cursor: pointer;
		transition: all 0.1s ease; /* Faster transition for snappier feel */
		user-select: none;
	}

	button:hover {
		background-color: #2a2a2a;
		border-color: #666;
		transform: translateY(-2px);
	}

	button:active {
		transform: translateY(1px);
		background-color: #151515;
	}
</style>