<template>
  <div>
    <div :class="{ cardOffreRight: cardOffreRight, cardOffre: cardOffre }">
      <div class="col-md-4">
        <div class="round">
          <p class="number"><slot name="number"></slot></p>
        </div>
      </div>
      <div class="card-body col-md-6">
        <h5 class="card-title offre"><slot name="title"></slot></h5>
        <p class="card-text offre"><slot name="text"></slot></p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardOffre",
  props: {
    cardOffre: {
      type: Boolean,
      default: true,
    },
    cardOffreRight: {
      type: Boolean,
      default: false,
    },
  },
};
</script>

<style lang="css" scoped>
.cardOffre {
  padding: 2rem 1rem 2rem 1rem;
  background-color: #e2e2e2;
  display: flex;
  flex-wrap: wrap;
  flex-direction: row !important;
  margin: 0 !important;
}

.offre {
  padding: 2rem 2rem 1.3rem 4rem;
}

.cardOffreRight {
  display: flex;
  flex-direction: row-reverse !important;
  justify-content: space-between;
  background-color: #7798ab;
}

.number {
  font-family: "Alata";
  font-size: 3rem;
}

.round {
  border: 0.3rem solid grey;
  border-radius: 75px;
  padding: 1.2rem;
  width: 8rem;
  height: 8rem;
  margin: 1rem !important;
}

.col-md-4 {
  padding: 75px 125px 0px 125px;
}
</style>
