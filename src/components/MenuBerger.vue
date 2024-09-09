<script setup>
const props = defineProps({
  activeLink: String,
  links: Array,
});

const emit = defineEmits(["update:activeLink", "closeMenu"]);

const selectLink = (linkName) => {
  emit("update:activeLink", linkName);
  emit("closeMenu"); // اینجا وضعیت منو بسته می‌شود
};

</script>

<template>
  <transition name="slide-down">
    <div class="menu-overlay">
      <ul class="menu-list">
        <li v-for="link in links" :key="link.name" @click="selectLink(link.name)">
          <a href="#" :class="{ active: activeLink === link.name }">{{ link.label }}</a>
        </li>
        <img class="close-btn" @click="$emit('closeMenu')" src="/icons/close-btn.svg" alt="Close Menu" />
      </ul>
    </div>
  </transition>
</template>

<style scoped>
.menu-overlay {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  background-color: white;
  border-radius: 0 0 10px 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.menu-list {
  list-style: none;
  padding: 15px;
  margin: 0;
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.menu-list li a {
  display: block;
  padding: 10px 15px;
  border-radius: 5px;
  text-align: center;
  color: #333;
  text-decoration: none;
}

.menu-list li a.active {
  background-color: #fb9c46;
  color: white;
}

.close-btn {
  width: 33px;
  margin: 0 auto;
  cursor: pointer;
}

.slide-down-enter-active,
.slide-down-leave-active {
  transition: all 0.3s ease;
}

.slide-down-enter-from {
  transform: translateY(-100%);
  opacity: 0;
}

.slide-down-enter-to {
  transform: translateY(0);
  opacity: 1;
}

.slide-down-leave-from {
  transform: translateY(0);
  opacity: 1;
}

.slide-down-leave-to {
  transform: translateY(-100%);
  opacity: 0;
}
</style>
