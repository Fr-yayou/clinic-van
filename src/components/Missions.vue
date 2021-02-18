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
            <div class="sub-mission-text">
                <p>A specialized team of experienced physical and mental health practitioners will guide</p>
                <p>patients’ recovery using evidence-based treatment plans. Our goal is to increase</p>
                <p>access to quality healthcare and ultimately improve the community’s physical health,</p>
                <p>mental health, sports performance and quality of life.</p>
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

/* Phone */

.mission-container{
    position: relative;
    background-color: #001b36;
}

.mission-content{
    display: flex;
    flex-direction: column;
    align-items: center;
    padding-top: 50px;
    margin-left: 15px;
    margin-right: 15px;
}
.mission-title h1{
    color:#001b36;
    background-color: white;
    font-size: 25px;
}

.circle{
        background-color: white;
        height: 40px;
        width: 40px;
        border-radius: 50%;
        position: absolute;
        top: 0%;
        left: 50%;
        transform: translate(-50%, -50%);
}
.mission-text {
    padding-top: 25px;
}

.mission-text p {
    color: white;
    font-size: 20px;
    text-align: center;
}

.sub-mission-text{
    padding-bottom: 70px;
    padding-top: 40px;
    font-size: 15px;
    color: white;
    opacity: 0.7;
    text-align: center;

}

/* Ipad */

@media screen and (min-width:768px){
    .mission-container{
        padding-top: 50px;
    }
    .mission-text p{
        color:#FAF2E8;
        font-size: 20px;
    }
    
    .circle{
        height: 60px;
        width: 60px;
    }

    .mission-content{
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        margin-left: 45%;
        padding-top: 60px;
    }
    .mission-text p {
        color: white;
        text-align: unset;
    }

    .sub-mission-text{
        padding-top: 30px;
        text-align: unset;
    }
}

/* Desktop */
@media screen and (min-width:1339px){
    .mission-title h1{
    font-size: 35px;
    }
    
    .mission-text p {
        font-size:25px
    }

    .sub-mission-text{
        font-size: 20px;
        padding-bottom: 100px;
    }
}

</style>