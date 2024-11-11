<script setup>
import { ref } from 'vue';

const projects = ref([
  {
    title: 'Crowdfund',
    name: 'Funding rates page',
    price: 'Funding amount: $5,000 - $6,000',
    text: 'Grant will be used to build a dedicated web app to give traders a view of all dYdX asset funding rates across multiple timeframes. The page will be interactive to include deep diving across different assets and historical analysis of changing rates. It will also include API functionalities to allow developer access.',
    icons: ['icon1.svg', 'icon2.svg']
  },
  {
    title: 'Edition',
    name: 'Tradingview integration',
    price: 'Funding amount: $5,000 - $6,000',
    text: 'The grant will be used to build a web application that integrates Tradingview strategies into a dYdX Trading account to execute trades directly through a strategy. Users will be able to tap into Tradingview resources and test out different ...',
    icons: ['emoji.svg', 'icon2.svg','icon2.svg']
  },
  {
    title: 'Entry',
    name: 'Rewards optimization research and paper',
    price: 'Funding amount: $5,000 - $6,000',
    text: 'The Grant will be used to write a full research report and code samples that will determine optimal trading strategies for rewards maximization. The paper will be marketed across several platforms and shared among trading circles to help readership.',
    icons: ['icon1.svg', 'icon2.svg','icon2.svg']
  }
]);
</script>

<template>
  <div class="projects">
    <div class="project__block">
      <h1 class="project__block__title">Projects built with grants</h1>
      <p class="project__block__text">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque nulla risus, <br> consectetur ut bibendum non, gravida non libero.</p>
      <button class="project__block__btn">
        <span> View all funded projects</span>
        <img src="@/assets/icons/fi_arrow-right.svg" alt="">
      </button>
    </div>

    <div class="project__cards">
      <div v-for="(project, index) in projects" :key="index" class="project__card">
        <h2 class="project__card__title">{{ project.title }}</h2>
        <h3 class="project__card__name">{{ project.name }}</h3>
        <p class="project__card__price">{{ project.price }}</p>
        <p class="project__card__text">{{ project.text }}</p>
        <div class="project__card__icons">
          <img class="emoji" v-for="( idx) in project.icons" :key="idx" src="@/assets/icons/emoji.svg" alt="" />
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.projects {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 20px;
  padding: 12px;
}
.project__block__title {
  color: #FFFFFF;
  font-family: "CircularStd", cursive;
  font-weight: 700;
  font-size: 40px;
  text-align: center;
}
.project__block__text {
  color: #C8C7D8;
  font-size: 18px;
  font-family: "CircularStd", cursive;
  text-align: center;
  font-weight: 400;
  margin-top: 16px;
}
.project__block {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.project__block__btn {
  display: flex;
  align-items: center;
  color: #6966FF;
  font-family: CircularStd;
  font-weight: 400;
  font-size: 18px;
  border: none;
  background: none;
  padding-top: 24px;
  cursor: pointer;
}
.project__block__btn span {
  margin-right: 8px;
}
.project__cards {
  display: flex;
  gap: 24px;
  margin-top: 20px;
}

.project__card {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  padding: 24px;
  background:#393953;
  border-radius: 8px;
  height: 560px;
  max-width: 400px;
}

.project__card__title {
  color: #A59EBA;
  font-family: "Work Sans";
  font-size: 16px;
  font-weight: 400;
}
.project__card__name {
  color: #FFFFFF;
  font-weight: 700;
  font-size: 24px;
  font-family: CircularStd, cursive;
  margin-top: 16px;
}
.project__card:nth-child(1), .project__card:nth-child(3) {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
}

.project__card:nth-child(2) {
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  height: 390px;
  margin-top: 170px;
}
.project__card__price {
  color: #A59EBA;
  font-weight: 400;
  font-size: 16px;
  font-family: "Work Sans", sans-serif;
  margin-top: 16px;
}
.project__card__text {
  color: white;
  font-family: CircularStd;
  font-size: 16px;
  font-weight: 450;
  margin-top: 16px;
}

.project__card__icons {
  display: flex;
  gap: 8px;
  margin-top: auto;
}
.project__card__icons {
  display: flex;
  position: relative;
  bottom: 30px;
  margin-top: auto;
}

.emoji {
  border-radius: 50%;
  position: absolute;
}

.emoji:nth-child(1) {
  left: 0;
}

.emoji:nth-child(2) {
  left: 25px;
}

.emoji:nth-child(3) {
  left: 50px;
}
@media (max-width: 900px) {
  .project__card:nth-child(3), .project__card:nth-child(2) {
    display: none;
  }
  .projects {
    padding: 32px;
  }
  .project__block__title {
    font-size: 24px;
  }
  .project__block__text {
    font-size: 16px;
  }
  .project__block__btn {
    margin-bottom: 48px;
  }
  .project__card {
    height: 450px;
  }
  .project__card__price {
    padding-right: 80px;
  }
}
</style>