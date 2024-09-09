<script setup></script>
<template>
  <div class="container">
    <div>
      <h2>Purchase your awesome lessons and find your tutors</h2>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Lorem habitant
        a tincidunt cras accumsan integer suscipit. Libero accumsan eget
        aliquet.
      </p>
      <div class="buttons">
        <button class="bg-button">Book Your Lessons</button>

        <button class="stork-button">Find Your Tutors</button>
      </div>
    </div>
    <img src="/icons/image-purchase.svg" alt="" />
  </div>
</template>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-top: 70px;
}
h2 {
  color: #000;
  font-size: 30px;
  font-weight: 600;
  line-height: 160%;
  letter-spacing: 1.05px;
}
p {
  color: #90a3b4;
  margin: 23px 0;
  font-size: 12px;
  font-weight: 400;
  line-height: 25px;
}

.buttons {
  display: flex;
  align-items: center;
  gap: 20px;
}
.bg-button {
  font-size: 12px;
  font-weight: 600;
  padding: 14.5px 20.5px;
  border-radius: 16px;
  color: #ffffff;
  background-color: #fb9c46;
  box-shadow: 0px 4px 357px 0px rgba(255, 146, 47, 0.15),
    0px 0.501px 44.702px 0px rgba(255, 146, 47, 0.08);
  cursor: pointer;
}
.stork-button {
  font-size: 12px;
  color: #fb9c46;
  padding: 14.5px 26px;
  font-weight: 600;
  border-radius: 16px;
  border: 3px solid #fb9c46;
  box-shadow: 0px 85px 80px 0px rgba(64, 127, 85, 0.08),
    0px 25.625px 24.118px 0px rgba(64, 127, 85, 0.05),
    0px 10.643px 10.017px 0px rgba(64, 127, 85, 0.04),
    0px 3.849px 3.623px 0px rgba(64, 127, 85, 0.03);
  cursor: pointer;
}
img {
  width: 100%;
  max-width: 540px;
}
@media (width>768px) {
  .container {
    flex-direction: row;
  }
  .buttons {
    justify-content: start;
    gap: 20px;
  }
  @media (width> 1000px) {
    h2 {
      color: #000;
      font-size: 36px;
      font-weight: 600;
      line-height: 160%;
      letter-spacing: 1.26px;
      max-width: 600px;
    }
    p {
      color: #6c6c6c;
      font-size: 18px;
      font-weight: 400;
      line-height: 160%;
      margin: 23px 0 33px 0;
      max-width: 610px;
    }
    img {
      max-width: 530px;
    }
    .buttons button {
      font-size: 16px;
      font-style: normal;
      font-weight: 600;
      line-height: normal;
      padding: 18.5px 24px;
    }
    .stork-button{
      padding: 18.5px 34px;
    }
  }
}
</style>
