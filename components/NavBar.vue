<script setup lang="ts">
import { onBeforeUnmount, onMounted, ref } from 'vue'
import Button from './Globals/Button.vue'
// const { session } = useAuth();
const navTransform = ref('translateY(0)')

let lastScrollPosition = 0

const route = useRoute()
route.path

function handleScroll() {
  const scrollY = window.scrollY;

  // Adjust the threshold value (200) based on your specific requirement
  const scrollThreshold = 200;

  navTransform.value =
    scrollY > lastScrollPosition && scrollY > scrollThreshold
      ? 'translateY(-100%)'
      : 'translateY(0)';

  lastScrollPosition = scrollY;
}

function handleIndicator(el: HTMLElement) {
  const indicator = document.querySelector('.nav-indicator') as HTMLElement
  const items = document.querySelectorAll('.nav-item')

  items.forEach((item) => {
    item.classList.remove('is-active')
    item.removeAttribute('style')
  })

  indicator.style.width = `${el.offsetWidth}px`
  indicator.style.left = `${el.offsetLeft}px`

  const activeColor = el.getAttribute('active-color')
  if (activeColor !== null) {
    indicator.style.backgroundColor = activeColor
    el.style.color = activeColor
  }

  el.classList.add('is-active')
}

interface HTMLElementWithActiveClass extends HTMLElement {
  classList: DOMTokenList & {
    contains(token: string): boolean
  }
}
// Function to setup listeners
function setupIndicatorListeners() {
  const items: NodeListOf<HTMLElement> = document.querySelectorAll('.nav-item')
  const indicator: HTMLElement | null
    = document.querySelector('.nav-indicator')

  items.forEach((item: HTMLElement) => {
    if (item.getAttribute('href') === route.path) {
      item.classList.add('is-active')
      handleIndicator(item)
    }
    item.addEventListener('click', e =>
      handleIndicator(e.target as HTMLElement))
    if ((item as HTMLElementWithActiveClass).classList.contains('is-active'))
      handleIndicator(item)
  })
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
  setupIndicatorListeners()
})

onBeforeUnmount(() => {
  window.removeEventListener('scroll', handleScroll)
})




const isOpen = ref(false)



</script>

<template>
  <div ref="nav"
    class="fixed top-0 z-50 lg:flex  w-full items-center lg:justify-around gap-4 lg:gap-0 bg-white p-2 text-gray-900 shadow-md transition-transform duration-300 ease-in-out"
    :style="{ transform: navTransform }">
    <div class="lg:w-1/3 px-2 hidden  lg:flex  ">
      <div class=" lg:text-4xl font-bold p-2 text-center w-full ">
        FrontierHvacIdaho
      </div>
    </div>
    <div class="lg:w-2/3 px-2">
      <div class=" hidden lg:flex gap-4 justify-end w-full ">
        <Button class="  hover:text-[var(--auburn)] bg-transparent   flex items-center justify-center gap-2 ">
          <Icon name="uis:schedule" size="30" />
          <span class="text-3xl">Schedule Now</span>
        </Button>
        <Button class="  hover:text-[var(--auburn)]  bg-transparent flex items-center justify-center gap-2 ">
          <Icon name="carbon:star-review" size="30" />
          <span class="text-sm">Review us on google</span>
        </Button>
        <Button class=" rounded-full  bg-[var(--auburn)]  text-white shadow-md flex items-center justify-center gap-2">
          <Icon name="material-symbols:call" size="30" />
          <span>1-208-921-232</span>
        </Button>
      </div>
      <div class="flex w-full items-center lg:justify-end">
          <Button class="bg-transparent lg:hidden block" label="Open" @click="isOpen = true">
            <Icon name="solar:hamburger-menu-linear" class="text-4xl" />
          </Button>
           <!-- OPEN & NAV BUTTONS -->
   <div class=" lg:hidden bloc lg:text-4xl font-bold p-2 text-center w-full ">
          FrontierHvacIdaho
        </div>
           
      
        <div class="relative hidden w-fit overflow-hidden lg:inline-flex">
          <NuxtLink href="/" class="nav-item is-active" active-color="red">
            Home
          </NuxtLink>
      
          <NuxtLink href="/contact" class="nav-item" active-color="red">
            Contact
          </NuxtLink>
          <span class="nav-indicator" />

               <!-- OPEN & NAV BUTTONS -->
        </div>
        <USlideover v-model="isOpen" :ui="{
          background: 'dark:bg-white',

        }">
          <div class="  flex flex-col items-center h-full  justify-between ">

            <!-- CLOSE & NAV BUTTONS -->
            <div class="flex flex-col w-full items-center justify-center text-black text-6xl">
              <div class="flex w-full justify-start">
                <Button color="gray" @click="isOpen = false">
                  <Icon name="material-symbols:cancel-rounded" class="text-5xl text-black" />
                </Button>
              </div>
              <NuxtLink href="/" class="nav-item is-active" active-color="red">
                Home
              </NuxtLink>
             
              <NuxtLink href="/contact" class="nav-item" active-color="red">
                Contact</NuxtLink>
            </div>
              <!-- CLOSE & NAV BUTTONS -->
              <!-- ======================================== -->
              <!-- ACTION BUTTONS -->
            <div class="flex flex-col items-center  space-y-8 justify-center w-full pb-24 text-3xl ">
              <Button
                class="  rounded-full border-2 border-[var(--auburn)] text-[var(--auburn)]    hover:text-[var(--auburn)] bg-transparent   flex items-center justify-center gap-2 ">
                <Icon name="uis:schedule"  class="text-5xl" />
                <span class="">Schedule Now</span>
              </Button>
              <Button
                class=" rounded-full  border-2 border-[var(--auburn)] text-[var(--auburn)]  bg-transparent flex items-center justify-center gap-2 ">
                <Icon name="carbon:star-review"  class="text-5xl" />
                <span class="text-3xl">Review us on google</span>
              </Button>
              <Button class=" rounded-full  bg-[var(--auburn)]   shadow-md flex items-center justify-center gap-2">
                <Icon name="material-symbols:call"  class="text-5xl" />
                <span>1-208-921-232</span>
              </Button>
            </div>
               <!-- ACTION BUTTONS -->
          </div>
        </USlideover>
      </div>
    </div>
  </div>
</template>

<style scoped>
.nav-item {
  padding: 20px;
  transition: 0.3s;
  margin: 0 6px;
  z-index: 1;
  font-weight: bold;

  position: relative;
}

.nav-item:before {
  content: "";
  position: absolute;
  bottom: -6px;
  left: 0;
  width: 100%;
  height: 5px;
  background-color: #801616;
  border-radius: 8px 8px 0 0;
  opacity: 0;
  transition: 0.3s;
}

.nav-item:not(.is-active):hover:before {
  opacity: 1;
  bottom: 0;
}

.nav-indicator {
  position: absolute;
  left: 0;
  bottom: 0;
  height: 4px;
  transition: 0.4s;
  height: 5px;
  z-index: 1;
  border-radius: 8px 8px 0 0;
}

@media (max-width: 580px) {
  .nav {
    overflow: auto;
  }
}
</style>
