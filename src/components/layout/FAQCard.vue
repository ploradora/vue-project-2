<template>
  <base-card>
    <img
      class="cube-desktop"
      src="../../assets/images/illustration-box-desktop.svg"
      alt="red cube illustration"
    />
    <section>
      <div class="illustrations">
        <img
          class="shadow-illustration-mobile"
          src="../../assets/images/bg-pattern-mobile.svg"
          alt="shadow illustration"
        />
        <img
          class="illustration-mobile"
          src="../../assets/images/illustration-woman-online-mobile.svg"
          alt="illustration woman online mobile"
        />
        <img
          class="background-lines-desktop"
          src="../../assets/images/bg-pattern-desktop.svg"
          alt="background pattern line desktop"
        />
        <img
          class="illustration-desktop"
          src="../../assets/images/illustration-woman-online-desktop.svg"
          alt=""
        />
      </div>
      <div class="content">
        <h1>FAQ</h1>
        <div class="questions">
          <faq-accordion></faq-accordion>
        </div>
      </div>
    </section>
  </base-card>
</template>

<script>
import FaqAccordion from "./FaqAccordion.vue";
import BaseCard from "../UI/BaseCard.vue";

export default {
  components: {
    BaseCard,
    FaqAccordion,
  },
  methods: {
  }
};
</script>

<style lang="scss">
.cube-desktop {
  display: none;
  @media only screen and(min-width: 830px) {
    position: absolute;
    left: -6.2rem;
    top: 41%;
    display: block;
    width: 9rem;
    z-index: 1;
  }
}

section {
  position: relative;
  .illustrations {
    .background-lines-desktop,
    .illustration-desktop {
      display: none;
    }
    .illustration-mobile {
      position: absolute;
      width: min(80%, 220px);
      top: 0;
      left: 50%;
      transform: translate(-50%, -60%);
    }
    .shadow-illustration-mobile {
      display: block;
      margin: auto;
      width: min(80%, 220px);
    }
  }
  .content {
    padding: 1.5rem;
    h1 {
      text-align: center;
      margin-bottom: 1rem;
      font-size: 2rem;
    }
    .questions {
      margin-bottom: 1.7rem;
      min-height: 319px;
    }
  }

  @media only screen and (min-width: 830px) {
    display: flex;
    align-items: center;
    width: 100%;
    overflow: hidden;
    .illustrations {
      flex-basis: 50%;
      .shadow-illustration-mobile,
      .illustration-mobile {
        display: none;
      }
      .illustration-desktop {
        position: absolute;
        width: 47%;
        bottom: 51%;
        left: -7%;
        transform: translateY(49%);
        display: block;
      }
      .background-lines-desktop {
        position: absolute;
        width: 100%;
        bottom: 55%;
        left: -60%;
        transform: translateY(45%);
        display: block;
      }
    }
    .content {
      flex-basis: 50%;
      padding: 3.5rem 5rem 3.5rem 0;
      h1 {
        text-align: unset;
        font-size: 1.5rem;
      }
      .questions {
        margin-bottom: unset;
      }
    }
  }
}
</style>
