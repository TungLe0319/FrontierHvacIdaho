<template>

  <RippleDiv>
   
  </RippleDiv>
  <SectionHeaderCenter title="What we provide"
      content="Elevate Comfort with Our Expert Heating, Air Conditioning, and Indoor Air Quality Services."
      header="Optimized HVAC Solutions" />
  <div class="flex w-full flex-col items-center justify-center">
    <div class="features">
      <div class="feature" v-for="feature in featureItems">
        <div class="feature-content   " >
          <Icon :name="feature.icon" size="100" />
          <span class="text-3xl font-bold">{{ feature.title }}</span>
          <span>{{ feature.content }}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>

const featureItems = [
  {
    title: 'Heating',
    icon: 'ph:sun-dim-duotone',
    content: `Ensure reliable warmth with Frontier's General Heating services. Our skilled technicians, equipped with advanced tools, promptly address and resolve various General Heating issues. Trust us for professional General Heating services, where your comfort is our priority.`,
  },

  {
    title: 'Air Quality',
    icon: 'material-symbols:air-rounded',
    content: `Elevate your living spaces with Frontier's top-notch Indoor Air Quality services. Our skilled technicians specialize in promptly addressing and resolving Indoor Air Quality issues. `,
  },
  {
    title: 'Cooling',
    icon: 'solar:snowflake-bold-duotone',
    content: `Frontier Heating & Air Conditioning is your go-to for complete Air Conditioning system services. From installation to maintenance and repair, we handle it all with expertise. We are known for exceptional service and quality craftsmanship.`,
  },
]




type TailwindColor = 'amber' | 'gray' | 'red' | 'purple' | 'emerald'; // Add more colors as needed
const theme = {
  get colorWithOpacity() {

    return getColorRGB('purple');
  },
};



onMounted(() => {
  const featuresEl = document.querySelector(".features");
  const featureEls = document.querySelectorAll(".feature");
  featuresEl!.addEventListener("pointermove", (ev) => {
    featureEls.forEach((featureEl) => {
      // Not optimized yet, I know
      const rect = featureEl.getBoundingClientRect();
      featureEl.style.setProperty("--x", ev.clientX - rect.left);
      featureEl.style.setProperty("--y", ev.clientY - rect.top);
    });
  });
});
function getColorRGB(color: TailwindColor): string {
  // Add logic to map Tailwind color names to RGB values
  // For simplicity, you can provide predefined RGB values here
  switch (color) {
    case 'amber':
      return 'rgba(246, 199, 59, 0.2)';
    case 'gray':
      return 'rgba(169, 169, 169, 0.2)';
    case 'red':
      return 'rgba(255, 0, 0, 0.2)';
    case 'purple':
      return 'rgba(128, 0, 128, 0.2)';
    case 'emerald':
      return 'rgba(0, 128, 0, 0.2)';
    default:
      return 'rgba(246, 199, 59, 0.2)';  // Default to amber if color is not recognized
  }
}





// Method to map color prop to Tailwind CSS background color class
function getBackgroundColorClass(color: TailwindColor): string {
  return `bg-${color}-500`; // Adjust as needed
}

// Method to map color prop to Tailwind CSS text color class
function getTextColorClass(color: TailwindColor): string {
  return `text-${color}-900`; // Adjust as needed
}


</script>

<style scoped>
*,
*:before,
*:after {
  box-sizing: border-box;
  position: relative;
}

.features {
  width: 100%;
  height: 40vh;
  display: grid;
  grid-column-gap: 0.3rem;
  grid-row-gap: 0.3rem;
  grid-template-columns: repeat(3, 1fr);
padding: 10px;

}

.feature {
  --x-px: calc(var(--x) * 1px);
  --y-px: calc(var(--y) * 1px);
  --border: 2px;

  border-radius: 0.5rem;
  overflow: hidden;

  background: radial-gradient(800px circle at var(--x-px) var(--y-px),
      v-bind('theme.colorWithOpacity'), transparency 40%,
    );
}



.feature:before,
.feature:after {
  content: "";
  display: block;
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  inset: 0px;
  border-radius: inherit;
  background: radial-gradient(800px circle at var(--x-px) var(--y-px),
      v-bind('theme.colorWithOpacity'),
      transparent 40%);

}

.feature:before {
  z-index: 1;
}

.feature:after {
  opacity: 5%;
  z-index: 2;
  transition: opacity 0.4s ease;
}

.feature:hover:after {
  opacity: 1;
}

.feature-content {
  background: #131315;
  border-radius: inherit;

  padding: 10px;
  z-index: 1;

  position: absolute;
  inset: var(--border);
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: center;

}
</style>
