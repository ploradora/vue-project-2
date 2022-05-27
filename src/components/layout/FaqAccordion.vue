<template>
  <div class="question-cell question-cell-1" :class="{open: isSelected === 'question1'}" @click="setSelectedTab('question1')">
    <div class="question question-1">
      <p>How many team members can I invite?</p>
      <img
        class="arrow arrow-1"
        src="../../assets/images/icon-arrow-down.svg"
        alt="icon arrow"
      />
    </div>
    <p class="answer">
      You can invite up to 2 additional users on the Free plan. There is no
      limit on team members for the Premium plan.
    </p>
  </div>
  <div class="question-cell question-cell-2" :class="{open: isSelected === 'question2'}" @click="setSelectedTab('question2')">
    <div class="question question-2">
      <p>What is the maximum file upload size?</p>
      <img
        class="arrow arrow-2"
        src="../../assets/images/icon-arrow-down.svg"
        alt="icon arrow"
      />
    </div>
    <p class="answer">
      No more than 2GB. All files in your account must fit your allotted storage
      space.
    </p>
  </div>
  <div class="question-cell question-cell-3" :class="{open: isSelected === 'question3'}" @click="setSelectedTab('question3')">
    <div class="question question-3">
      <p>How do I reset my password?</p>
      <img
        class="arrow arrow-3"
        src="../../assets/images/icon-arrow-down.svg"
        alt="icon arrow"
      />
    </div>
    <p class="answer">
      Click “Forgot password” from the login page or “Change password” from your
      profile page. A reset link will be emailed to you.
    </p>
  </div>
  <div class="question-cell question-cell-4" :class="{open: isSelected === 'question4'}" @click="setSelectedTab('question4')">
    <div class="question question-4">
      <p>Can I cancel my subscription?</p>
      <img
        class="arrow arrow-4"
        src="../../assets/images/icon-arrow-down.svg"
        alt="icon arrow"
      />
    </div>
    <p class="answer">
      Yes! Send us a message and we’ll process your request no questions asked.
    </p>
  </div>
  <div class="question-cell question-cell-5" :class="{open: isSelected === 'question5'}" @click="setSelectedTab('question5')">
    <div class="question question-5">
      <p>Do you provide additional support?</p>
      <img
        class="arrow arrow-5"
        src="../../assets/images/icon-arrow-down.svg"
        alt="icon arrow"
      />
    </div>
    <p class="answer">
      Chat and email support is available 24/7. Phone lines are open during
      normal business hours.
    </p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isSelected: 'question1',
    };
  },
  methods: {
    setSelectedTab(tab) {
      this.isSelected = tab;
    },
  },
};
</script>

<style lang="scss">
.question-cell {
  border-bottom: 1px solid hsl(240, 6%, 80%);
  .question {
    padding: 1.1rem 0;
    display: flex;
    align-items: center;
    justify-content: space-between;
    cursor: pointer;
    &:hover {
      > p {
        color: hsl(14, 88%, 65%);
      }
    }
    > p {
      margin-right: 1rem;
      color: hsl(237, 12%, 50%);
      font-weight: 700;
    }
  }
  .answer {
    width: 90%;
    // padding-bottom: 1.1rem;
    color: hsl(240, 6%, 50%);
    // display: none;
    height: 0px;
    opacity: 0;
    overflow: hidden;
  }
}
// .open {
  //   .question {
//     > p {
  //       color: #000;
//     }
//     .arrow {
  //       transform: rotate(180deg);
//     }
//   }
//   .answer {
//     display: block;
//   }
// }
.open {
  .question {
    > p {
      color: #000;
    }
    .arrow {
      transform: rotate(180deg);
    }
  }
  .answer {
    transition: all .2s linear;
    opacity: 1;
    height: 100%;
    padding-bottom: 1.1rem;
  }
}
</style>
