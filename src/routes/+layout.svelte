<script lang="ts">
	import Modal from './modal.svelte';

	let showModal: boolean = false;
	let toggleModal = () => {
		showModal = !showModal;
	};
</script>

<Modal message="Hello, Ninjas!" {showModal} on:click={toggleModal} />
<nav>
	<a href="/">Home</a>
	<a href="/about">About</a>
	<a href="/login">Login</a>
    <button on:click|once={toggleModal}>Open Modal</button>
</nav>

<slot />

<footer>
	<p>Author: Joshua Edwards</p>
	<p>&copy;2022</p>
</footer>

<style>
	footer {
		text-align: center;
		vertical-align: bottom;
	}
</style>
