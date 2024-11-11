<script setup>
</script>

<template>
  <div class="news">
    <div class="news__block">
      <h1 class="news__block__title">What’s new?</h1>
      <p class="news__block__text">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque nulla risus, <br>
        consectetur ut bibendum non, gravida non libero.
      </p>
      <button class="news__block__btn">
        <span>Read more on our blog</span>
        <img src="@/assets/icons/fi_arrow-right.svg" alt="">
      </button>
    </div>

    <div class="news__cards">
      <div class="news__card">
        <img class="news__card__image" src="@/assets/img/img.png" alt="">
        <div class="news__card__content">
          <h3 class="news__card__name">Funding round</h3>
          <p class="news__card__title">Round 9 of approvals</p>
        </div>
        <div class="news__card__date">January 1, 2022</div>
      </div>
      <div class="news__card">
        <img class="news__card__image" src="@/assets/img/img.png" alt="">
        <div class="news__card__content">
          <h3 class="news__card__name">Funding round</h3>
          <p class="news__card__title">Round 9 of approvals</p>
        </div>
        <div class="news__card__date">January 1, 2022</div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.news {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 20px;
  padding: 12px;
}

.news__block__title {
  color: #FFFFFF;
  font-family: "CircularStd", cursive;
  font-weight: 700;
  font-size: 40px;
  text-align: center;
}

.news__block__text {
  color: #C8C7D8;
  font-size: 18px;
  font-family: "CircularStd", cursive;
  text-align: center;
  font-weight: 400;
  margin-top: 16px;
}

.news__block {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.news__block__btn {
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

.news__block__btn span {
  margin-right: 8px;
}

.news__cards {
  display: flex;
  justify-content: space-between;
  margin-top: 40px;
}

.news__card {
  display: flex;
  flex-direction: column;
  width: 48%;
  background-color: #393953;
  border-radius: 8px;
}

.news__card__content {
  padding: 24px;
}

.news__card__name {
  font-size: 16px;
  font-weight: 400;
  color: #C8C7D8;
  font-family: "Work Sans", serif;
}

.news__card__title {
  font-size: 24px;
  font-weight: 700;
  font-family: "CircularStd", cursive;
  color: #FFFFFF;
  margin-bottom: 80px;
  margin-top: 8px;
}

.news__card__date {
  padding: 8px 24px;
  color: #C8C7D8;
  font-size: 16px;
  font-weight: 400;
  font-family: "Work Sans", serif;
}

@media (max-width: 900px) {
  .news__cards {
    flex-direction: column;
    align-items: center;
  }

  .news__card {
    width: 80%;
    margin-bottom: 20px;
  }

  .news__card__image {
    width: 100%;
    border-radius: 8px 8px 0 0;
  }

  .news__card__content {
    width: 100%;
    padding: 12px;
  }
}
</style>