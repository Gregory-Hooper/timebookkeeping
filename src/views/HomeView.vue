<template>
  <v-app id="home">
    <NavBar />
    <v-container fluid>
      <v-row>
        <v-col cols="12" class="mt-5" id="about">
          <div class="about">
            <v-row>
              <v-col cols="12" class="mt-7">
                <div><v-divider style="width: 100%;" class="border-opacity-100" color="#d9bd2d"></v-divider></div>
                <h2 class="headerLabel mt-2 text-center">ABOUT TIME</h2>
                <div><v-divider style="width: 100%;" class="border-opacity-100" color="#d9bd2d"></v-divider></div>
              </v-col>
            </v-row>
            <v-row>
              <v-col cols="12" sm="4">
                <div class="egg">
                  <v-img class=".d-sm-none .d-lg-none" src="i2.png" max-height="300"></v-img>
                </div>
              </v-col>
              <v-col cols="12" sm="8">
                  <br/>
                   <p class="text-grey text-center">Time Bookkeeping is a Freelance Service Provider which is dedicated to revolutionizing the way businesses manage their finances. Specializing in freelance bookkeeping services, we offer a tailored approach to suit the unique needs of each client.</p>
                  <br/>
                  <p class="text-grey text-center">Our team of skilled professionals is committed to delivering accurate and timely financial solutions, ensuring that clients can focus on their core business activities while we handle the intricacies of bookkeeping. With a customer-centric mindset, Time Bookkeeping takes pride in fostering long-lasting partnerships, providing reliable support, and contributing to the financial success of businesses across diverse industries. Trust us to keep your time and finances in order, empowering you to thrive in your endeavors.</p>
              </v-col>
            </v-row>

          </div>
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="12" id="services">
          <div class="services" >
            <v-row>
                <v-col cols="12" class="mt-7 ">
                  <v-divider style="width: 100%;" class="border-opacity-100" color="#d9bd2d"></v-divider>
                  <h2 class="headerLabel mt-2 text-center">SERVICES</h2>
                  <v-divider style="width: 100%;" class="border-opacity-100" color="#d9bd2d"></v-divider>
                </v-col>
              </v-row>
            <v-row>
              <v-col cols="12" sm="4">
                <v-card class="mx-auto" max-width="350" height="100%">
                  <v-img src="book-keeping.jpg" height="200px" cover></v-img>

                  <v-card-title> BOOKKEEPING </v-card-title>

                  <v-card-text>
                    Optimize your business finances with our freelance bookkeeping services. 
                    From meticulous record-keeping to strategic financial insights, we ensure accuracy and efficiency. 
                  </v-card-text>
                </v-card>
              </v-col>
              <v-col cols="12" sm="4">
                <v-card class="mx-auto" max-width="350" height="100%">
                  <v-img src="Invoicing.jpg" height="200px" cover></v-img>

                  <v-card-title> INVOICING </v-card-title>

                  <v-card-text>
                    Streamline your invoicing process with our freelance invoicing services. We ensure timely, accurate, and professional invoicing, allowing you to focus on your work while we handle the financial details seamlessly.
                  </v-card-text>
                </v-card>
              </v-col>
              <v-col cols="12" sm="4">
                <v-card class="mx-auto" max-width="350" height="100%">
                  <v-img src="otherServices.jpg" height="200px" cover></v-img>

                  <v-card-title> OTHER </v-card-title>

                  <v-card-text>
                    Efficiently manage your administrative tasks with our freelance services, specializing in data capturing. We ensure precise and organized data handling, allowing you to streamline operations effortlessly.
                  </v-card-text>
                </v-card>
              </v-col>
            </v-row>
          </div>
        </v-col>
      </v-row>
      <v-row class="getintouch">
        <v-col cols="12" sm="12" class="px-16" id="contact">
          <div class="getintouch">
          <v-row>
            <v-col cols="12" class="mt-7">
              <v-divider style="width: 100%;" class="border-opacity-100" color="#d9bd2d"></v-divider>
              <h2 class="headerLabel mt-2">GET IN TOUCH</h2>
              <v-divider style="width: 100%;" class="border-opacity-100" color="#d9bd2d"></v-divider>
            </v-col>
          </v-row>
          <v-row>
            <v-col cols="12" sm="9">
                <h1 class="text-center">Contact Us</h1>
                <v-divider></v-divider>
                <br/>
                <p>Experience expert services with Time Bookkeeping.
                Contact us touch today for personalized and efficient bookkeeping solutions.</p><br/>
              <form ref="form" @submit.prevent="sendEmail">
                <v-row>
                  <v-col cols=12 sm="6">
                    <v-text-field label="Name" name="user_name" v-model="user_name" persistent-hint variant="outlined"></v-text-field>
                  </v-col>
                  <v-col cols=12 sm="6">
                    <v-text-field ref="email" label="Email Address" name="user_email" v-model="user_email" persistent-hint variant="outlined"></v-text-field>
                  </v-col>
                </v-row>
                <v-textarea  label="Message" name="message" v-model="message" persistent-hint variant="outlined"></v-textarea>
                <v-btn type="submit" color="#FBDF7E" class="mt-2">Submit Now</v-btn>
              </form>
            </v-col>
            <v-col cols="12" sm="3">
              <div class="contact">
                <h1 class="text-center">Contact Info</h1>
                <v-divider></v-divider>
                <v-btn icon="fas fa-map-marker-alt" @click="goToLocation" class="mt-10" variant="outlined"></v-btn><br/>
                <span class="text-caption">Century City, Cape Town, South Africa</span><br/>
                <v-btn icon="fas fa-phone-alt" @click="copyCellNumber" class="mt-10" variant="outlined"></v-btn><br/>
                <span class="text-caption" ref="cellNumber" v-on:focus="$event.target.select()" >078 553 4119</span><br/>
                <v-btn icon="fas fa-envelope" @click="mailtTo" class="mt-10" variant="outlined"></v-btn><br/>
                <span class="text-caption">time.bookkeeping@gmail.com</span><br/>
              </div>
            </v-col>
          </v-row>
        </div>
        </v-col>
      </v-row>
    </v-container>
    <FooterView />
 
  </v-app>
  <div class="text-center ma-2">
    <v-snackbar v-model="snackbar">
      {{ snackBarText }}

      <template v-slot:actions>
        <v-btn color="pink" variant="text" @click="snackbar = false">
          Close
        </v-btn>
      </template>
    </v-snackbar>
  </div>
