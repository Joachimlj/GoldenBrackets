<template>
	<header class="app-header py-3 bg-green shadow sm:shadow-md md:shadow lg:shadow">
		<section class="container">
			<h1 class="font-normal uppercase text-black text-xl tracking-wide"> {{ brandTitle }} </h1>
		</section>
	</header>
</template>

<script>
export default {
  name: 'TheHeader',
  data () {
    return {
      brandTitle: 'Golden Brackets',
    }
  }
}
</script>
