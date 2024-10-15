<template>
    <div class="grid grid-cols-2">
        <div>
            <h2 align="center" class="pt-5 text-3xl font-bold text-rose-600">Todoist</h2>
            <div class=" h-full flex flex-col justify-center items-center">
                <h2 class="font-bold text-3xl py-10">
                    Créez votre profil
                </h2>
                <div>
                    <div class="flex  justify-between items-center border border-gray-200 py-3 px-4 rounded-lg w-96">
                        <img src="../icones/upload.png" class="h-5" alt="">
                        <p>
                            Télécharger votre image
                        </p>
                    </div>

                    <div class="flex flex-col justify-between items-start border border-gray-200  px-4 rounded-lg w-96 my-3" :class="{'border-gray-400': nomActif, 'border-gray-200':!nomActif}">
                        <p class="text-sm font-bold">Votre nom</p>
                        <input type="text" placeholder="Ex:Augustin Doist" class="outline-none w-full" @focus="nomActif=true" @blur="nomActif=false">
                    </div>


                    <div class="flex  justify-between items-center border border-gray-200 py-3 px-4 rounded-lg w-96">
                        <p class="text-sm">
                            Je souhaite utiliser Todoist avec mon équipe
                        </p>
                        <div class="bg-gray-500 w-14 h-7 flex items-center rounded-full cursor-pointer" @click="toggleBtn">
                            <div id="circle" class="relative left-1 bg-white w-6 h-6 rounded-full transition-transform duration-500">
                                
                            </div>
                        </div>
                    </div>

                    <div class="flex justify-center items-center border border-gray-200 py-3 px-4 rounded-lg w-96 my-3 text-white bg-rose-300 font-bold text-xl">
                        Continuer
                    </div>
                </div>
            </div>
        </div>
        <div class="bg-rose-50 h-screen">VRAI</div>
    </div>
    
</template>

<script setup>
    import {ref} from 'vue';

    const nomActif = ref(false);
    const toggleBtn = ()=>{
        const circle = document.querySelector('#circle');
        circle.classList.toggle('translate-x-6');
    }
</script>