</template>

<script>
import { defineComponent } from 'vue';
import emailjs from '@emailjs/browser';

// Components
import NavBar from '@/components/NavBar.vue';
import FooterView from '@/components/FooterView.vue';

export default defineComponent({
  name: "HomeView",
  data() {
    return {
      user_name: "",
      user_email: "",
      message: "",
      snackbar: false,
      snackBarText: "",
      snackBarTimer: "",
    };
  },
  components: {
    NavBar,
    FooterView
  },
  methods: {
    sendEmail(){
      // eslint-disable-next-line
      var mailformat = /^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,3})+$/;

      if (this.snackBarTimer){
        window.clearInterval(this.snackBarTimer);      
      }
      
      if (this.user_email == "") {
        this.displaySnackBar("Please make sure you have added your email address before submitting");
        return;
      }
      else if(!this.user_email.match(mailformat)){
        this.displaySnackBar("Please make sure your email address is valid before submitting");
        return;
      }

      emailjs.sendForm('service_d1d8m4g', 'template_z9xf8kv', this.$refs.form, 'gq1h5IwyYSaYI10wz')
        .then((result) => {
            console.log('SUCCESS!', result.text);
        }, (error) => {
            console.log('FAILED...', error.text);
        });
    },
    mailtTo: function(){
      window.location = "mailto:hooperblade@gmail.com";
    },
    goToLocation: function(){
      window.open("https://maps.google.com?q="+-33.88690219452499+","+18.514321863997406 );
    },
    copyCellNumber() {
      navigator.clipboard.writeText("078 553 4119");
      this.displaySnackBar("The contact number has been copied");
    },
    displaySnackBar(text){
      if (this.snackBarTimer){
        window.clearInterval(this.snackBarTimer);      
      }
      this.snackbar = true;
      this.snackBarText = text;
      this.snackBarTimer = window.setInterval(() => {
        this.snackBarText = "";
        this.snackbar = false;
      }, 5000)
    }
  }
});
</script>
<style scoped>
.v-container{
  padding: 0 0;
}

.about{
  padding: 0 100px;
  padding-bottom: 10px;
  background-color: #f5f5f5;
}

.getintouch{
  padding-bottom: 10px;
  background-color: #f5f5f5;
}

.headerLabel{
  text-align:center;
  padding:0;
  margin:0;
  font-family:Newsreader;
  color: #494e54;
}

.egg{
  background-image: linear-gradient(to top, #494e54, #f5e07a,#494e54);
  border-radius: 50% 50% 50% 50% / 60% 60% 40% 0%;
}

.contact{
  display: inline-block;
  padding: 0 40px;
  vertical-align: middle;
  text-align: center;
  margin-right: 6px;
  margin-left: 6px;
  padding-bottom: 10px;
  background-color: white;
}

.imgHover{
  padding: 0 200px;
}
.services{
  width:100%;

  text-align: center;
  padding: 0 100px;
}
</style>
