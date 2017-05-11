# Project Carboneum

*Carboneum* - is a lightweight library to create your own custom HTML elements, using web standard [Web Component](https://www.w3.org/standards/techs/components#w3c_all) API.

###### *Example:*
```html
<template>
	<style>
		/* styles */
	</style>
	<input type="text" value="this.userName" oninput="::this.userName = this.value">
	[[this.userName]]
</template>
<script type="text/javascript">
	class HelloApp extends Custom.Element {
		static get is () { return 'hello-app' }
		static get observedProperties () { return ['userName'] }

		constructor() {
			super()
			this.userName = 'Arthur'
		}
	}
	window.customElements.define(HelloApp.is, HelloApp.element)
</script>
```
