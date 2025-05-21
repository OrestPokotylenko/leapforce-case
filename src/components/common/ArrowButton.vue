<script setup>
import ArrowLeftIcon from '@/components/icons/ArrowLeftIcon.vue';
import ArrowRightIcon from '@/components/icons/ArrowRightIcon.vue';

defineProps({
    direction: String,
    disabled: Boolean
})
</script>

<template>
    <div class="arrow-button-box d-flex justify-content-center align-items-center" :class="{ disabled }"
        :tabindex="disabled ? -1 : 0" :aria-disabled="disabled">
        <component :is="direction === 'left' ? ArrowLeftIcon : ArrowRightIcon" class="arrow" aria-hidden="true" />
    </div>
</template>

<style scoped>
.arrow-button-box {
    width: 56px;
    height: 56px;
    border: 2px solid var(--opacity-zwart-30);
    border-radius: 4px;
    cursor: pointer;
}

.arrow-button-box:hover {
    border-color: var(--opacity-zwart-50);
}

.arrow-button-box:active {
    border-color: var(--opacity-zwart-80);
}

.arrow-button-box.disabled {
    opacity: 0.3;
    cursor: default;
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