<script setup>
import kitchenImage from '@/assets/images/kitchen.jpg';
import ArrowButtonKitchen from '@/components/common/ArrowButtonSection.vue';

defineProps({
    title: String,
    text: String
})
</script>

<template>
    <div class="kitchen-section d-flex flex-column justify-content-end"
        :style="{ backgroundImage: `url(${kitchenImage})` }">
        <div class="gradient-overlay"></div>
        <div class="content d-flex flex-row justify-content-between align-items-end">
            <div class="text d-flex flex-column align-items-center">
                <strong>{{ title }}</strong>
                <p>{{ text }}</p>
            </div>
            <ArrowButtonKitchen direction="right" />
        </div>
    </div>
</template>

<style scoped>
.kitchen-section {
    position: relative;
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    width: 100%;
    aspect-ratio: 644 / 515;
    border-radius: 4px;
    overflow: hidden;
}

.gradient-overlay {
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0;
    width: 100%;
    height: 257.5px;
    opacity: 0.8;
    background: linear-gradient(0deg, #141414 0%, rgba(20, 20, 20, 0.00) 100%);
    pointer-events: none;
    border-radius: 0 0 4px 4px;
    z-index: 1;
}

.content {
    position: relative;
    z-index: 2;
    margin: 0 24px 32px 24px;
}

.text {
    text-align: start;
    gap: 8px;
}

strong {
    color: var(--wit);
    font-family: "TT Commons Pro Bold";
    align-self: stretch;
    font-size: 28px;
    font-style: normal;
    font-weight: 600;
    line-height: 32px;
    letter-spacing: -0.56px;
}

p {
    color: var(--neutrals-soft-white);
    opacity: 0.5;
}

@media (max-width: 992px) {
    .kitchen-section {
        aspect-ratio: 352 / 468;
    }

    .text {
        width: 248px;
    }

    .gradient-overlay {
        height: 234px;
    }
}

@media (max-width: 600px) {
    .kitchen-section {
        aspect-ratio: 335 / 252;
        margin-bottom: 16px;
    }

    .content {
        margin: 0 16px 24px 16px;
    }

    strong {
        font-size: 23px;
        line-height: 24px;
        letter-spacing: -0.46px;
    }

    .gradient-overlay {
        height: 126px;
    }

    .text {
        width: 237px;
    }
}
</style>