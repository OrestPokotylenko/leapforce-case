<script setup>
import ArrowButton from '@/components/common/ArrowButton.vue';
import OptionalButton from '@/components/common/OptionalButton.vue';
import KitchenSection from '@/components/sections/KitchenSection.vue';

const label = 'Label';
const titleBefore = 'Mandatory title about the';
const callToAction = 'call-to-action';
const titleAfter = 'here';
const body = 'Optional body copy goes here.';
const optionalButtonText = 'Optional button';
const kitchenSectionTitle = 'Title';
const kitchenSectionText = 'Supporting text about the call-to-action goes here.';
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
        <KitchenSection class="kitchen-section" :title="kitchenSectionTitle"
            :text="kitchenSectionText" />
        <KitchenSection class="kitchen-section" :title="kitchenSectionTitle"
            :text="kitchenSectionText" />
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
    color: #212121;
    text-align: center;
    font-family: "TT Commons Pro";
    font-size: 40px;
    font-style: normal;
    font-weight: 600;
    line-height: 48px;
    letter-spacing: -1.2px;
}

.call-to-action {
    color: #212121;
    font-family: "GT Alpina";
    font-size: 42px;
    font-style: normal;
    font-weight: 300;
    line-height: 48px;
    letter-spacing: -1.26px;
}

p {
    color: #1E2526;
    text-align: center;
    font-family: "TT Commons Pro";
    font-style: normal;
    font-weight: 450;
    margin: 0;
}

.label {
    font-size: 15px;
    line-height: 16px;
    letter-spacing: 0.3px;
    margin-bottom: 8px;
}

.body {
    font-size: 19px;
    line-height: 24px;
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
        font-size: 17px;
        margin: 16px 0;
    }
}
</style>