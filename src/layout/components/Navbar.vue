<template>
  <div class="navbar" flex="justify:between align:center">
    <div class="right-menu" flex="align:center">
      <slot name="left">
      </slot>
    </div>
    <div class="right-menu" flex="align:center">
      <slot name="right">
      </slot>
    </div>
  </div>
</template>

<script>

export default {
  created() {
  },
  methods: {
  }
}
</script>

<style lang="scss" scoped>
	.navbar {
		height: $headerHeight;
		overflow: hidden;
		position: relative;
		background: $whiteColor;
		box-shadow: 0px 2px 10px 0px rgba(0, 0, 0, 0.1);
		padding: 0 30px;

		.right-menu {
			height: 100%;

			&:focus {
				outline: none;
			}
		}
	}
</style>
