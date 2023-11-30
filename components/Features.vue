<template>

  <SectionHeaderCenter title="What we provide"
    content="Elevate Comfort with Our Expert Heating, Air Conditioning, and Indoor Air Quality Services."
    header="Optimized HVAC Solutions" />
  <div class="flex w-full flex-col items-center justify-center p-4 lg:p-10">
    <div class="features">
 
      <div class="feature shadow-2xl shadow-purple-500/10 group" v-for="feature in featureItems">
          <div class="feature-content    ">
            <Icon :name="feature.icon"  class="text-8xl group-hover:text-amber-300 "/>
            <span class="text-3xl font-bold  group-hover:text-amber-300 transition-colors duration-300">{{ feature.title }}</span>
            <span>{{ feature.content }}</span>
          </div>
        </div>
      
    </div>
  </div>
</template>

<script  setup>
import  Button from "./Globals/Button.vue";


const featureItems = [
  {
    title: 'Furnaces',
    icon: 'game-icons:furnace',
    content: `Ensure your home stays comfortably warm with Frontier's Furnace expertise. Our skilled technicians, equipped with advanced tools, promptly address and resolve various Furnace issues. Trust us for professional Furnace services, where your warmth is our priority.`,
  },

  {
    title: 'Air Conditioners',
    icon: 'icon-park-outline:air-conditioning',
    content: `Elevate your indoor comfort with Frontier's top-notch Air Conditioning services. Our skilled technicians specialize in promptly addressing and resolving Air Conditioning issues.`,
  },
  {
    title: 'Gas Piping',
    icon: 'mdi:pipe-disconnected',
    content: `Frontier Heating & Air Conditioning ensures your complete comfort with expert Gas Piping services. From installation to maintenance and repair, we handle it all with expertise. Trust us for exceptional service and quality craftsmanship.`,
  },
  {
    title: 'Water Heaters',
    icon: 'material-symbols:water-heater',
    content: `Enjoy reliable hot water with Frontier's Water Heater solutions. Our skilled technicians promptly address and resolve various Water Heater issues. Trust us for professional Water Heater services, ensuring your comfort is our priority.`,
  },

  {
    title: 'Pool Heaters',
    icon: 'material-symbols-light:water-heater-outline',
    content: `Extend your pool season with Frontier's Pool Heater expertise. Our skilled technicians specialize in promptly addressing and resolving Pool Heater issues.`,
  },
  {
    title: 'Ductless Systems',
    icon: 'mingcute:air-condition-fill',
    content: `Frontier Heating & Air Conditioning offers expert Ductless System services. From installation to maintenance and repair, we handle it all with expertise, ensuring exceptional service and quality craftsmanship.`,
  },
];





const theme = {
  get colorWithOpacity() {

    return getColorRGB('purple');
  },
};



onMounted(() => {
  const featuresEl = document.querySelector(".features");
  const featureEls = document.querySelectorAll(".feature");
  featuresEl.addEventListener("pointermove", (ev) => {

    featureEls.forEach((featureEl) => {
      // Not optimized yet, I know
      const rect = featureEl.getBoundingClientRect();
      featureEl.style.setProperty("--x", ev.clientX - rect.left);
      featureEl.style.setProperty("--y", ev.clientY - rect.top);
    });
  });
});
function getColorRGB(color) {
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
function getBackgroundColorClass(color) {
  return `bg-${color}-500`; // Adjust as needed
}

// Method to map color prop to Tailwind CSS text color class
function getTextColorClass(color) {
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
  height: 75vh;
  display: grid;
  grid-column-gap: 0.3rem;
  grid-row-gap: 0.3rem;
  grid-template-columns: repeat(3, 1fr);
   grid-template-rows: repeat(2, 1fr);
  padding: 10px;
@media screen and (max-width: 768px) {
  grid-template-columns: repeat(1, 1fr);
  grid-row-gap: 0.3rem;
  grid-column-gap: 0.3rem;
  padding: 10px;
  
  height: 100vh;
}
}

.feature {
  --x-px: calc(var(--x) * 1px);
  --y-px: calc(var(--y) * 1px);
  --border: 2px;

  border-radius: 0.5rem;
  overflow: hidden;

  background: radial-gradient(800px circle at var(--x-px) var(--y-px),
      v-bind('theme.colorWithOpacity'), transparency 60%,
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
      transparent 60%);

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
