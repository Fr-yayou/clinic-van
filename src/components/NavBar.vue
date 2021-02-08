<template>
  <div class="container-navBar">
        <h5 id="logo">Logo</h5>
        <div v-if="!isOpen" v-on:click="toogleHamburger" class="hamburger">
            <div class="line"></div>
            <div class="line"></div>
            <div class="line"></div>
        </div>
        <div v-else v-bind:class="{close:isOpen}" v-on:click="toogleHamburger"></div>
        <ul class="nav-links" v-bind:class="{linksOpen:isOpen}">
            <li>Home</li>
            <li>Example</li>
            <li>Example</li>
            <li>Example</li>
            <li><button>BOOK NOW</button></li>
        </ul>
  </div>
</template>

<script>
export default {
    name:"NavBar",

    data(){
        return{
            isOpen:false 
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
    background-color: black;
    display: flex;
    justify-content: space-between;
    z-index: 1;
}

.nav-links li button{
    background-color: black;
    color:#34E1E7;
    border: 1px solid #34E1E7;
    padding:10px
}
.nav-links li button:focus{
    outline: none;
    background-color: #34E1E7 ;
    color:black;
    border: 1px solid #34E1E7 ;
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
        margin-left: 15px;
    }


    .nav-links{
        position:fixed;
        background-color:black;
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
    background-color:#34E1E7; ;
}
    .close:before {
    transform: rotate(45deg);
    }
    .close:after {
    transform: rotate(-45deg);
    }

    

}

</style>