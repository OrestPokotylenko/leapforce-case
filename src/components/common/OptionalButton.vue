<script setup>
import ArrowRightIcon from '@/components/icons/ArrowRightIcon.vue';
defineProps({
    text: String,
    disabled: Boolean
})
</script>

<template>
    <div class="button" :class="{ disabled }" :tabindex="disabled ? -1 : 0" :aria-disabled="disabled">
        <p class="content">{{ text }}</p>
        <ArrowRightIcon class="arrow" />
    </div>
</template>

<style scoped>
.button {
    display: flex;
    flex-direction: row;
    align-items: center;
}

.content {
    color: var(--main-colors-oranje-rood);
    font-family: "TT Commons Pro";
    font-size: 17px;
    font-style: normal;
    font-weight: 450;
    line-height: 24px;
    margin: 0;
    margin-right: 4px;
    cursor: pointer;
}

.arrow {
    color: var(--main-colors-oranje-rood);
    margin: 6px;
}

.button:hover .content,
.button:hover .arrow {
    color: var(--interactive-oranje-rood-hover);
}

.button:active .content,
.button:active .arrow {
    color: var(--interactive-oranje-rood-focussed);
}

.button.disabled .content,
.button.disabled .arrow {
    color: var(--neutrals-zwart);
    opacity: 0.3;
    cursor: default;
}
</style>