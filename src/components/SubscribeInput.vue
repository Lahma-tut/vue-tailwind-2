<template>
  <div class="subscribe">
    <div class="w-full relative">
      <div class="relative">
        <input type="email"
          class="w-full placeholder:text-gray-500
                text-gray-700 text-sm
                rounded-tl-lg rounded-tr-3xl
                rounded-bl-lg rounded-br-3xl
                pl-4 pr-20 py-4 
                transition duration-300 ease 
                focus:outline-none focus:border-slate-400 
                hover:border-gray-300 
                focus:shadow"
          placeholder="Электронная почта" />
        
          <button 
                class="max-sm:hidden absolute right-0 top-0
                rounded-full bg-[#316FEE] p-4
                border border-transparent 
                text-center text-sm text-white 
                transition-all shadow-sm hover:shadow 
                focus:bg-slate-700 focus:shadow-none 
                active:bg-slate-700 hover:bg-slate-700 
                active:shadow-none disabled:pointer-events-none 
                disabled:opacity-50 disabled:shadow-none"
                type="button">
          {{ 'Подписаться' }}
        </button>

        <button class="sm:hidden absolute right-0 top-0
                rounded-full bg-[#316FEE] px-5 py-4
                border border-transparent 
                text-center text-sm text-white 
                transition-all shadow-sm hover:shadow 
                focus:bg-slate-700 focus:shadow-none 
                active:bg-slate-700 hover:bg-slate-700 
                active:shadow-none disabled:pointer-events-none 
                disabled:opacity-50 disabled:shadow-none"
                type="button">
          {{ '>' }}
        </button>
      </div>
    </div>

    <div class="flex gap-2 items-center pt-4">
      <label class="switch">
        <input type="checkbox">
        <span class="slider round"></span>
      </label>
      <p class="text-sm font-normal text-gray-600 py-4">Подписаться на все рассылки</p>
    </div>
  </div>
</template>

<style scoped>

/*   switch - the box around the slider  */
.switch {
  position: relative;
  display: inline-block;
  width: 32px;
  height: 16px;
}

.switch input {
  display: none;
}

.slider {
  position: absolute;
  cursor: pointer;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: #ccc;
  -webkit-transition: .4s;
  transition: .4s;
}

.slider:before {
  position: absolute;
  content: "";
  height: 14px;
  width: 14px;
  left: 1px;
  bottom: 1px;
  background-color: white;
  -webkit-transition: .4s;
  transition: .4s;
}

input:checked+.slider {
  background-color: #2196F3;
}

input:focus+.slider {
  box-shadow: 0 0 1px #2196F3;
}

input:checked+.slider:before {
  -webkit-transform: translateX(16px);
  -ms-transform: translateX(16px);
  transform: translateX(16px);
}

.slider.round {
  border-radius: 34px;
}

.slider.round:before {
  border-radius: 50%;
}
</style>
