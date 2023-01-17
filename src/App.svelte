<script>
	import viewport from './useViewportAction';
</script>

<div style="height: 200px; background: red;" />
<div style="height: 200px; background: blue;" />
<div style="height: 200px; background: green;" />
<div style="height: 200px; background: red;" />
<div style="height: 200px; background: blue;" />
<div style="height: 200px; background: green;" />

<h1 use:viewport
		on:enterViewport={() => console.log('enter!')}
		on:exitViewport={() => console.log('exit!')}
>
	Hello World!
</h1>

<div style="height: 200px; background: red;" />
<div style="height: 200px; background: blue;" />
<div style="height: 200px; background: green;" />
<div style="height: 200px; background: red;" />

<img
		 use:viewport
		 on:enterViewport={(e) => e.target.classList.add("blur-in")}
		 on:exitViewport={(e) => e.target.classList.remove("blur-in")}
		 src="/images/camera.gif"
     class="opacity-0"
     alt=""
/>

<div style="height: 200px; background: blue;" />
<div style="height: 200px; background: green;" />
<div style="height: 200px; background: red;" />
<div style="height: 200px; background: blue;" />
<div style="height: 200px; background: green;" />