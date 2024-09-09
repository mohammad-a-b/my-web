<script setup></script>
<template>
  <div class="how-it-works">
    <div class="contents">
      <h2>Here’s how it <span class="highlight">works</span></h2>
      <p class="how-work-dec">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lorem habitant
        a tincidunt cras accumsan integer suscipit.eget aliquet.
      </p>
      <ul class="steps">
        <li class="step">
          <img class="step-icon" src="/icons/find-tutor.svg" alt="" />
          <div class="content">
            <h4>Find a tutor</h4>
            <p>
              Choose your ideal teacher from over 10,000 qualified language
              tutors.
            </p>
          </div>
        </li>
        <li class="step">
          <img class="step-icon" src="/icons/book-lesson.svg" alt="" />
          <div class="content">
            <h4>Book a lesson</h4>
            <p>Select a lesson time and add it to their calendar.</p>
          </div>
        </li>
        <li class="step">
          <img class="step-icon" src="/icons/start-learning.svg" alt="" />
          <div class="content">
            <h4>Start learning</h4>
            <p>Simple as that, you’re learning a language.</p>
          </div>
        </li>
      </ul>
    </div>
    <div class="video-content">
      <img class="video-img" src="/icons/image-video.png" alt="" />
      <img class="svg" src="/icons/howWork-svg.svg" alt="" />
      <div class="play-button">
        <img src="/icons/play-btn.svg" alt="" />
      </div>
    </div>
  </div>
</template>

<style scoped>
h2 {
  color: #393939;
  font-size: 32px;
  font-style: normal;
  font-weight: 600;
  letter-spacing: 1.05px;
}
h4 {
  color: #fb9c46;
  font-size: 14px;
  font-style: normal;
  font-weight: 400;
  line-height: 170%;
}
.content p {
  color: #393939;
  font-size: 12px;
  font-style: normal;
  font-weight: 300;
  line-height: 170%;
  margin: 0;
}
.how-work-dec {
  margin: 25px 0;
  max-width: 630px;
  color: #90a3b4;
  font-size: 15px;
  font-style: normal;
  font-weight: 400;
  line-height: 200%;
}
.how-it-works {
  gap: 0px 70px;
  margin-top: 60px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-radius: 15px;
}
.highlight {
  color: #fb9c46;
}
.step {
  display: flex;
  gap: 30px;
  align-items: center;
  padding: 15px;
  border-radius: 10px;
  margin-bottom: 20px;
  max-width: 600px;
  box-shadow: 0px -2px 128px 0px #fb9d4649;
}
.step-icon {
  border-radius: 50%;
  padding: 10px;
  background: #fb9c46;
}

.video-img {
  max-width: 600px;
  width: 100%;
  margin-top: 25px;
}

.video-content {
  position: relative;
}

.svg {
  position: absolute;
  bottom: -8%;
  right: -2%;
  width: 100%;
  max-width: 170px;
  z-index: 2;
}
.play-button {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  cursor: pointer;
}

.play-button img {
  width: 60px;
  height: 60px;
}

@media (width>768px) {
  .how-it-works {
    flex-direction: row;
  }
}
@media (width>1000px) {
  h2 {
    font-size: 36px;
    font-weight: 600;
    letter-spacing: 1.26px;
  }
  .how-work-dec {
    color: #6c6c6c;
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    max-width: 550px;
    line-height: 160%; /* 28.8px */
  }
  .video-img {
    margin: 0;
  }
  h4 {
    font-size: 18px;
  }
  .content p {
    font-size: 14px;
    font-weight: 300;
  }
}
</style>
<!-- 
<script setup>
import { ref } from "vue";

const menuVisible = ref(false);
const toggleMenu = () => {
  menuVisible.value = !menuVisible.value;
};

const props = defineProps({
  activeLink: String,
  links: Array,
});
const emit = defineEmits(["update:activeLink"]);

const selectLink = (linkName) => {
  emit("update:activeLink", linkName);
  toggleMenu();
};
</script>
<template>
  <header class="mobile-header">
    <a href="#" class="header-title">Tutorify</a>
    <button class="menu-btn" @click="toggleMenu">
      <img src="/icons/menu-berger.svg" alt="Menu" />
    </button>
    <transition name="slide-down">
      <div v-if="menuVisible" class="menu-overlay">
        <ul class="menu-list">
          <li
            v-for="link in links"
            :key="link.name"
            @click="selectLink(link.name)"
            >
            <a href="#" :class="{ active: activeLink === link.name }">{{
              link.label
            }}</a>
          </li>
          <img class="close-btn" @click="toggleMenu" src="/icons/close-btn.svg" alt="">
        </ul>
      </div>
    </transition>
  </header>
</template>

<style scoped>
.mobile-header {
  display: none;
  justify-content: space-between;
  align-items: center;
  padding: 10px 20px;
  background-color: white;
  border-bottom: 2px solid #f0f0f0;
}

.menu-btn {
  background: none;
  border: none;
  cursor: pointer;
}
.close-btn{
  width: 33px;
margin: 0 auto;
cursor: pointer;
}

.menu-overlay {
  position: fixed;
  top: 10px;
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

.menu-list li {
  margin: 0;
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
.mobile-header button {
  padding: 5px;
}

@media (width < 815px) {
  .mobile-header{
   display: flex;
  }}
</style>
 -->
