<script setup>
import { ref } from 'vue';

const isMenuOpen = ref(false);
const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};
</script>

<template>
  <header class="header">
    <img src="@/assets/logo/logo.svg" alt="Logo" class="header__logo" />
    <div class="burger__mob">
      <button class="header__nav__btn__mob">
        <span>Apply</span>
      </button>
      <button class="header__burger" @click="toggleMenu">
        <template v-if="isMenuOpen">
          <span>
            <img src="@/assets/icons/close.svg" alt="">
          </span>
        </template>
        <template v-else>
          <span class="burger-line"></span>
          <span class="burger-line"></span>
          <span class="burger-line"></span>
        </template>
      </button>
    </div>

    <ul class="header__nav" :class="{ 'is-open': isMenuOpen }">
      <li>Discover initiatives</li>
      <li>Funded grants</li>
      <li>Program expenses</li>
      <li>Blog</li>
      <li>FAQ</li>
      <li>
        <template v-if="isMenuOpen">
          <div class="header__icon">
            <img  src="@/assets/icons/twitter.svg" alt="Twitter">
            <img  src="@/assets/icons/discord.svg" alt="Twitter">
          </div>
        </template>
        <template v-else>
          <button class="header__nav__btn">
            <span>Apply for grant</span>
          </button>
        </template>
      </li>
    </ul>
  </header>
</template>

<style scoped>
.header {
  padding: 32px 24px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.header__nav {
  font-family: "Work Sans", serif;
  list-style: none;
  color: #FFFFFF;
  font-weight: 400;
  font-size: 16px;
  display: flex;
  gap: 16px;
  align-items: center;
}

.header__nav__btn {
  padding: 12px 16px;
  border-radius: 10px;
  background: #6966FF;
  border: none;
  color: #FFFFFF;
  font-weight: 500;
  font-size: 16px;
  font-family: CircularStd;
}

.header__nav__btn__mob {
  display: none;
}

.header__burger {
  display: none;
  flex-direction: column;
  gap: 4px;
  background: none;
  border: none;
  cursor: pointer;
}

.burger-line, .cross-line {
  width: 20px;
  height: 2px;
  background-color: #FFFFFF;
  border-radius: 10px;
}

.header__icon {
  display: flex;
  gap: 32px;
  margin-top: 88px;
}

@media (max-width: 900px) {
  .header__nav {
    display: none;
    position: absolute;
    top: 70px;
    right: 0;
    background: #393953;
    flex-direction: column;
    padding-bottom: 20px;
    padding-top: 20px;
    z-index: 1;
    width: 100%;
    gap: 32px;
  }
  .header__nav.is-open {
    display: flex;
  }
  .header {
    padding: 12px 24px;
  }

  .header__burger {
    display: flex;
  }

  .burger__mob {
    display: flex;
    align-items: center;
    gap: 16px;
  }
  .header__nav__btn__mob {
    display: flex;
    padding: 10px 14px;
    border-radius: 10px;
    background: #6966FF;
    border: none;
    color: #FFFFFF;
    font-weight: 500;
    font-size: 16px;
    font-family: CircularStd;
  }
}
</style>