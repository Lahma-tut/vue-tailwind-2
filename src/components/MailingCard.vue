<script setup>
import MailingCardItem from './MailingCardItem.vue'
import SubscribeInput from './SubscribeInput.vue';
</script>

<template>
  <div class="rounded-2xl bg-gray-100">
    <div class="md:px-12 md:pt-10 md:pb-2 px-6 pt-8">
      <h2 class="text-2xl md:text-center pb-6 font-medium">
        Выберите рассылки, которые подходят именно вам
      </h2>
      <SubscribeInput />
    </div>
    <article class="grid sm:grid-cols-1 md:grid-cols-2 gap-6 px-6 pb-12 pt-2 ">
      <MailingCardItem
        title="Утренний бухгалтер"
        subtitle="Перед рассветом" 
        desc="Самые важные новости и события за день. Кратко, по делу, структурировано."
        human="Уже получает 59 342 человек"
        image="/frame-3505.png"
        :list="['Новости для бухгалтеров, ИП и директора', 'Подборка статей за день']"
        />

      <MailingCardItem
        title="Ночной бухгалтер"
        subtitle="Перед закатом" 
        desc="Самая краткая газета о налогах и бухучете в мире — современная рассылка для чтения."
        human="Уже получает 37 480 человек"
        image="/frame-3507.png"
        :list="['Анализ, оценка и только самое главное', 'Лучшие комменты юзеров в обзоре']"
        />

      <MailingCardItem
        title="Ножницы скидок"
        subtitle="Раз в две недели" 
        desc="Подборка самых выгодных и полезных спецпредложений от надежных компаний."
        human="Уже получает 92 118 человек"
        image="/frame-3509.png"
        :list="['Акции и скидки от лидеров рынка', 'Те, кто подписался – экономят много денег' ]"
        />

        <MailingCardItem
          title="Чемодан вебинаров"
          subtitle="По мере появления анонсов" 
          desc="Подборка с анонсами бесплатных вебинаров на самые топовые темы при участии экспертов."
          human="Уже получает 92 082 человек"
          image="/frame-3511.png"
          :list="['Никогда не пришлем платные вебинары', 'Подборка топовых тем для вебинаров']"
          />
    </article>
  </div>
</template>