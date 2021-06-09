<template>
  <div>
    <h1>Solidan is an IT Consulting and Outsourcing Firm</h1>
    <p>
      Solidan specializes in the enterprise integration of financial, human
      resource, supply chain and customer relationship management (CRM)
      applications and systems. Our IT consultants leverage their business
      process knowledge and technical expertise to provide the&nbsp;integration,
      support and training necessary to result in improved operational
      efficiencies and increased profitability.&nbsp;
    </p>
  </div>
</template>

<script>
export default {}
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
@apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
