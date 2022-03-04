
<template v-on:scroll="scroll">
  <div class="slack">
    <img src="./assets/2560px-Slack_Technologies_Logo.svg.png" alt="" />
    <div class="animate-to">
      <p>1.Gmail, Outlook, Zoho mail</p>
      <p>2. Hubspot, Pipedrive, SugarCRM</p>
      <p>3. Xero, Monday.com, Shopify</p>
      <p>4. Stripe</p>
    </div>
  </div>
  <div class="createScroll">

  </div>
</template>
<script>
  export default {
    created() {
      document.addEventListener('scroll',() => {
          document.querySelector('.animate-to').classList.add('animation')
          document.querySelector('.slack').classList.add('addHeight')
      })
    },
  };
</script>
<style>
@import "./assets/base.css";
.slack {
  border: 1px solid black;
  box-shadow: 2px 2px 10px #ddd;
  width: 500px;
  padding: 20px;
  margin: auto;
  margin-top: 15%;
  height:150px;
}
.slack .animate-to {
  position: absolute;
  bottom: 120%;
}
.slack img {
  width: 100%;
  height: auto;
}
.createScroll{
  height:1000px
}
.animation{
  animation-name:animation;
  animation-duration:2s;
  animation-fill-mode: forwards;
}
@keyframes animation {
  0%{
    bottom: 120%;
  }
  100%{
    bottom:0%;
  }
}
.addHeight{
  animation-name:ani;
  animation-duration:2s;
  animation-fill-mode: forwards;
}
@keyframes ani {
  0%{
    padding:20px;
  }
  100%{
    padding-bottom:220px;
  }
}
</style>
