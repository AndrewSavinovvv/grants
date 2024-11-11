<script setup>

</script>

<template>
  <div class="question">
    <div class="question__block">
      <h1 class="question__block__title">Frequently asked questions</h1>
      <p class="question__block__text">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque nulla risus, <br>
        consectetur ut bibendum non, gravida non libero.
      </p>
    </div>
    <div class="question__nav">
      <ul class="question__nav__list">
        <li class="question__nav__list-item">
          <p>How do I apply?</p>
          <span>+</span>
        </li>
        <li class="question__nav__list-item">
          <p>Can I apply as a U.S. based person/company?</p>
          <span>+</span>
        </li>
        <li class="question__nav__list-item">
          <p>How will I be compensated?</p>
          <span>+</span>
        </li>
        <li class="question__nav__list-item">
          <p>What type of project will qualify for a Grant?</p>
          <span>+</span>
        </li>
        <li class="question__nav__list-item">
          <p>What is the application timeline? When can I expect to hear back?</p>
          <span>+</span>
        </li>
        <li class="question__nav__list-item">
          <p>How can I increase my chances of getting funded?</p>
          <span>+</span>
        </li>
        <li class="question__nav__list-item">
          <p>How often do you approve new Rounds of funding?</p>
          <span>+</span>
        </li>
      </ul>
    </div>
  </div>
</template>

<style scoped>
.question {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 20px;
  padding: 12px;
}

.question__block__title {
  color: #FFFFFF;
  font-family: "CircularStd", cursive;
  font-weight: 700;
  font-size: 40px;
  text-align: center;
}

.question__block__text {
  color: #C8C7D8;
  font-size: 18px;
  font-family: "CircularStd", cursive;
  text-align: center;
  font-weight: 400;
  margin-top: 16px;
}

.question__block {
  display: flex;
  flex-direction: column;
  align-items: center;
}


.question__block__btn span {
  margin-right: 8px;
}

.question__nav__list-item {
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: #FFFFFF;
  border-top: 1px solid #393953;
  padding-top: 24px;
  padding-bottom: 24px;
}
.question__nav__list-item:nth-child(7) {
  border-bottom: 1px solid #393953;
}
.question__nav__list-item span {
  font-size: 24px;
  font-weight: bold;
}
.question__nav {
  width: 100%;
}

@media (max-width: 900px) {
  .question__nav ul {
  padding: 0;
  }
}
</style>