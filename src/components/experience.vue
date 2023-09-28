<script setup>
</script>

<template>
    <div class="exps  position-absolute bottom-0 start-50 translate-middle">
        <div id="carouselExampleControls" class="carousel slide" data-bs-ride="carousel">
            <div class="carousel-inner">
                <div class="carousel-item active ">
                    <div class="row">
                        <img src="../assets/exper/352790302_733478115240113_4121577584437960897_n.jpg" class="col"
                            alt="...">
                        <img src="../assets/exper/353648497_735467738374484_7503158865876528130_n.jpg" class="col"
                            alt="...">
                        <img src="../assets/exper/353739676_735471405040784_7095168962064115350_n.jpg" class="col"
                            alt="...">
                    </div>
                </div>
                <div class="carousel-item gap-2">
                    <div class="row">
                        <img src="../assets/exper/353998745_735470151707576_6691005206612090600_n.jpg" class="col"
                            alt="...">
                        <img src="../assets/exper/354432386_737267371527854_895841310737664475_n.jpg" class="col" alt="...">
                        <img src="../assets/exper/363784513_760518295869428_4021621427293230659_n.jpg" class="col"
                            alt="...">
                    </div>
                </div>
            </div>
            <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleControls"
                data-bs-slide="prev">
                <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                <span class="visually-hidden">Previous</span>
            </button>
            <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleControls"
                data-bs-slide="next">
                <span class="carousel-control-next-icon" aria-hidden="true"></span>
                <span class="visually-hidden">Next</span>
            </button>
        </div>
    </div>
</template>
<style scoped>
.exps {
    width: 280px;
}

.exps img {
    width: 80px;
}

@media (min-width: 568px) {
    .exps {
        width: 100vh;
    }
    
    .exps img {
        width: 100px;
    }
}</style>