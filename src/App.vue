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
    <div class="d-flex justify-content-center content">
        <div class="grid-container">
            <p class="label">{{ label }}</p>
            <h1>
                {{ titleBefore }} <span class="call-to-action">{{ callToAction }}</span> {{ titleAfter }}
            </h1>
            <p class="body">{{ body }}</p>
            <OptionalButton class="optional-button" :text="optionalButtonText" />
            <KitchenSection class="kitchen-section" :title="section1Title" :text="section1Text" />
            <KitchenSection class="kitchen-section" :title="section2Title" :text="section2Text" />
        </div>
    </div>
</template>

<style scoped>
.content {
    text-align: center;
    margin-top: 64px;
}

.grid-container {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    column-gap: 24px;
    max-width: 1600px;
    padding: 0 64px;
    width: 100%;
    box-sizing: border-box;
    margin-bottom: 96px;
}

h1 {
    font-family: 'TT Commons Pro Bold';
    color: var(--header-zwart);
    grid-column: 4 / span 6;
    text-align: center;
    font-size: 40px;
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
    white-space: nowrap;
}

p {
    text-align: center;
}

.label {
    color: var(--main-colors-groengrijs);
    grid-column: 4 / span 6;
    font-size: 15px;
    line-height: 16px;
    letter-spacing: 0.3px;
    margin-bottom: 8px;
}

.body {
    color: var(--body-zwart);
    grid-column: 3 / span 8;
    opacity: 0.8;
    margin: 24px 0;
}

.kitchen-section {
    grid-column: span 6;
}

.optional-button {
    grid-column: 4 / span 6;
    justify-self: center;
    margin-bottom: 80px;
}

@media (max-width: 992px) {
    .content {
        margin-top: 64px;
    }

    .grid-container {
        column-gap: 16px;
        padding: 0 24px;
    }

    .label {
        grid-column: 2 / span 10;
    }

    h1 {
        grid-column: 2 / span 10;
    }

    .body {
        grid-column: 1 / span 12;
    }

    .optional-button {
        margin-bottom: 48px;
    }
}

@media (max-width: 600px) {
    .content {
        margin-top: 48px;
    }

    .grid-container {
        grid-template-columns: repeat(6, 1fr);
        column-gap: 12px;
        padding: 0 20px;
        margin-bottom: 64px;
    }

    .label {
        grid-column: 1 / span 6;
        font-size: 14px;
        letter-spacing: 0.28px;
        line-height: 16px;
    }

    h1 {
        grid-column: 1 / span 6;
        font-size: 36px;
        line-height: 40px;
        letter-spacing: -0.72px;
        align-self: start;
    }

    .call-to-action {
        font-size: 38px;
        line-height: 40px;
        letter-spacing: -1.14px;
        white-space: normal;
    }

    .body {
        grid-column: 1 / span 6;
        margin: 16px 0;
    }

    .optional-button {
        grid-column: 2 / span 4;
        margin-bottom: 32px;
    }
}
</style>