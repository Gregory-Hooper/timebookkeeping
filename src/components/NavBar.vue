<template>
    
<div class="head">
        <v-row>
            <v-col cols="12">
                <div class="mt-10" style="position: absolute; z-index: 9999; top: 0px; margin-left: auto; margin-right: auto; left: 0; right: 0; text-align: center;">
                    <v-img class="h-auto w-auto" src="GoldDog1.png" contain max-height="220"></v-img>
                </div>
            </v-col>
        </v-row>
        <v-row>
            <v-col cols="12">
                <div class="mt-14" style="position: absolute; z-index: 9999; top: 170px; margin-left: auto; margin-right: auto; left: 0; right: 0; text-align: center;">
                    <h1 class="text-white text-h4 text-md-h3 text-lg-h2" style="font-family:'Newsreader !important;' ">TIME BOOKKEEPING </h1>
                    <span class="slogon text-h6 text-md-h4 text-lg-h3 ">BOOKKEEPING BEYOND NUMBERS, BECAUSE YOUR TIME MATTERS</span><br />
                </div>
            </v-col>
        </v-row>
        <v-row>
            <v-col cols="12">
            <div style="position: absolute; z-index: 9999; bottom: 10px; left: 0; right: 0; text-align: center;">
                <v-btn text @click="scroll('about')" class="text-black mx-2">About</v-btn>
                <v-btn text @click="scroll('services')" class="text-black mx-2">Services</v-btn>
                <v-btn text @click="scroll('contact')" class="text-black mx-2">Get in Touch</v-btn>
            </div>
            </v-col>
        </v-row>
    </div>
</template>
<script>
export default {
    methods: {
        scroll(refName){
            const element = document.getElementById(refName);
            element.scrollIntoView({behavior: "smooth"});
        }
    }
}
</script>
<style>
.head {
  position: relative;
  text-align: center;
  height: 420px;
  width: 100%;
  color: white;
}
.head:before{
  content: " ";
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width:50%;
  background: linear-gradient(to right, #737e7f, #1d2123);
  transform: skew(0deg,4deg);
}
.head:after{
  content: " ";
  position: absolute;
  top: 0;
  right: 0;
  height: 100%;
  width:50%;
  background: linear-gradient(to right, #1d2123, #737e7f);
  transform: skew(0deg,-4deg);
}

.slogon{
  background-image: linear-gradient(to top, #494e54, #f5e07a,white);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  text-align:center;
  font-family:'Newsreader';
}

</style>