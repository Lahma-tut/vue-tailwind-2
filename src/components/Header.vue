<template>
  <header class="flex flex-col items-center">
    <div>
      <a href="/"><img src="/klerk.png"alt="logo-klerk"></a>
    </div>
    <ul class="flex pt-6 text-gray-400 text-sm font-medium">
      <li><a href="/">Главная</a></li>
      <li><a href="/">Категория</a></li>
      <li><a href="/">Подписка</a></li>
    </ul>
  </header>
</template>

<style scoped>
li::after {
  content: "→";
  padding: 10px;
}

li:last-child:after {
  content: "";
}

a {
  cursor: pointer;
  text-decoration-line: underline;
  text-decoration-color: #E6EDFF;
  text-decoration-thickness: 1px;
  text-underline-offset: 3px;
  transition: all 0.2s ease-in;
}

a:hover {
  text-decoration-color: #999999;
}

</style>
