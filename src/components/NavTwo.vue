<template>
  <div class="container-nav">
      <img v-bind:src="logo" alt="logo"/>
        <div v-if="!isOpen" v-on:click="toogleHamburger" class="hamburger">
            <div class="line"></div>
            <div class="line"></div>
            <div class="line"></div>
        </div>
        <div v-else v-bind:class="{close:isOpen}" v-on:click="toogleHamburger"></div>
        <ul class="nav-links" v-bind:class="{linksOpen:isOpen}">
            <li>Health Services</li>
            <li>Our Team</li>
            <li>Blog</li>
            <button>BOOK NOW</button>
        </ul>
  </div>
</template>

<script>
import Logo from "../assets/logo.png"
export default {
    name:"NavTwo",

    data(){
        return{
            isOpen:false ,
            logo:Logo
        }
    },
    methods:{
        toogleHamburger(){
            this.isOpen = !this.isOpen

            console.log(this.isOpen)
        }
    }
}
</script>

<style scoped>

/* Phone */
.container-nav{
    background-color: #001b36;
    height: 100px;
    width: 100%;
    display: flex;
    align-items: center;
    position: relative;
    z-index: 1;
}
.container-nav img{
    margin-left: 20px;
    height: 70px;
}

.line{
    width: 40px;
    height: 4px;
    background-color: white;
    margin: 7px;
}

.hamburger{
    position: absolute;
    cursor: pointer;
    margin-right: 15px;
    margin-top: 10px;
    right: 0px;
}
.nav-links{
    width: 100%;
    position: fixed;
    top: 0;
    height: 100vh;
    background-color:#001b36 ;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-around;
    clip-path: circle(50px at 90% -10%);
    -webkit-clip-path: circle(50px at 90% -10%);
    transition: all 1s ease-out;
        
}
.nav-links li{
    color:white;
    list-style: none; 
}
.nav-links button{
    background-color: #001b36;
    color:white;
    border: 1px solid white;
    padding:10px
}
.linksOpen{
        clip-path: circle(1300px at 90% -10%);
        -webkit-clip-path: circle(1300px at 90% -10%); 
}

#logo{
    display: none;
        
}
.close{
    cursor:pointer;
    display: unset;
    z-index: 1;
    color: white;
    margin-top: 25px;
    font-size: 30px;
}
.close:hover {
    opacity: 1;
    position: fixed;
}
.close:before, .close:after {
    position: absolute;
    left: 20px;
    content: ' ';
    height: 33px;
    width: 2px;
    margin-left: 15px;
    background-color:white;
}
.close:before {
    transform: rotate(45deg);
}
.close:after {
    transform: rotate(-45deg);
}




/* Ipad */
@media only screen and (min-width:768px){

    .hamburger{
        display: none;
    }
    .container-nav{
        height: 80px; 
        position: fixed;
        justify-content: space-between;
    }
    .container-nav img{
        height: 70px;
    }

    .nav-links{
        margin-right: 20px;
        display: flex;
        width: 60%;
        justify-content: space-around;
        list-style: none;
        color:white;
        position: unset;
        height: unset;
        transition: unset;
        -webkit-clip-path:unset;
        clip-path:unset;
        align-items: unset;
        flex-direction: unset;
    }
    .nav-links li {
        display: flex;
        align-items: center;
    }
    .nav-links button{
        background-color: #001b36;
        color:white;
        border: 1px solid white;
        padding:10px
    }
    .nav-links li button:focus{
        outline: none;
        background-color: white ;
        color:#001b36;
        border: 1px solid #001b36 ;
    }
    .nav-links li:nth-child(1) {
        border-right: 3px solid white;
        display: flex;
        padding-right: 25px;
        align-items: center;
    }
    .nav-links li:nth-child(2) {
        border-right: 3px solid white;
        display: flex;
        padding-right: 25px;
        align-items: center;
    }

}


/* Desktop */

@media only screen and (min-width:1339px){
    
    .nav-links{
        width: 40%;
    }

}


</style>