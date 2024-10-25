<script setup>
import Header from './components/Header.vue'
import MailingCard from './components/MailingCard.vue'
</script>

<template>
  <Header />
  <main>
    <h1 class="md:text-6xl text-3xl font-medium pt-6 text-center">
      Подписки «Клерка»
    </h1>
    <nav>
      <ul class="flex gap-6 justify-center pt-6 pb-4 text-base text-gray-500">
        <li><a href="/" class="activeLink">Рассылки</a></li>
        <li><a href="">Соцсети</a></li>
        <li><a href="">Мессенджеры</a></li>
      </ul>
    </nav>
    <MailingCard />
  </main>
</template>
<style scoped>
a:hover {
  color: #5A8CF1;
  text-decoration-line: underline;
  text-decoration-color: #5A8CF1;
  text-decoration-thickness: 2px;
  text-underline-offset: 10px;
}

.activeLink {
  color: #5A8CF1;
  text-decoration-line: underline;
  text-decoration-color: #5A8CF1;
  text-decoration-thickness: 2px;
  text-underline-offset: 20px;
}
</style>
