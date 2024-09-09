<script setup>
import { ref } from "vue";
import MobileMenu from "./MenuBerger.vue";

const props = defineProps({
  activeLink: String,
  links: Array,
});

const menuVisible = ref(false);

const toggleMenu = () => {
  menuVisible.value = !menuVisible.value;
};

const emit = defineEmits(["update:activeLink"]);

const selectLink = (linkName) => {
  emit("update:activeLink", linkName);
};
</script>

<template>
  <header class="desktop-header">
    <a href="#" class="header-title">Tutorify</a>
    <nav class="desktop-nav">
      <ul class="desktop-menu">
        <li
          v-for="link in links"
          :key="link.name"
          :class="{
            login: link.name === 'Login',
            signup: link.name === 'Signup',
          }"
        >
          <a
            href="#"
            :class="{ active: activeLink === link.name }"
            @click.stop="selectLink(link.name)"
          >
            {{ link.label }}
          </a>
        </li>
        <img src="/icons/menu-berger.svg" alt="Menu" @click="toggleMenu" />
      </ul>
    </nav>

    <MobileMenu
      v-show="menuVisible"
      :activeLink="activeLink"
      :links="links"
      @update:activeLink="selectLink"
      @closeMenu="toggleMenu"
    />
  </header>
</template>

<style scoped>
.desktop-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 30px 80px;
  background-color: white;
  border-bottom: 2px solid #f0f0f0;
}

.desktop-menu {
  display: flex;
  align-items: center;
  gap: 25px;
}

.desktop-menu li a {
  padding: 7px 0;
  font-size: 16px;
  font-weight: 600;
}

.login,
.signup {
  border-radius: 8px;
  padding: 10px 29px;
}

.login {
  background-color: #407f55;
  margin: 0 30px 0 20px;
}

.signup {
  background-color: #fb9c46;
}
.login a,
.signup a {
  color: #ffffff;
}
.desktop-menu a.active {
  color: #fb9c46;
  position: relative;
}
.login a.active,
.signup a.active {
  color: rgb(255, 255, 255);
}
.desktop-menu a.active::after {
  content: "";
  position: absolute;
  transform: translateX(-50%);
  left: 50%;
  bottom: 0;
  width: 55%;
  height: 3px;
  background-color: #fb9c46;
  border-radius: 30px;
}
.login a.active::after,
.signup a.active::after {
  width: 0;
}

.header-title {
  font-size: 18px;
  font-weight: 900;
}

img {
  display: none;
  cursor: pointer;
}
@media (width<987px) {
  .desktop-menu {
    gap: 16px;
  }
  .login,
  .signup {
    padding: 7px 10px;
  }
  .login {
    margin-left: 10px;
  }
  .desktop-header {
    padding: 15px 30px 20px 30px;
  }
}
@media (max-width: 815px) {
  img {
    display: flex;
  }

  li {
    display: none;
  }
  .desktop-header {
    padding: 10px 25px 15px 25px;
  }
}
@media (width> 1200px) {
  .desktop-header{

    justify-content:space-around;
  }

}
</style>

<!-- <script setup>

const props = defineProps({
  activeLink: String,
  links: Array,
});
const emit = defineEmits(["update:activeLink"]);

const selectLink = (linkName) => {
  emit("update:activeLink", linkName);
};
</script>
<template>
  <header class="desktop-header">
    <a href="#" class="header-title">Tutorify</a>
    <nav class="desktop-nav">
      <ul class="desktop-menu">
        <li
          v-for="link in links"
          :key="link.name"
          :class="{
            login: link.name === 'Login',
            signup: link.name === 'Signup',
          }"
        >
          <a
            href="#"
            :class="{ active: activeLink === link.name }"
            @click="selectLink(link.name)"
          >
            {{ link.label }}
          </a>
        </li>
        <img src="/icons/menu-berger.svg" alt="" />
      </ul>
    </nav>
  </header>
</template>

<style scoped>
.desktop-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 50px;
  background-color: white;
  border-bottom: 2px solid #f0f0f0;
}
li a {
  color: #393939;
  font-size: 16px;
  font-style: normal;
  font-weight: 600;
  line-height: normal;
}

.desktop-menu {
  display: flex;
  align-items: center;
  gap: 25px;
}

.desktop-menu a {
  padding: 10px 5px;

}
.login,
.signup {
  border-radius: 8px;
  color: #fff;
  font-size: 16px;
  font-weight: 600;
  line-height: normal;
  padding: 10px 11px;
}
 .login a,
.signup a {
  color: #ffffff;
} 
.login {
  background-color: #407f55;
  margin: 0 30px 0 20px;
}
.desktop-menu .signup {
  color: #f0f0f0;
}
.signup {
  background-color: #fb9c46;
  padding: 10px 7px;
}

img {
  display: none;
  cursor: pointer;
}
.desktop-menu a.active {
  color: #fb9c46;
  position: relative;
}

.desktop-menu a.active::after {
  content: "";
  position: absolute;
  transform: translateX(-50%);
  left: 50%;
  bottom: 0;
  width: 30%;
  height: 2px;
  background-color: #fb9c46;
  border-radius: 4px;
}

.header-title {
  font-size: 18px;
  font-weight: 900;
}
@media (width<890px) {
  .desktop-menu a {
    padding: 5px 7px;
    font-size: 15px;
  }
  .desktop-menu{
    gap: 10px;
  }
}
@media (width < 815px) {
  li {
    display: none;
  }
  img {
    display: flex;
  }
  .desktop-header{
    padding: 0;
    padding-bottom: 10px;
  }
}

</style>
 -->
