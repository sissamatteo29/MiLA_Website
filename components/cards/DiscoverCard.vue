<script lang="ts">
// Import necessary functions from Vue
import { defineComponent, ref } from 'vue';

// Define the DiscoverCard component
export default defineComponent({
  // Component name
  name: 'DiscoverCard',
  // Define props expected by the component
  props: {
    // Title of the card
    title: {
      type: String,
      required: true
    },
    // Description of the card
    text: {
      type: String,
      required: true
    },
    // URL or route to navigate to when the card is clicked
    to: {
      type: String,
      required: true,
    },
  },
  // Setup reactive data for the component
  setup() {
    const hover = ref(false); // Tracks whether the mouse is over the button
    const active = ref(false); // Tracks whether the button is being pressed
    const focused = ref(false); // Tracks whether the button has focus

    return { hover, active, focused }; // Expose reactive data to the template
  },
});
</script>

<template>
  <!-- Wrap the card content in a NuxtLink for navigation -->
  <NuxtLink :to="to">
    <!-- Card container -->
    <div class="card-container">
      <!-- Card -->
      <div class="card">
        <!-- Card content -->
        <div class="card-content">
          <!-- Activity title -->
          <h1 class="card-name">{{ title }}</h1>
          <!-- Activity description -->
          <p class="card-text">{{ text }}</p>
          <!-- Forward arrow icon -->
          <Icon name="ForwardArrowIcon" size="32" />
        </div>
      </div>
    </div>
  </NuxtLink>
</template>

<!-- Styles for the DiscoverCard -->
<style scoped>
/* Card styling */
.card {
  width: 600px;
  height: 380px;
  border-radius: var(--border-radius-card);
  overflow: hidden;
  background-color: var(--white);
  box-shadow: 0px 5px 20px var(--black-shadow);
  transition: transform var(--transition) ease-in-out;
  cursor: pointer;
}

/* Card container styling */
.card-container {
  display: inline-block;
  vertical-align: top;
}

/* Hover effect on card */
.card:hover:not(.is-disabled) {
  background-color: var(--beige-hover);

  .icon {
    color: var(--purple-hover);
  }
}

/* Active effect on card */
.card:active:not(.is-disabled) {
  transform: scale(0.98);
  background-color: var(--beige-active);

  .icon {
    color: var(--purple-active);
  }
}

/* Disabled effect on card */
.card.is-disabled {
  opacity: 0.5;
  background-color: var(--grey3);
  cursor: not-allowed;
}

/* Content styling */
.card-content {
  padding: 0px;
  position: relative;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  text-align: center;
  color: var(--black);
  padding-left: 70px;
  padding-right: 100px;
}

/* Title styling */
.card-name {
  font-family: var(--font-playfair);
  font-size: var(--h4);
  color: var(--black);
  font-weight: var(--semibold);
  margin-top: 2rem;
  margin-bottom: 9px;
  text-align: left;
  line-height: 80px;
}

/* Text styling */
.card-text {
  flex-grow: 1;
  font-family: var(--font-montserrat);
  color: var(--grey1);
  font-size: var(--body3);
  line-height: var(--l-height3);
  font-weight: var(--medium);
  text-align: left;
}

/* Icon styling */
.icon {
  position: absolute;
  bottom: 40px;
  right: 40px;
}




@media (max-width: 650px){  
  .card{
    width: 80vw;
    height: 330px;
  }
  .card-name {
    font-size: 30px;
    line-height: 47px;
  }
  .card .icon{
    margin-left: 80%;
  }
  .card-text{
    font-size: var(--body1);
    line-height: var(--l-height1);
  }
  .card-content{
    padding: 0 20px;
  }
}

@media screen and (max-width: 450px) {
  .card{
    width: 80vw;
    height: 410px;
  }
}
</style>