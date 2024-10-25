<script setup>
defineProps({
  title: String,
  subtitle: String,
  desc: String,
  human: String,
  image: String,
  list: Array,
})
</script>

<template>
  <div class="flex rounded-2xl bg-white p-6 cursor-pointer transition ease hover:shadow-lg ">
    <div>
      <span class="text-sm font-normal text-gray-400">
        {{ subtitle }}
      </span>
      <h3>{{ title }}</h3>
      <p class="text-sm font-normal text-gray-600 py-4">{{ desc }}</p>
      <ul class="ml-7 text-sm">
        <li v-for="(item, index) in list" :key="index">
          {{ item }}
        </li>
      </ul>
      
      <div class="subscribe-switch">
        <label class="switch">
          <input type="checkbox">
          <span class="slider round"></span>
        </label>
        <p class="text-sm font-normal text-gray-600 py-4">
          {{ human }}
        </p>
      </div>
    </div>
    <div>
      <img 
        :src="image" 
        :alt="title" 
        width="80" 
        height="80"
        >
    </div>
  </div>
</template>

<style scoped>
li {
  position: relative;
}

li::before {
  content: " ";
  width: 16px;
  height: 16px;
  background: url("check.png") no-repeat center;
  position: absolute;
  left: -25px;
  top: 3px;
}

/*   switch - the box around the slider  */
.subscribe-switch {
  padding-top: 16px;
  display: flex;
  align-items: center;
  gap: 8px;
}

.subscribe-switch p {
  padding: 0;
}

.switch {
  position: relative;
  display: inline-block;
  width: 50px;
  height: 24px;
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
  height: 22px;
  width: 22px;
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
  -webkit-transform: translateX(26px);
  -ms-transform: translateX(26px);
  transform: translateX(26px);
}

.slider.round {
  border-radius: 34px;
}

.slider.round:before {
  border-radius: 50%;
}
</style>
