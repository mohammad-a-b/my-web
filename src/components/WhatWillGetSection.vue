<script setup>
import { ref } from "vue";

const items = ref([
  {
    id: 1,
    title: "1-on-1 lessons in more than 150 languages",
    description: "certified teachers with proven experience",
    moreText:
      "Lorem ipsulibero ipsam ducimus porro architecto harum odio eveniet obcaecati necessitatibus numquam.",
    showMore: false,
  },
  {
    id: 2,
    title: "Practice for free with the italki community",
    description:
      "Develop skills by from certified building connections with others",
    moreText:
      "Lorem ipsulibero ipsam ducimus porro architecto harum ryuf,fy.,fui.o/iyo/tgu.ecusandae odio eveniet obcaecati necessitatibus numquam.",
    showMore: false,
  },
  {
    id: 3,
    title: "Take learning beyond the classroom",
    description: "Learn from certified teachers with proven experience",
    moreText:
      "Lorem ipsulibero ipsam ducicusandae odio eveniet obcaecati necessitatibus numquam.",
    showMore: false,
  },
]);
</script>

<template>
  <div class="container">
    <div class="image-container">
      <img class="image" src="/icons/what-image.svg" alt="" />
    </div>
    <div>
      <h2>What Will You <span class="highlight-green">Get</span> ?</h2>
      <p class="highlight">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Id interdum dui
        mollis . Suspendisse nulla :
      </p>

      <ul>
        <li v-for="item in items" :key="item.id">
          <div class="flex-li">
            <img src="/icons/tick.svg" alt="" />
            <h4>{{ item.title }}</h4>
          </div>
          <div class="card-dec">
            <p>
              <span class="item-description">{{ item.description }}</span>
              <span v-show="item.showMore">{{ item.moreText }}</span>
              <button
                @click="item.showMore = !item.showMore"
                class="highlight-green read-more"
              >
                {{ item.showMore ? "Read less" : "Read more" }}
              </button>
            </p>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<style scoped>
.container {
  margin-top: 80px;
  display: flex;
  flex-direction: column-reverse;
  align-items: center;
  gap: 70px;
}

.highlight {
  color: #90a3b4;
  margin: 30px 0;
  font-size: 12px;
  font-style: normal;
  font-weight: 400;
  line-height: 200%;
  max-width: 400px;
}
button {
  cursor: pointer;
  padding: 5px;
  font-size: 10px;
}
.item-description::before {
  content: "•";
  font-size: 15px;
  margin-right: 6px;
}
.item-description{
  font-size: 12px;
}
h2 {
  font-size: 35px;
  color: #393939;
  font-size: 30px;
  font-style: normal;
  font-weight: 600;
  letter-spacing: 1.05px;
}
.highlight-green {
  color: #058e6e;
}

h4 {
  color: #393939;
  font-size: 12px;
  font-style: normal;
  font-weight: 700;
  line-height: 20.4px;
}
p {
  line-height: 24px;
}
.center-li {
  margin: 20px 0;
}
li {
  margin-top: 20px;
  padding: 15px 23px 3px 23px;
  max-width: 500px;
  border-radius: 17px;
  background: #fff;
  box-shadow: 0px -2px 128px 0px rgba(5, 142, 110, 0.14);
}
.image {
  max-width: 350px;
  width: 100%;
  border-radius: 50px;
  position: relative;
  top: -60px;
}
.image-container {
  height: 310px;
  margin: 20px;
  background-color: #efd8c9;
  border-radius: 50px;
}
.flex-li {
  display: flex;
  align-items: center;
  gap: 10px;
}
.card-dec {
  margin: 10px 43px 20px 40px;
  color: #8d8d8d;
  font-size: 10px;
  font-style: normal;
  font-weight: 400;
  line-height: 200%;
}
@media (width<460px) {
  .image-container {
    background: transparent;
    margin: 0 auto;
  }
  .image {
    background-color: #efd8c9;
    border-radius: 50px;
  }
}
@media (width>768px) {
  .container {
    align-items: center;
    display: flex;
    flex-direction: row;
    justify-content: center;
    gap: 60px;
  }
  .image-container{
  display: none;
  }
  .highlight {
    font-size: 15px;
    max-width: 470px;
  }
  h2 {
    font-size: 33px;
    letter-spacing: 1.26px;
  }
  h4 {
    font-size: 15px;
  }
  button {
    font-size: 15px;
    font-weight: 400;
  }
  .card-dec {
    font-size: 13px;

  }
}
@media (width>1000px) {
  .highlight {
    color: #6c6c6c;
    font-size: 16.5px;
    font-weight: 400;
    line-height: 160%;
    margin: 5px 0;
    max-width: 470px;
  }
  h2 {
    color: #393939;
    font-size: 36px;
    font-weight: 600;
    letter-spacing: 1.26px;
  }
  h4 {
    color: #393939;
    font-family: Poppins;
    font-size: 16px;
    font-style: normal;
    font-weight: 600;
  }
  .card-dec {
    color: #8d8d8d;
    font-family: Poppins;
    font-size: 14px;
    font-style: normal;
    font-weight: 400;
    line-height: 160%;
    margin: 2px 30px 18px 45px;
  }
  button {
    font-size: 14px;
    font-weight: 400;
  }
  li img {
    width: 43.3px;
  }
  .image{
    max-width: 430px;
  }
  .image-container{
    display: block;
    height: 390px;
  }
}
</style>
