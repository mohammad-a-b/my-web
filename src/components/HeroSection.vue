<template>
  <div class="container">
    <div>
      <div class="we-are-the-best">
        <h4>We are The Best</h4>
        <div class="line"></div>
      </div>
      <h1 class="main-title">
        Learn From Home With
        <span class="highlight">The Best</span> Online Language Tutors
      </h1>
      <p class="main-description">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Id interdum dui
        mollis. Suspendisse nulla:
      </p>
      <button class="try-free-button">Try Free Lessons</button>
    </div>
    <div class="image-container">
      <img class="hero-image" src="/icons/hero-image.svg" alt="hero" />
      <img class="japan" src="/icons/japan-hero.svg" alt="" />
      <img class="china" src="/icons/china-hero.svg" alt="" />
      <img class="italy" src="/icons/italy-hero.svg" alt="" />
    </div>
  </div>
</template>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  margin-top: 50px;
}

.we-are-the-best {
  display: flex;
  align-items: center;

  gap: 10px;
}

.we-are-the-best h4 {
  color: #fb9c46;
  font-size: 16px;
  font-weight: 600;
}

.main-title {
  text-align: left;
  font-weight: 800;
  margin: 20px 0;
  max-width: 650px;
  color: #000;
  font-size: 32px;
  letter-spacing: 1.12px;
  line-height: 51.2px;
}

.highlight {
  color: #fb9c46;
}

.main-description {
  text-align: left;
  color: #90a3b4;
  margin-bottom: 15px;
  font-family: Poppins;
  font-size: 14px;
  font-style: normal;
  font-weight: 400;
  line-height: 28px;
}

.try-free-button {
  cursor: pointer;
  background-color: #058e6e;
  font-size: 18px;
  font-weight: 600;
  line-height: normal;
  color: #ffffff;
  padding: 22px 45px;
  border-radius: 15px;
  transition: background-color 0.3s, box-shadow 0.3s;
  display: flex;
  justify-content: start;
}

.try-free-button:hover {
  background-color: #058e6e;
  box-shadow: 0px 5px 15px rgba(0, 0, 0, 0.2);
}

.hero-image {
  max-width: 270px;
  width: 100%;
  margin-top: 40px;
}
@media (width< 280px) {
  .try-free-button {
    padding: 10px 16px;
  }
}
@media (width> 768px) {
  .container {
    flex-direction: row;
    justify-content: center;
    gap: 30px;
    text-align: left;
  }

  .hero-image {
    min-width: 350px;
  }
  @media (width> 1000px) {
    .main-title {
      line-height: 57px;
      max-width: 500px;
    }
    .try-free-button {
      padding: 19px 79px;
      font-size: 16px;
    }
    .main-title {
      margin: 37px 0 44px 0;
      font-size: 48px;
      font-weight: 700;
      line-height: 160%;
      letter-spacing: 1.68px;
      max-width: 700px;
    }
    .main-description {
      margin-bottom: 27px;
      color: #6c6c6c;
      font-size: 18px;
      font-weight: 400;
      line-height: 28.8px;
      max-width: 650px;
    }
  }

  .hero-image {
    min-width: 400px;
  }
  .image-container {
    position: relative;
  }
  .japan {
    position: absolute;
    left: -40px;
    top: 100px;
  }
  .china {
    position: absolute;
    top: 40px;
    right: 0;
  }
  .italy {
    position: absolute;
    top: 340px;
    right: -20px;
    border-radius: 50%;
    border: 6px solid #f9f9f9;
  }
  @keyframes upDown {
    0% {
      transform: translateY(0);
    }
    50% {
      transform: translateY(-20px);
    }
    100% {
      transform: translateY(0);
    }
  }

  .japan,
  .china,
  .italy {
    animation: upDown 2s infinite;
  }
}
</style>
