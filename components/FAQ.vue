<template>
  <div class="flex items-center justify-center p-4 lg:p-0 ">
    <div class=" lg:w-2/3 ">
      <SectionHeaderCenter title="HVAC Knowledge Hub" content="Common HVAC Queries" header="Frequently asked questions" />
      <div class=" mt-24">
        <v-expansion-panels color="blue-lighten-3" multiple>
          <v-expansion-panel v-for="(item, index) in items" :key="index" :title="item.label"
            text="Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi, ratione debitis quis est labore voluptatibus! Eaque cupiditate minima">
            <template v-slot:title>
              <Icon :name="item.icon" class="text-4xl  " />
              <div class=" ml-4 font-semibold">
                {{ item.label }}
              </div>
            </template>
          </v-expansion-panel>
        </v-expansion-panels>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>


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