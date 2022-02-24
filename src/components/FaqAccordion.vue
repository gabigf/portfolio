<template>
  <div class="faq-container">
    <div class="accordion" v-for="faq in faqData" :key="faq">
      <div
        class="accordion-item"
        @click="handleClick(faq)"
        :class="{ open: faq.isOpen }"
      >
        <button class="accordion-question">
          {{ faq.question }}
          <img
            class="arrow"
            src="../assets/images/arrow.svg"
            alt="+"
            :class="{ flip: faq.isOpen }"
          />
        </button>
        <div class="accordion-collapse" v-if="faq.isOpen">
          <div class="accordion-content">
            {{ faq.answer }}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  name: "Faq",
  setup() {
    const faqData = ref([
      {
        id: 1,
        question: "A digital agency is a business",
        answer:
          "Digital marketing efforts, instead of handling in-house. They can provide your business with a variety of digital solutions to promote your product or service online and help you hit your marketing goals and grow your business.",
        isOpen: true,
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

    const handleClick = (el) => {
      el.isOpen = !el.isOpen;
      for (const faq of faqData.value) {
        if (faq.id !== el.id) {
          faq.isOpen = false;
        }
      }
    };

    return { faqData, handleClick };
  },
};
</script>

<style>
.faq-container {
  width: 100%;
  padding-top: 3.5rem;
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
}

.accordion-question {
  display: flex;
  align-items: center;
  justify-content: space-between;
  text-align: initial;
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
  display: flex;
  justify-content: center;
  height: fit-content;
  padding-bottom: 1rem;
}

.accordion-content {
  width: 87%;
  color: var(--primary-light);
  line-height: 2rem;
}

.open {
  background: white;
}

.flip {
  animation: spin1 10ms ease;
  animation-fill-mode: forwards;
}

@keyframes spin1 {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(180deg);
  }
}

@media only screen and (min-width: 768px) {
  .faq-container {
    width: 55%;
  }

  .accordion-collapse {
    height: 8.5rem;
    padding-bottom: 0;
  }
}
</style>
