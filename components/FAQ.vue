<template>
  <div class="flex items-center justify-center p-4 lg:p-0 ">
    <div class=" lg:w-2/3 ">
      <SectionHeaderCenter title="HVAC Knowledge Hub" content="Common HVAC Queries" header="Frequently asked questions" />
      <UAccordion multiple :items="items" :ui="{
        wrapper: 'flex flex-col w-full', item: {
          size: 'text-base',
          color: '',
padding:'p-4'
        }
      }">
        <template #default="{ item, index, open }">
          <Button
            class="  hover:bg-blue-200/20 border-b flex items-center justify-between border-gray-200 dark:border-gray-700 gap-1"
            :class="open && 'bg-[var(--aero)]  rounded'">
            <div class="rounded-full  ">
              <Icon :name="item.icon" class="text-4xl text-white " />
            </div>
            <span class="truncate">{{ index + 1 }}. {{ item.label }}</span>
            <Icon name="i-heroicons-chevron-right-20-solid"
              class="w-10 h-10 ms-auto transform transition-transform duration-200" :class="[open && 'rotate-90']" />
          </Button>
        </template>
      </UAccordion>
    </div>
  </div>
</template>

<script lang="ts" setup>
import Button from './Globals/Button.vue'
const items = [{
  label: 'Heating System Maintenance',
  icon: 'bi:thermometer-sun',
  defaultOpen: true,
  content: 'Ensure your heating system runs smoothly with our comprehensive maintenance services. Our expert technicians will inspect, clean, and optimize your heating system, keeping your home warm and comfortable throughout the colder seasons.'
}, {
  label: 'Air Conditioning Installation',
  icon: 'material-symbols:air-purifier',
  content: 'Thinking about installing a new air conditioning system? Our HVAC professionals specialize in efficient and reliable air conditioning installations. Experience cool and refreshing indoor air during hot summer days.'
}, {
  label: 'Energy-Efficient Thermostats',
  icon: 'material-symbols:lightbulb-rounded',
  content: 'Upgrade to energy-efficient thermostats for optimized heating and cooling. Our team can recommend and install smart thermostats to help you save on energy costs while maintaining a comfortable indoor environment.'
}, {
  label: 'Ventilation Solutions',
  icon: 'material-symbols:directory-sync',
  content: 'Improve indoor air quality and ventilation with our HVAC solutions. We offer ventilation system assessments and installations to ensure the air circulating in your home is fresh, clean, and free from pollutants.'
}, {
  label: 'Emergency HVAC Repairs',
  icon: 'jam:tools-f',
  content: 'Facing a sudden HVAC breakdown? Our emergency repair services have you covered. Contact us 24/7, and our skilled technicians will promptly address and resolve any unexpected heating or cooling issues.'
}, {
  label: 'Ductwork Inspection and Cleaning',
  icon: 'solar:clipboard-list-bold',
  content: 'Maintain efficient airflow and prevent allergens by scheduling regular ductwork inspections and cleanings. Our HVAC experts will ensure that your ducts are in optimal condition for a healthier and more comfortable living environment.'
}];
</script>

<style></style>