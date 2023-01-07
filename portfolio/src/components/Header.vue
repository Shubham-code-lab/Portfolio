<template>
  <div>
    <div class="bg-slate-800 h-full">
    <nav class="md:flex md:flex-row md:justify-end">
        <ul class="flex flex-row justify-evenly md:w-1/2 p-3">
            <li><a href="#" class="text-white hover:text-green-700">Home</a></li>
            <li><a href="#" class="text-slate-50 hover:text-green-700">Skill</a></li>
            <li ><a href="#" class="text-slate-100 hover:text-green-700">Experience</a></li>
            <li ><a href="#" class="text-slate-200 hover:text-green-700">Projects</a></li>
            <li ><a href="#" class="text-slate-300 hover:text-green-700">Education</a></li>
        </ul>
    </nav>
    <div class="md:flex flex-row  h-1/2">
      <div class="flex flex-row justify-center items-center md:w-1/2  h-1/2 md:h-full">
        <div class="w-1/2 text-center font-sans text-3xl sm:text-4xl lg:text-5xl xl:text-6xl 2xl:text-7xl font-extrabold bg-clip-text text-transparent bg-gradient-to-r from-green-700 to-green-200">SHUBHAM SHINDE</div>
      </div>
      <div class="flex flex-row justify-center items-center md:w-1/2  h-full md:h-full">
        <div>{</div>
        <!-- 3/4 =75% 1/3 =33%  3/5=60% 5/12=41% -->
        <ul class="flex h-3/4 flex-row w-3/5 md:w-1/2 2xl:w-1/3 relative bg-red-600 ">
            <li ref="leftImage" class="absolute left-1/2 h-1/2 w-5/12 z-10 top-1/2 translate-x-[-110%] translate-y-[-50%]">
                <img class="object-cover h-full w-full" src="../assets/images/img1.jpg" alt="">
            </li>
            <li ref="middleImage" class="absolute left-1/2 h-3/4 w-3/5 z-30 top-1/2 translate-x-[-50%] translate-y-[-50%]">
                <img class="object-cover h-full w-full" src="../assets/images/img2.jpg" alt="">
            </li>
            <li ref="rightImage" class="absolute left-1/2 h-1/2 w-5/12 z-10 top-1/2 translate-x-[10%] translate-y-[-50%]">
                <img class="object-cover h-full w-full" src="../assets/images/img3.jpg" alt="">
            </li>   
        </ul>
        <div>}</div>
      </div>
    </div>
    </div>
  </div>
</template>

<script>
import {ref} from 'vue';
export default {
    setup(){
        const leftImage = ref(null);
        const middleImage = ref(null);
        const rightImage = ref(null);
        const count = 1;
        setInterval(()=>{
            leftImage.value.classList.remove('');
            leftImage.value.classList.add('');
            
            middleImage.value.classList.remove('');
            middleImage.value.classList.add('');

            rightImage.value.classList.remove('');
            rightImage.value.classList.add('');
        },2000);
        
        return {
            leftImage,
            middleImage,
            rightImage
        }
    }
};
</script>

<style>
</style>