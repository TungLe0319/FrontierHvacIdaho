<script setup lang="ts">
import Button from '../components/Globals/Button.vue'
</script>

<template>
  <main class="  mt-28">
    <div
      class="mx-auto  flex max-w-screen-md flex-col items-center justify-center px-4 py-8 lg:py-16"
    >
      <SectionHeaderCenter
        header="Contact Us"
        title="Get in touch"
        content="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nostrum deserunt, porro quisquam rerum soluta laborum
      impedit veniam voluptate culpa iste at quibusdam, facilis fugit expedita?"
      />
      <div
        class="bg-[var(--midnight-blue)] text-neutral-content rounded-md p-10 shadow-xl"
      >
        <form action="#" class="space-y-8">
          <div class="flex justify-between space-x-8">
            <div class="flex flex-col space-y-8">
              <div>
                <label for="email" class="mb-2 block text-sm font-medium">Your email</label>
                <input
                  id="email"
                  type="email"
                  class="form"
                  placeholder="Email..."
                  required
                >
              </div>
              <div>
                <label for="subject" class="mb-2 block text-sm font-medium">Subject</label>
                <input
                  id="subject"
                  type="text"
                  class="form"
                  placeholder="Subject..."
                  required
                >
              </div>
            </div>
            <div class="flex items-center justify-center">
              <img
                src="https://images.unsplash.com/photo-1610051400050-e03bee86e2ff?auto=format&fit=crop&q=80&w=1470&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
                alt=""
                class="hidden lg:block lg:w-2/3"
              >
            </div>
          </div>
          <div class="sm:col-span-2">
            <label for="message" class="mb-2 block text-sm font-medium">Your message</label>
            <textarea
              id="message"
              rows="6"
              cols="100"
              class="form"
              placeholder="Leave a comment..."
            />
          </div>
          <Button type="submit" class="  rounded  bg-[var(--auburn)]">
            Send message
          </Button>
        </form>
      </div>
    </div>
  </main>
</template>

<style scoped>
.form {
  @apply rounded-md p-2 ring-2 ring-amber-400 focus:ring bg-[var(--night)];
}


</style>
