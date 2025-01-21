<script setup>
import IconWhatsapp from '../icons/IconWhatsapp.vue'
import IconInstagram from '../icons/IconInstagram.vue'
import IconMail from '../icons/IconMail.vue'

import {RouterLink} from 'vue-router'



const links=[
    {name:"Home",link:"/"},
    {name:"Listings",link:"/"},
    {name:"Contact",link:"/"},
  
]
</script>

<template>
    <div class="p-4 h-auto flex justify-center gap-2">
    
    <div class="">

    <div class="py-2"><h1 class="text-3xl text-center font-bold">Abmara <span class="text-rose-600">Properties</span></h1></div>
    <div class="py-5"><h4 class="text-2xl text-center">Let us find your forever home</h4></div>
    
    <div class="py-5 flex justify-center gap-1">
        <div class="flex flex-row gap-3">
            <RouterLink  to="/"> <IconWhatsapp /></RouterLink>
            <RouterLink  to="/"> <IconInstagram/></RouterLink>
            <RouterLink  to="/"> <IconMail/></RouterLink>
        </div>
     </div>


     <div class="py-2 flex justify-center gap-1">
        <div class="flex  flex-col md:flex-row gap-6">
          <RouterLink v-for="link in links" class="mx-3 hover:underline ":to="link.link">{{ link.name }}</RouterLink>

      </div></div>      

     <div class="py-5">
        <h1 class="text-center text-lg text-gray-500">All rights reserved to abmara.co.ke</h1>
     </div>
       
</div>
</div>  
</template>