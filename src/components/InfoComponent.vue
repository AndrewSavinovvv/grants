<script setup>

</script>

<template>
  <div class="info">
   <div class="info__block">
     <h1 class="info__block__title">Powering the future  of <br> dYdX through <br> community grants</h1>
     <div class="info__block__btns">
       <button class="info__block__discover">
         <span>Discover RFPs</span>
       </button>
       <button class="info__block__grant">
         <span>Apply for grant</span>
         <img src="@/assets/icons/arrow-right.svg" alt="">
       </button>
     </div>
   </div>
    <div class="info__metric">
      <ul class="info__metric__list">
        <li class="info__metric__list__item">
          <div>100+ </div>
          <p>projects funded</p>
        </li>
        <li class="info__metric__list__item">
          <div>$3+ milion</div>
          <p>awarded</p>
        </li>
        <li class="info__metric__list__item">
          <div>400+</div>
          <p>projects funded</p>
        </li>
      </ul>
    </div>
    <span>
      <img src="@/assets/icons/down%20arrow.svg" alt="">
    </span>
  </div>
</template>

<style scoped>
.info {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.info__block {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.info__block__title{
  font-family: CircularStd;
  font-size: 80px;
  font-weight: 700;
  color: #FFFFFF;
  text-align: center;
}
.info__block__btns {
  display: flex;
  gap: 32px;
  margin-top: 52px;
}
.info__block__discover {
  background: #393953;
  border: none;
  font-family: CircularStd;
  color: white;
  padding: 12px 39px;
  border-radius: 10px;

}
.info__block__grant{
  display: flex;
  justify-content: center;
  background:#6966FF;
  border: none;
  font-family: CircularStd;
  color: white;
  padding: 12px 21px;
  border-radius: 10px;

}
.info__metric {
  display: flex;
  justify-content: space-between;
  margin-top: 112px;
  margin-bottom: 78px;
}
.info__metric__list{
  display: flex;
  list-style: none;
  gap: 48px;
  padding: 0;
}
.info__metric__list__item p {
  font-size: 18px;
  color: #C8C7D8;
  font-family: "Work Sans", serif;
  font-weight: 400;
  text-align: center;
}
.info__metric__list__item div {
  font-family: "Work Sans", sans-serif;
  color: white;
  font-weight: 400;
  font-size: 20px;
  text-align: center;
}
@media (max-width: 900px) {
  .info {
    overflow: hidden;
    display: flex;
    align-items: center;
    flex-direction: column;
    padding: 24px;
  }

  .info__block,
  .info__metric {
    flex-direction: column;
    align-items: center;
    width: 100%;
  }

  .info__block__btns {
    flex-direction: column;
    gap: 16px;
    width: 100%;
  }

  .info__metric__list {
    flex-direction: column;
    gap: 24px;
    align-items: center;
    padding: 0;
  }

  .info__block__title {
    font-size: 40px;
    text-align: center;
  }

  .info__metric {
    margin-top: 32px;
    margin-bottom: 32px;
  }
}
</style>