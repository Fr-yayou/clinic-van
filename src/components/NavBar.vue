<template>
  <div class="container-navBar">
      <img v-bind:src="Logo" alt="logo"/>
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
            <li><button>BOOK NOW</button></li>
        </ul>
  </div>
</template>

<script>
import Logo from "../assets/logo.png"
export default {
    name:"NavBar",

    data(){
        return{
            isOpen:false ,
            Logo:Logo
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

<style>
.container-navBar{
    height: 80px;
    background-color:#001b36;
    display: flex;
    justify-content: space-between;
    z-index: 1;
}

.container-navBar img {
    margin-left: 15px;
}

.nav-links li {
    display: flex;
    align-content: center;
}

.nav-links li:hover{
    color:#34E1E7;
}

.nav-links li button{
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

.nav-links{
    display: flex;
    justify-content: space-between;
    width: 50%;
    align-items: center;
    color:white;
    list-style: none;
    padding-right: 30px;
}
#logo{
    color: white;
    align-self: center;
    padding-left: 30px;
}
.nav-links li:nth-child(1) {
    border-right: 3px solid white;
    width: 130px;
    height: 30px;
    display: flex;
    align-items: center;
}
    
.nav-links li:nth-child(2) {
    border-right: 3px solid white;
    width: 130px;
    height: 30px;
    display: flex;
    align-items: center;
}

@media screen and (max-width:768px){

    .line{
        width: 30px;
        height: 3px;
        background-color: white;
        margin: 5px;
    }

    .container-navBar{
        position: relative;
    }

    .hamburger{
        position: absolute;
        cursor: pointer;
        margin-top: 25px;
        margin-right: 15px;
        right: 0px;
    }


    .nav-links{
        position:fixed;
        background-color:#001b36 ;
        height: 100vh;
        width: 100%;
        flex-direction: column;
        justify-content: space-around;
        clip-path: circle(50px at 90% -10%);
        -webkit-clip-path: circle(50px at 90% -10%);
        transition: all 1s ease-out;
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
    left: 15px;
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
    
    .nav-links li:nth-child(1) {
        border-right:none;
        width: unset;
        height: unset;
        display: unset;
    }
    
    .nav-links li:nth-child(2) {
        border-right: none;
        width: unset;
        height: unset;
        display: unset;
    }

    

}

</style>