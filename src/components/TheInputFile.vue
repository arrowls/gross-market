<script setup>
import ThePaperClip from './svg/ThePaperClip.vue';

const props = defineProps({
	placeholder: {
		type: String,
		default: '',
	},
});
</script>

<template>
	<label class="form-file__wrapper field">
		<input type="file" class="form-file" :placeholder="props.placeholder" />
		<div class="form-file__image">
			<ThePaperClip />
		</div>
		<div class="form-file__text">выберете или перетащите файл</div>
	</label>
</template>

<style lang="scss">
.form-file {
	display: none;

	&__wrapper {
		display: flex;
		gap: 12px;
	}

	&__text {
		color: $silver-color;
	}
}
</style>
