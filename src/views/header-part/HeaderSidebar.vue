<template>
  <div class="sidebar-container">
    <ul class="sidebar-wrapper">
      <li><a href="#">Главная</a></li>
      <li><a href="#">Последние новости</a></li>
      <li><a href="#">Трансляции</a></li>
      <li><a href="#">Видео</a></li>
      <li><a href="#">Достижения</a></li>
      <li class="sidebar-dropdown">
        <div @click="dropdownActive" class="dropdown-visible">
            Виды
        <svg
          width="13"
          height="8"
          viewBox="0 0 13 8"
          fill="currentcolor"
          xmlns="http://www.w3.org/2000/svg"
          :class="isDropdown ? 'drop-svg-active' : 'drop-svg-deactive'"
        >
          <path
            d="M1.17737 1.42952L6.64797 6.63327L11.5849 1.42952"
            stroke="black"
            stroke-width="1.48678"
            stroke-linecap="round"
          />
        </svg>
        </div>
        <div
        class="dropdown-item" 
        :class="isDropdown ? 'dropdown-active' : 'dropdown-hidden'">
            <span>Футбол</span>
            <span>Теннис</span>
            <span>Баскетбол</span>
            <span>Хоккей</span>
            <span>Бокс</span>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: "header-sidebar",
  data(){
    return{
        isDropdown: false
    }
  },
  methods:{
    dropdownActive(){
        this.isDropdown = !this.isDropdown
    }
  }
};
</script>
