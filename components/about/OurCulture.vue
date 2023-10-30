<template>
  <section>
    <v-container>
      <app-section-descriptor
        title="Our mission"
        heading="Neatio Vision"
        style="max-width: 60rem"
      />
      <app-section-descriptor
            description="With Neatio, users can expect lightning-fast transaction speeds, eliminating the frustrating delays that have long been associated with traditional payment systems. 
            Our platform ensures that transactions are processed swiftly, enabling seamless and timely transfers of value."
style="text-align: left;" />
<div class="spc"></div>
      <app-section-descriptor
            description="       Our mission at Neatio is to revolutionize traditional payments. By leveraging cutting-edge blockchain technology, 
        we offer lightning-fast transactions, enhanced security, heightened privacy, and significant cost savings. Join us in reshaping the future of payments, making it accessible, secure, and efficient for everyone. 
        Together, let's unlock the transformative power of decentralization."
style="text-align: left;" />
      <v-stack justify="space-between" wrap>
        <div
          v-for="culturePoint in culturePoints"
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
      </v-stack>
    </v-container>
  </section>
</template>

<script>
export default {
  name: 'OurCulture',
  data() {
    return {
      culturePoints: [

      ],
    }
  },
}
</script>

<style >
@import url('../lib/media-query-helper.css');

.our-culture-points {
  width: 30%;
  justify-content: center;
  align-items: center;
  margin: 2rem 0;

  @media (--viewport-medium) {
    width: 50%;
  }
}
.description-text{
font-family: Play, Arial, Helvetica, sans-serif;
}
.our-culture-points > * {
  margin: 0 auto;
  max-width: 12rem;
}
.spc{
  padding: 1rem;
}
.spcs{
  padding: 2.4rem;
}
.our-culture-points > .blurb-description {
  font-size: 1.125rem !important;
  line-height: 1.375rem;

  @media (--viewport-medium) {
    font-size: 1rem;
    line-height: 1.125rem;
  }
}
</style>
