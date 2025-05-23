<script setup>
import OptionalButton from '@/components/common/OptionalButton.vue';
import KitchenSection from '@/components/sections/Section.vue';

const label = 'Why choose us?';
const titleBefore = 'Get the help you need from';
const callToAction = 'certified local professionals';
const titleAfter = 'you can trust';
const body = 'We design and develop websites that not only look beautiful but drive real results. Let’s take your digital presence to the next level.';
const optionalButtonText = "Let's talk";
const section1Title = 'Website Development';
const section1Text = 'Custom-built websites tailored to your business needs with a focus on speed, SEO, and conversion.';
const section2Title = 'Digital Strategy';
const section2Text = 'We help you define a digital roadmap to achieve your goals — from marketing automation to content strategy.';
</script>

<template>
    <div class="grid-container">
        <div class="header">
            <p class="label">{{ label }}</p>
            <h1>
                {{ titleBefore }} <span class="call-to-action">{{ callToAction }}</span> {{ titleAfter }}
            </h1>
            <p class="body">{{ body }}</p>
            <OptionalButton :text="optionalButtonText" />
        </div>
        <KitchenSection class="kitchen-section" :title="section1Title" :text="section1Text" />
        <KitchenSection class="kitchen-section" :title="section2Title" :text="section2Text" />
    </div>
</template>

<style scoped>
.grid-container {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    column-gap: 24px;
    max-width: 1600px;
    margin: 0 auto;
    padding-left: 64px;
    padding-right: 64px;
    width: 100%;
    box-sizing: border-box;
    margin-bottom: 96px;
}

.header {
    grid-column: 5 / span 4;
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    margin: 64px 0 80px 0;
}

h1 {
    color: var(--header-zwart);
    text-align: center;
    font-size: 40px;
    font-style: normal;
    font-weight: 600;
    line-height: 48px;
    letter-spacing: -1.2px;
}

.call-to-action {
    color: var(--header-zwart);
    font-family: "GT Alpina";
    font-size: 42px;
    font-style: normal;
    font-weight: 300;
    line-height: 48px;
    letter-spacing: -1.26px;
}

p {
    text-align: center;
}

.label {
    color: var(--main-colors-groengrijs);
    font-size: 15px;
    line-height: 16px;
    letter-spacing: 0.3px;
    margin-bottom: 8px;
}

.body {
    color: var(--body-zwart);
    opacity: 0.8;
    margin: 24px 0;
}

.kitchen-section {
    grid-column: span 6;
}

@media (max-width: 992px) {
    .grid-container {
        padding-left: 32px;
        padding-right: 32px;
    }

    .header {
        grid-column: 3 / span 8;
        margin: 64px 0 48px 0;
    }
}

@media (max-width: 600px) {
    .grid-container {
        grid-template-columns: repeat(6, 1fr);
        column-gap: 12px;
        padding-left: 20px;
        padding-right: 20px;
        margin-bottom: 64px;
    }

    .header {
        grid-column: 1 / span 6;
        margin: 48px 0 32px 0;
        padding: 0 16px;

    }

    .label {
        font-size: 14px;
        letter-spacing: 0.28px;
    }

    h1 {
        font-size: 36px;
        line-height: 40px;
        letter-spacing: -0.72px;
    }

    .call-to-action {
        font-size: 38px;
        line-height: 40px;
        letter-spacing: -1.14px;
    }

    .body {
        margin: 16px 0;
    }
}
</style>