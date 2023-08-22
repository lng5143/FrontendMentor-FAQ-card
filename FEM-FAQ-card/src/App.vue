<template>
  <div class="container">
    <div class="illu-mobile">
      <img src="./assets/images/illustration-woman-online-mobile.svg">
      <img src="./assets/images/bg-pattern-mobile.svg">
    </div>

    <div class="illu-desktop">
      <img src="./assets/images/illustration-box-desktop.svg">
      <img src="./assets/images/illustration-woman-online-desktop.svg">
      <img src="./assets/images/bg-pattern-desktop.svg">
    </div>
    <h1>FAQ</h1>
    <question v-for="faq in faqs"
    v-bind:question="faq.q"
    v-bind:answer="faq.a"
    />
  </div>
</template>

<script>
  export default {
    data() {
      return {
        faqs: [
          {
            q: 'How many team members can I invite?',
            a: 'You can invite up to 2 additional users on the Free plan. There is no limit on team members for the Premium plan.'
          },
          {
            q: 'What is the maximum file upload size?',
            a: 'No more than 2GB. All files in your account must fit your allotted storage space.'
          },
          {
            q: 'How do I reset my password?',
            a: 'Click “Forgot password” from the login page or “Change password” from your profile page. A reset link will be emailed to you.'
          },
          {
            q: 'Can I cancel my subscription?',
            a: 'Yes! Send us a message and we’ll process your request no questions asked.'
          },
          {
            q: 'Do you provide additional support?',
            a: 'Chat and email support is available 24/7. Phone lines are open during normal business hours.'
          }
        ]
      }
    },
    methods: {

    }
  }
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Kumbh+Sans:wght@400;700&display=swap');

  body {
    background-color: hsl(273, 75%, 66%);
  }

  .container {
    padding: 20px;
    background-color: white;
    border-radius: 10px;
    position: relative;
    box-shadow: 0px 30px 0px 20px rgba(0,0,0,0.3);
  }

  .illu-desktop {
    display: none;
  }
</style>