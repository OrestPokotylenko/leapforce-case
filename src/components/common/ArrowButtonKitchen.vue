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
    min-width: 56px;
    min-height: 56px;
    border: 2px solid var(--opacity-wit-30);
    border-radius: 4px;
    cursor: pointer;
    margin-left: 10px;
}

.arrow {
    color: var(--neutrals-wit);
}

@media (max-width: 600px) {
    .arrow-button-box {
        width: 48px;
        height: 48px;
    }
}
</style>