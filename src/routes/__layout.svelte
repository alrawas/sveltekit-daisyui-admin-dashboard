<script>
	import '../app.css';
	import Navbar from '$lib/components/Navbar.svelte';
	import Footer from '$lib/components/Footer.svelte';
</script>

<div class="drawer">
	<input id="my-drawer-3" type="checkbox" class="drawer-toggle" />
	<div class="drawer-content flex flex-col">
		<!-- Navbar -->
		<Navbar />
		<!-- Page content here -->
		<slot />
		<Footer />
	</div>
  <!-- Sidebar on mobile here -->
	<div class="drawer-side">
		<label for="my-drawer-3" class="drawer-overlay" />
		<ul class="menu p-4 overflow-y-auto w-80 bg-base-100">
			<!-- Sidebar content here -->
			<li>
				<a
					on:click={() => {
						document.getElementById('my-drawer-3').click();
					}}
					href="/">Home</a
				>
			</li>
			<li>
				<a
					on:click={() => {
						document.getElementById('my-drawer-3').click();
					}}
					href="/about">About</a
				>
			</li>
		</ul>
	</div>
</div>
