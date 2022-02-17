<template>
  <div class="faq-container">
    <div class="accordion" v-for="faq in faqData" :key="faq">
      
      <div class="accordion-item" @click="handleClick(faq)">
        <button class="accordion-question">
          {{ faq.question}}
          <img class="arrow" src="../assets/images/arrow.png" alt="expand" />
        </button>
        <div class="accordion-collapse collapse" :class="[faq.isOpen ? collapse : '']">
          <div class="accordion-content">
            {{ faq.answer }}
          </div>
        </div>
      </div>
      
    </div>
  </div>
</template>

<script>
import { watchEffect, ref } from 'vue'
export default {
  name: "Faq",
  setup() {

    const faqData = ref([
      {
        id: 1,
        question: "A digital agency is a business",
        answer:
          "Digital marketing efforts, instead of handling in-house. They can provide your business with a variety of digital solutions to promote your product or service online and help you hit your marketing goals and grow your business.",
        isOpen: false,
      },
      {
        id: 2,
        question: "Hire to outsource your digital",
        answer:
          "Digital marketing efforts, instead of handling in-house. They can provide your business with a variety of digital solutions to promote your product or service online and help you hit your marketing goals and grow your business.",
        isOpen: false,
      },
      {
        id: 3,
        question: "Marketing efforts",
        answer:
          "Digital marketing efforts, instead of handling in-house. They can provide your business with a variety of digital solutions to promote your product or service online and help you hit your marketing goals and grow your business.",
        isOpen: false,
      },
    ]);

    const handleClick = (data) => {
     data.isOpen = !data.isOpen;
      console.log(data);
    };

    return { handleClick, faqData };
  }
};
</script>

<style>
.faq-container {
  width: 55%;
  padding-top: 3.5rem;
}

.collapse {
  display: none;
}

.accordion {
  background: transparent;
}

.accordion-item {
  border: 1px solid #f3d1bf;
  cursor: pointer;
}

.arrow {
  width: 2rem;
  content: url("../assets/images/arrow.png");
}

.accordion-question {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
  height: 6.5rem;
  font-size: 24px;
  font-weight: 700;
  padding: 0 2rem 0 2rem;
}

.accordion-question,
.accordion-question:hover {
  border: none;
  background: transparent;
  color: var(--primary);
}

.accordion-collapse {
  transition: height 300ms ease;
  display: flex;
  align-items: center;
  line-height: 2rem;
  padding: 0 2rem 3rem 2rem;
  width: 83%;
  color: var(--primary-light);
}

.accordion-collapse.collapse {
  display: none;
}

.accordion__collapse.collapsing {
  height: 0;
  overflow: hidden;
}

.accordion__collapse.open {
  display: block;
}

.vcp__header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
  height: 6.5rem;
  font-size: 24px;
  font-weight: 700;
  padding: 0 2rem 0 2rem;
}
.vcp__header-icon[data-v-64321428] {
  display: flex;
  align-items: center;
  transition: transform 0.3s cubic-bezier(0.5, 0.25, 0, 1);
}
.vcp--expanded .vcp__header-icon[data-v-64321428] {
  transform-origin: center;
  transform: rotate(180deg);
}

.vcp__header-icon > span[data-v-64321428] {
  display: flex;
  height: 24px;
  width: 24px;
}
.vcp__header-icon[data-v-64321428] svg {
  height: 100%;
  width: 100%;
}
</style>
