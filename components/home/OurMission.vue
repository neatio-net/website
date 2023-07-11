<template>
  <section>
    <v-container>
      <app-section-descriptor
        title="Our mission"
        heading="Neatio Vision"
        style="max-width: 60rem"
      />

      <app-section-descriptor
            description="With Neatio, users can expect lightning-fast transaction speeds, eliminating the frustrating delays that have long been associated with traditional payment systems. Our platform ensures that transactions are processed swiftly, enabling seamless and timely transfers of value."
style="text-align: left;" />
<div class="spc"></div>

      <app-section-descriptor
            description="Our mission at Neatio is to revolutionize the traditional payment system with our groundbreaking platform. For far too long, inefficiency, insecurity, and exorbitant costs have plagued conventional payment methods, limiting access and hindering financial progress. We are determined to disrupt this status quo by harnessing cutting-edge blockchain technologies and democratizing their benefits for all. By leveraging the power of decentralization, we empower users to unlock a transformative payment experience that surpasses the limitations of the past."
style="text-align: left;" />
<div class="spc"></div>



<app-section-descriptor
            description="Security is also at the core of our mission. Traditional payment methods have often fallen victim to security breaches and data theft, exposing individuals and businesses to significant risks. Neatio tackles this challenge head-on by implementing robust security measures, leveraging the immutability and transparency of blockchain technology. Our users can have peace of mind, knowing that their transactions are protected by state-of-the-art cryptographic protocols and secure decentralized networks."
style="text-align: left;" />
<div class="spc"></div>

<app-section-descriptor
            description="Privacy is another aspect we prioritize. We understand the importance of personal and financial privacy in an increasingly interconnected world. Neatio empowers individuals and businesses to maintain their privacy by minimizing the collection and exposure of sensitive data. Through our platform, users can conduct transactions with confidence, knowing that their personal information is safeguarded."
style="text-align: left;" />
<div class="spc"></div>

<app-section-descriptor
            description="Cost savings are a significant advantage of the Neatio platform. Conventional payment systems often come with exorbitant fees and complex intermediaries, adding unnecessary financial burdens for users. We believe in making payments accessible and affordable for everyone. Neatio significantly reduces transaction costs, allowing users to retain more of their hard-earned money and stimulating economic growth."
style="text-align: left;" />
<div class="spc"></div>

      <!-- <v-stack justify="space-between" wrap>
        <div
          
          :key="culturePoint.title"
          class="our-culture-points"
        >
        
          <v-blurb
            :image="culturePoint.icon"
            :alt="culturePoint.title"
            :title="culturePoint.title"
            :description="culturePoint.description"
          />
        </div>
      </v-stack> -->
    </v-container>
  </section>
</template>

<script>
export default {
  name: 'OurMission',
}
</script>

<style lang="css" scoped>
@import url('../lib/media-query-helper.css');

section {
  @media (--viewport-small) {
    margin-top: 0 !important;
  }
}

.illustration-container {
  position: relative;
}

.illustration-container::before {
  content: '';
  position: absolute;
  inset: -20%;
  z-index: -1;
  background: radial-gradient(
    50% 40% at 50% 40%,
    rgba(248, 81, 142, 0.2) 0%,
    rgba(0, 0, 0, 0) 100%
  );
}

.principles-illustration {
  width: 100%;
  max-width: 28rem;
  align-self: center;

  @media (--viewport-medium) {
    max-width: 20rem;
    margin: 2rem auto;
  }
}
</style>
