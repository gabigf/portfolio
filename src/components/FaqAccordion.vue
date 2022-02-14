<template>
  <div class="faq-container">
    <div class="accordion">
      <div class="accordion-item">
        <button class="accordion-question">
          A digital agency is a business
          <img class="arrow" src="../assets/images/arrow.png" alt="expand" />
        </button>
        <div class="accordion-collapse">
          <div class="accordion-content">
            Digital marketing efforts, instead of handling in-house. They can
            provide your business with a variety of digital solutions to promote
            your product or service online and help you hit your marketing goals
            and grow your business.
          </div>
        </div>
      </div>

      <div class="accordion-item">
        <button class="accordion-question">
          Hire to outsource your digital
          <img class="arrow" src="../assets/images/arrow.png" alt="expand" />
        </button>
        <div class="accordion-collapse collapse">
          <div class="accordion-content">
            No more than 2GB. All files in your account must fit your allotted
            storage space.
          </div>
        </div>
      </div>

      <div class="accordion-item">
        <button class="accordion-question">
          Marketing efforts
          <img class="arrow" src="../assets/images/arrow.png" alt="expand" />
        </button>
        <div class="accordion-collapse collapse">
          <div class="accordion-content">
            Click “Forgot password” from the login page or “Change password”
            from your profile page. A reset link will be emailed to you.
          </div>
        </div>
      </div>
      <!-- 
					<div class="accordion-item">
						<button class="accordion-question">
							Can I cancel my subscription?
						</button>
						<div class="accordion-collapse collapse">
							<div class="accordion-content">
								Yes! Send us a message and we'll process your request no
								questions asked.
							</div>
						</div>
					</div>

					<div class="accordion-item">
						<button class="accordion-question">
							Do you provide additional support?
						</button>
						<div class="accordion-collapse collapse">
							<div class="accordion-content">
								Chat and email support is available 24/7. Phone lines are open
								during normal business hours.
							</div>
						</div>
					</div> -->
    </div>
  </div>
</template>

<script>
export default {};
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
}

.arrow {
  width: 2rem;
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
</style>
