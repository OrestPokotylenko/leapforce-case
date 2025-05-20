<script setup>
import arrowLeft from '@/assets/icons/arrow-left.svg';
import arrowRight from '@/assets/icons/arrow-right.svg';

defineProps({
    direction: String,
    disabled: Boolean
})
</script>

<template>
    <div class="arrow-button-box d-flex justify-content-center align-items-center" :class="{ disabled }" :tabindex="disabled ? -1 : 0" :aria-disabled="disabled">
        <img class="arrow" :src="direction === 'left' ? arrowLeft : arrowRight" :alt="`Arrow ${direction}`">
    </div>
</template>

<style scoped>
.arrow-button-box {
    width: 56px;
    height: 56px;
    border: 2px solid var(--opacity-zwart-30);
    border-radius: 4px;
}

.arrow-button-box:hover {
    border-color: var(--opacity-zwart-50);
}

.arrow-button-box:active {
    border-color: var(--opacity-zwart-80);
}

.arrow-button-box.disabled {
    opacity: 0.3;
    cursor: not-allowed;
    pointer-events: none;
}

.arrow {
    width: 12px;
    height: 12px;
}

@media (max-width: 600px) {
    .arrow-button-box {
        width: 48px;
        height: 48px;
    }
}
</style>