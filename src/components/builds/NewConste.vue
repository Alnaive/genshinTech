<template>
    <section> 
        <ul class="flex flex-col w-[70px]  bg-transparent absolute left-[10px] bottom-2 ">
            <li v-if="build.conste > 0" >
                <div>
                    <div v-if="build.conste >= 1" class="hero w-14 h-14" :style="{backgroundImage: 'url('+ constBorder() +')'}" >
                        <div  class="hero-content text-center text-neutral-content">
                            <img :src="`https://res.cloudinary.com/genshin/image/upload/sprites/${build.character.Consts[0]}.png`" alt="">
                        </div>
                    </div>
                    <div v-else class="hero w-14 h-14" style="background-image: url('/images/svg/Const.svg');">
                        <div  class="hero-content text-center text-neutral-content">
                            <img :src="`https://res.cloudinary.com/genshin/image/upload/sprites/${build.character.Consts[0]}.png`" alt="">
                        </div>
                    </div>
                </div>
                <div>
                    <div v-if="build.conste <= 1" class="hero w-14 h-14" style="background-image: url('/images/svg/Const.svg');">
                        <div  class="hero-content text-center text-neutral-content">
                            <img :src="`https://res.cloudinary.com/genshin/image/upload/sprites/${build.character.Consts[1]}.png`" alt="">
                        </div>
                    </div>
                    <div v-else class="hero w-14 h-14" :style="{backgroundImage: 'url('+ constBorder() +')'}">
                        <div  class="hero-content text-center text-neutral-content">
                            <img :src="`https://res.cloudinary.com/genshin/image/upload/sprites/${build.character.Consts[1]}.png`" alt="">
                        </div>
                    </div>
                </div>
                <div>
                    <div v-if="build.conste <= 2" class="hero w-14 h-14" style="background-image: url('/images/svg/Const.svg');">
                        <div  class="hero-content text-center text-neutral-content">
                            <img :src="`https://res.cloudinary.com/genshin/image/upload/sprites/${build.character.Consts[2]}.png`" alt="">
                        </div>
                    </div>
                    <div v-else class="hero w-14 h-14" :style="{backgroundImage: 'url('+ constBorder() +')'}">
                        <div  class="hero-content text-center text-neutral-content">
                            <img :src="`https://res.cloudinary.com/genshin/image/upload/sprites/${build.character.Consts[2]}.png`" alt="">
                        </div>
                    </div>
                </div>
                <div>
                    <div v-if="build.conste <= 3" class="hero w-14 h-14" style="background-image: url('/images/svg/Const.svg');">
                        <div  class="hero-content text-center text-neutral-content">
                            <img :src="`https://res.cloudinary.com/genshin/image/upload/sprites/${build.character.Consts[3]}.png`" alt="">
                        </div>
                    </div>
                    <div v-else class="hero w-14 h-14" :style="{backgroundImage: 'url('+ constBorder() +')'}">
                        <div  class="hero-content text-center text-neutral-content">
                            <img :src="`https://res.cloudinary.com/genshin/image/upload/sprites/${build.character.Consts[3]}.png`" alt="">
                        </div>
                    </div>
                </div>
                <div>
                    <div v-if="build.conste <= 4" class="hero w-14 h-14" style="background-image: url('/images/svg/Const.svg');">
                        <div  class="hero-content text-center text-neutral-content">
                            <img :src="`https://res.cloudinary.com/genshin/image/upload/sprites/${build.character.Consts[4]}.png`" alt="">
                        </div>
                    </div>
                    <div v-else class="hero w-14 h-14" :style="{backgroundImage: 'url('+ constBorder() +')'}">
                        <div  class="hero-content text-center text-neutral-content">
                            <img :src="`https://res.cloudinary.com/genshin/image/upload/sprites/${build.character.Consts[4]}.png`" alt="">
                        </div>
                    </div>
                </div>
                <div>
                    <div v-if="build.conste <= 5" class="hero w-14 h-14" style="background-image: url('/images/svg/Const.svg');">
                        <div  class="hero-content text-center text-neutral-content">
                            <img :src="`https://res.cloudinary.com/genshin/image/upload/sprites/${build.character.Consts[5]}.png`" alt="">
                        </div>
                    </div>
                    <div v-else class="hero w-14 h-14" :style="{backgroundImage: 'url('+ constBorder() +')'}">
                        <div  class="hero-content text-center text-neutral-content">
                            <img :src="`https://res.cloudinary.com/genshin/image/upload/sprites/${build.character.Consts[5]}.png`" alt="">
                        </div>
                    </div>
                </div>
            </li>
            <li v-else>
                <div v-for="cons in build.character.Consts" :key="cons" class="hero w-14 h-14" style="background-image: url('/images/svg/Const.svg');">
                    <div class="hero-content text-center text-neutral-content">
                        <img :src="`https://res.cloudinary.com/genshin/image/upload/sprites/${cons}.png`" alt="">
                    </div>
                </div>
            </li>
        </ul>
    </section>
</template>

<script>
export default {
    props: [ 'build'],
    methods:{
            constBorder(){
                const ele = this.build.character.element;
                if(ele == "Ice"){
                    return "/images/svg/Const_Cryo.svg";
                } else if(ele == "Rock"){
                    return "/images/svg/Const_Geo.svg";
                } else if(ele == "Grass"){
                    return "/images/svg/Const_Dendro.svg";
                } else if(ele == "Wind"){
                    return "/images/svg/Const_Anemo.svg";
                } else if(ele == "Electric"){
                    return "/images/svg/Const_Electro.svg";
                } else if(ele == "Water"){
                    return "/images/svg/Const_Hydro.svg";
                } else if(ele == "Fire"){
                    return "/images/svg/Const_Pyro.svg";
                } 
            },
    }
}
</script>