<template>
  <div class="container">
    <div class="what-offer">
      <div class="what-offer-content">
        <div class="highlight">What do you want to learn?</div>
        <h2 class="what-we-offer-title">What We Offer</h2>
        <div class="center-line">
          <div class="highlight to-learn">I want to learn</div>
          <div class="line"></div>
        </div>
      </div>
      <div class="what-offer-dec">
        <p>
          Lorem ipsum dolor sit amet, consectetur advising edit. Donec urna nec
          faucibus ridiculus Volutpat eget ut vitae amet
          ullamcorper et, ante venenatis.
        </p>
        <ul class="countries">
          <li><img src="../assets//Countries/france.svg" alt="France" /></li>
          <li><img src="../assets//Countries/china.svg" alt="China" /></li>
          <li><img src="../assets//Countries/germany.svg" alt="Germany" /></li>
          <li><img src="../assets//Countries/japan.svg" alt="Japan" /></li>
          <li><img src="../assets//Countries/netherland.svg" alt="Netherlands" /></li>
          <li><img src="../assets//Countries/italy.svg" alt="Italy" /></li>
          <li><img src="../assets//Countries/spain.svg" alt="Spain" /></li>
          <div class="view-all-countries">
            <div class="highlight">View All</div>
            <img src="/icons/view-all.svg" alt="View All" />
          </div>
        </ul>
      </div>
    </div>
  </div>
</template>

<style scoped>
.what-offer {
  display: flex;
  flex-direction: column;
  gap: 25px;
  margin-top: 70px;
}
.what-offer p {
  margin-bottom: 30px;
  line-height: 24px;
  color: #90a3b4;
  font-family: Poppins;
  font-size: 13px;
  font-style: normal;
  font-weight: 400;
  line-height: 200%;
  max-width: 725px;
}
.what-offer-content h2 {
  margin: 10px 0;
}

.highlight {
  color: #fb9c46;
  font-weight: 600;
}
.center-line {
  display: flex;
  align-items: center;
  gap: 20px;
}
.countries {
  display: flex;
  flex-wrap: wrap;
  cursor: pointer;
  gap: 10px;
}

.countries img {
  width: 45px;
}

.view-all-countries {
  display: flex;
  align-items: center;
  gap: 5px;
}
.view-all-countries div {
  font-size: 18px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
}

.view-all-countries img {
  width: 14px;
}

@media (min-width: 768px) {
  .container {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 30px;
  }
  .what-offer-content {
    min-width: 280px;
  }
  .what-offer {
    display: flex;
    flex-direction: row;

    align-items: center;
  }
  .what-offer-dec p{
    color: #6c6c6c;
    font-size: 14px;
    font-weight: 400;
    line-height: 200%;
  }
  .what-offer-content {
    width: 50%;
  }

  .what-we-offer-title {
    font-size: 36px;
    margin-bottom: 20px;
  }

  .countries {
    justify-content: space-between;
  }
}
@media (width> 1000px) {
  .what-offer-content div {
    font-size: 18px;
  }
  .what-we-offer-title {
    color: #393939;
    font-size: 48px;
    font-weight: 600;
    letter-spacing: 1.68px;
  }
}
</style>
