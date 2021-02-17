<template>
    <div class="mission-container">
        <div class="circle"></div>
        <div class="mission-content">
            <div class="mission-title">
                <h1>Our Mission</h1>
            </div>
            <div class="mission-text">
                <p> Horseshoe Bay Health & Performance will provide high quality,</p>
                <p>patient-centred healthcare to the beautiful community of<p>
                <p>Horseshoe Bay and surrounding areas.</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name:"Mission"
}
</script>

<style scoped>


@media screen and (min-width:768px){
    .mission-container{
        padding-top: 50px;
        background-color: #001b36;
        position: relative;

    }

    .mission-title h1{
        color:#001b36;
        background-color: white;
    }
    .mission-text p{
        color:#FAF2E8;
        font-size: 20px;
    }
    
    .circle{
        background-color: white;
        height: 60px;
        width: 60px;
        border-radius: 50%;
        position: absolute;
        top: 0%;
        left: 50%;
        transform: translate(-50%, -50%);
    }

    .mission-content{
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        margin-left: 45%;
        padding-top: 60px;
    }
}

</style>