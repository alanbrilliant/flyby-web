

<template>
  <div>

    <div id="app">
    <b-navbar toggleable="lg" type="dark"  id="nav">
    <b-navbar-brand href="#"><img src='./assets/flyybylogo.png' alt ='brand' width = '100' height = '35'></b-navbar-brand>
    
     <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav>
        <b-nav-item href="#">Blog</b-nav-item>
        <b-nav-item href="#" disabled>Contact Us</b-nav-item>
      </b-navbar-nav>
      </b-collapse>
    </b-navbar>
    <div class = 'container'>
      <b-row>
        <b-col>
          <b-jumbotron container-fluid='true' id="bigBox" text-variant='white'>
            <template v-slot:header>
              Get
              <span class="typed-text">{{ typeValue }}</span>
              <span class="cursor" :class="{'typing': typeStatus}">&nbsp;</span>the food they need.
            </template>

            <template v-slot:lead>
              No one should have to risk their health to put food on the table.
            </template>
            
            <hr class="my-4">
            <b-row>
            <b-col>
            <p>
              FlyyBy partners with food banks near you to bring contagion-free meals to the most vulnerable people in your lives. Free of charge. 

            </p>
            <hr class="my-5">
            <b-button variant="primary"  id='contact' href="#">Contact Us</b-button>
            <b-button variant="success" id='blog' href="#">Blog</b-button>   
            </b-col>
            <b-col>
            <img src='./assets/flyybydrone.png' alt='our drone' width='400' height="250">
            </b-col>
            </b-row>

          
        </b-jumbotron>

      </b-col>
      <!-- <b-col>
        <p>Hello</p>
      </b-col> -->
      </b-row>
      </div>
    </div>
    <h1>Contact Us</h1>
    <p>Please email us at  achubbic@ucsc.edu</p>
  </div>
  
</template>

<script>
import { setTimeout } from 'timers';
  export default {
    data: () => {
      return {
        typeValue: '',
        typeStatus: false,
        typeArray: ['seniors','patients','working families'],
        typingSpeed: 200,
        erasingSpeed: 100,
        newTextDelay: 2000,
        typeArrayIndex: 0,
        charIndex: 0
      }
    },
    methods: {
      typeText() {
        if(this.charIndex < this.typeArray[this.typeArrayIndex].length) {
          if(!this.typeStatus)
            this.typeStatus = true;
          this.typeValue += this.typeArray[this.typeArrayIndex].charAt(this.charIndex);
          this.charIndex += 1;
          setTimeout(this.typeText, this.typingSpeed);
        }
        else {
          this.typeStatus = false;
          setTimeout(this.eraseText, this.newTextDelay);
        }
      },
      eraseText() {
        if(this.charIndex > 0) {
          if(!this.typeStatus)
            this.typeStatus = true;
          this.typeValue = this.typeArray[this.typeArrayIndex].substring(0, this.charIndex - 1);
          this.charIndex -= 1;
          setTimeout(this.eraseText, this.erasingSpeed);
        }
        else {
          this.typeStatus = false;
          this.typeArrayIndex += 1;
          if(this.typeArrayIndex >= this.typeArray.length)
            this.typeArrayIndex = 0;
          setTimeout(this.typeText, this.typingSpeed + 1000);
        }
      }
    },
    created() {
      setTimeout(this.typeText, this.newTextDelay + 200);
    }
  }
</script>

<style>

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  min-height:900px;
  background: rgb(9,5,32);
background: linear-gradient(180deg, rgba(9,5,32,1) 38%, rgba(30,30,181,1) 90%);

}
#ol {
  text-align: left;
}

#nav{
  background-color:#32527b
}

#blog{
  background-color:#c9ffdd;
  color:black
}

#contact{
  background-color:#dcfcfc;
  color:black
}

#bigBox{
  background-color:#212121;
  
  color:white;
  position: relative;
  top:100px;

}


#grad{
  background: rgb(0,212,255);
  background: linear-gradient(90deg, rgba(0,212,255,1) 23%, rgba(9,9,119,1) 93%, rgba(2,0,36,1) 100%); 
}

#flex{

  /* margin: 40px 40px 40px; */
  /* padding: 40px 40px 40px; */
  display: flex;
  flex-direction: row;
  justify-content: space-around
  
}

h1 {
    font-size: 6rem;
    font-weight: normal;
    span.typed-text {
      color: #D2B94B;
    }
    span.cursor {
      display: inline-block;  
      margin-left: 3px;
      width: 4px;
      background-color: #fff;
      animation: cursorBlink 1s infinite;
    }
    span.cursor.typing {
      animation: none;
    }
}
@keyframes cursorBlink {
    49% { background-color: #fff; }
    50% { background-color: transparent; }
    99% { background-color: transparent; }
}

</style>
