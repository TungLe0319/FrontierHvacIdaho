<template>

 <div class="flex items-center justify-center">
  <div class="w-2/3">
      <SectionHeader header="Heating & Air Conditioning" title="Request a Service or Estimate"
                    content="
Fill out the form below or give us a call to request information about our products and services." />
  </div>
 </div>
    <section class="lg:flex  items-start justify-center mt-32 w-full  ">




      
        <div v-motion-slide-visible-left :delay="200" class="lg:w-1/3 flex flex-col items-center justify-center">
          <h1 class="text-2xl font-bold  text-amber-400 font-serif">Lorem Ipsum Construction</h1>
          <div class="w-full my-10">
            <hr class="h-2 w-full">
          </div>
          <div class=" text-start flex flex-col items-start space-y-5">
            <p class="font-bold">Available Hours:</p>
            <p class="text-center ">Monday - Friday: 9am - 5pm</p>
            <p class="text-center ">Saturday: 10am - 4pm</p>
             <p class="text-center ">Sunday: Closed</p>
          </div>
          <div class="w-full my-10">
            <hr class="h-2 w-full">
          </div>
          <div class=" text-start flex flex-col items-start space-y-5">
            <p class="text-center ">1234 Fake Street</p>
            <p class="text-center ">Fake City, Fake State 12345</p>
            <div class="flex items-center justify-center space-x-4">
              <Icon name="fluent:call-end-16-filled" class="text-amber-400" />
              <a href="tel:123-456-7890" class="text-amber-400">123-456-7890</a>
            </div>
            <div class="flex items-center justify-center space-x-4">
              <Icon name="uil:envelope" class="text-amber-400" />
              <a href="tel:123-456-7890" class="text-amber-400">123fake@email.com</a>
            </div>
          </div>
        </div>
        <div v-motion-slide-visible-right :delay="200" class="lg:w-2/3 ">
          <div class="lg:hidden block text-center font-serif  mt-10 lg:mt-0 ">
            Leave us a message!
             <hr class="h-2 w-full my-10">
          </div>
          <v-form @submit.prevent>
            <v-container>
              <v-row class="mb-4">
                <v-col cols="12" md="6">
                  <v-text-field v-model="firstName" :rules="firstNameRules" label="First name"
                    color="orange-lighten-2"></v-text-field>
                </v-col>
                <v-col cols="12" md="6">
                  <v-text-field v-model="lastName" label="Last name" :rules="lastNameRules"
                    color="orange-lighten-2"></v-text-field>
                </v-col>
                <v-col cols="12">
                  <v-text-field v-model="email" label="E-mail" :rules="emailRules" color="orange-lighten-2"></v-text-field>
                </v-col>
                <v-col cols="12">
                  <v-text-field v-model="subject" label="Subject" :rules="subjectRules"
                    color="orange-lighten-2"></v-text-field>
                </v-col>
              </v-row>
              <v-textarea v-model="content" :rules="contentRule" clearable label="Content"
                color="orange-lighten-2"></v-textarea>
              <v-btn type="submit" variant="outlined" block color="orange-lighten-2" class="mt-2 ">Send a message</v-btn>
            </v-container>
          </v-form>
        </div>

    
      </section>
          <div class=" my-20 border-y-4 border-orange-300 relative">
           <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d23107.716467429007!2d-116.3375111064698!3d43.61768906142244!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x54ae543eef90e923%3A0x6eeda35bd710d3b9!2sThe%20Village%20at%20Meridian!5e0!3m2!1sen!2sus!4v1701667154931!5m2!1sen!2sus" 
          height="450" 
          style="border:0;" 
          allowfullscreen="" 
          loading="lazy" 
          referrerpolicy="no-referrer-when-downgrade"
          class="w-full">
  </iframe>


     <div
        class="absolute z-40 -top-9 left-1/2 -translate-x-1/2  rounded-full   shadow-xl shadow-black/30 border-8 border-black/30  transition-all duration-150 ">
        <Icon name='logos:teamwork-icon' class="text-amber-400 text-6xl" />
      </div>
          </div>
</template>

<script  setup>

const firstName = ref('');
const lastName = ref('');
const email = ref('');
const subject = ref('');
const content = ref('')
const requiredRule = (value) => value ? true : 'This field is required.';
const emailRule = (value) => /.+@.+\..+/.test(value) || 'Enter a valid email address.';

const firstNameRules = [requiredRule];
const lastNameRules = [requiredRule];
const emailRules = [requiredRule, emailRule];
const subjectRules = [requiredRule];
const contentRule = [requiredRule];

</script>

<style>

</style>