<script setup>
import certificate from './certificate.vue'
import exp from './experience.vue'

import { ref, onBeforeUnmount, onMounted, computed } from "vue";

let fade_hello = ref();
let isActive = computed(() => fade_hello.value === 0);

function logScroll() {
  const scrollY = window.scrollY;
  fade_hello.value = scrollY;

  // Reset fade_hello.value to 0 when scrolling below 200px
  if (scrollY < 500) {
    fade_hello.value = 0;
  }
}

onMounted(() => {
  window.addEventListener("scroll", logScroll);
});

onBeforeUnmount(() => {
  window.removeEventListener("scroll", logScroll);
});

</script>
<template>
    <div class="ptf d-flex">
        <div
          class="box pe-2"
          :class="{ fadeInUp: isActive }"
          :style="{ animationDelay: isActive ? '1s' : '0s' }"
        >
          Hello
        </div>
        <br />
        <div :class="{ fadeInUp: isActive }" :style="{ animationDelay: isActive ? '2s' : '0s' }">
          I'm Ohm
        </div>
      </div>
    <div class="pf text-center position-relative">
        <div class="title pt-2">
            Sirichai Kasemsuk
        </div>
        <div class="fac">
            computer science
        </div>
        <div class="pic position-absolute top-50 start-50 translate-middle">
            <img src="../assets/profile/Intersect.png" alt="">
        </div>
    </div>
    <div class="edu">
        <div class="title">
            Education
        </div>
        <div class="d-flex justify-content-center">
            <div class="timeline position-relative">
                <div class="main-line position-absolute top-50 start-50 translate-middle"></div>
                <div class="orage">
                    <div class="main-ball"></div>
                    <div class="line-ball"></div>
                    <div class="sub-ball"></div>
                </div>
                <div class="yellow">
                    <div class="main-ball"></div>
                    <div class="line-ball"></div>
                    <div class="sub-ball"></div>
                </div>
                <div class="high-school">
                    <div class="years">2013 - 2020</div>
                    <div class="place-gpa">Watcharawittaya School<br />GPA : 3.13</div>
                </div>
                <div class="university">
                    <div class="years">2020 - 2023</div>
                    <div class="place-gpa">Maejo University<br />GPA : 3.36</div>
                </div>
            </div>
        </div>
    </div>
    <div class="exp position-relative">
        <div class="title text-center">Experience</div>
        <div class="detail text-center">
            I work in the computer science department. Maejo University and is the head of the year of the branch Has
            responsibility for organizing various activities such as Wai Khru Ceremony, camps, and sports activities within
            the branch. Orient new students and work as a TA for the university.
        </div>
        <exp />
    </div>
    <div class="certi position-relative">
        <div class="title text-center">certificate</div>
        <certificate />
    </div>
    <div class="cont position-relative" id="contact">
        <div class="title ps-3">contact</div>
        <div class="tel">
            <a>tel 095-658-5160</a>
        </div>
        <div class="box-contact">
            <a>INSTAGRAM</a><br />
            <a>DISCORD</a><br />
            <a>FACEBOOK</a><br />
            <a>SK.dinsorkot@gmail.com</a>
        </div>

    </div>
</template>

<style scoped>
.fadeInUp{animation:fadeInUp 1s ease backwards;}
@keyframes fadeInUp{
  0%{transform:translate(0px, 100px); opacity: 0;}
  100%{transform:translate(0px, 0); opacity: 1;}
}
.ptf {
    height: 90vh;
    font-size: 30px;
    font-weight: 600;
    justify-content: center;
    align-items: center;
}

.pf {
    height: 400px;
}

.pf img {
    height: 200px;
    filter: drop-shadow(0px 15px 4px 0px rgba(0, 0, 0, 0.25));
}

.title {
    font-size: 20px;
    font-weight: 500;
}

.edu {
    height: 400px;
}

.edu .title {
    padding: 40px 0 0 30px;
}

.timeline {
    width: 300px;
    height: 300px;
}

.orage {
    width: 22%;
    height: 20px;
    position: absolute;
    left: 39%;
    top: 30%;
    transform: translate(-50%, -50%);
}

.orage .main-ball {
    position: absolute;
    width: 20px;
    height: 20px;
    border-radius: 50%;
    background-color: #EC5C27;
    border: 2px solid #E6EAEE;
    filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.25));
    left: 100%;
    top: 50%;
    transform: translate(-50%, -50%);
}

.orage .line-ball {
    position: absolute;
    width: 60%;
    height: 5px;
    background-color: #EC5C27;
    left: 55%;
    top: 50%;
    transform: translate(-50%, -50%);
}

.orage .sub-ball {
    position: absolute;
    width: 12px;
    height: 12px;
    border-radius: 50%;
    background-color: #EC5C27;
    border: 0.5px solid #E6EAEE;
    left: 15%;
    top: 50%;
    transform: translate(-50%, -50%);
}

.main-line {
    border-radius: 5px;
    width: 5px;
    height: 200px;
    background-color: #333;
}

.yellow {
    width: 22%;
    height: 20px;
    position: absolute;
    left: 61%;
    top: 60%;
    transform: translate(-50%, -50%);
}

.yellow .main-ball {
    position: absolute;
    width: 20px;
    height: 20px;
    border-radius: 50%;
    background-color: #efb544;
    border: 2px solid #E6EAEE;
    filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.25));
    left: 0;
    top: 50%;
    transform: translate(-50%, -50%);
}

.yellow .line-ball {
    position: absolute;
    width: 60%;
    height: 5px;
    background-color: #efb544;
    left: 45%;
    top: 50%;
    transform: translate(-50%, -50%);
}

.yellow .sub-ball {
    position: absolute;
    width: 12px;
    height: 12px;
    border-radius: 50%;
    background-color: #efb544;
    border: 0.5px solid #E6EAEE;
    right: 0;
    top: 50%;
    transform: translate(-50%, -50%);
}

.high-school {
    position: absolute;
    left: 25%;
    top: 42%;
    transform: translate(-50%, -50%);
    text-align: end;
}

.high-school .years {
    font-size: 10px;
    font-weight: 500;
}

.high-school .place-gpa {
    padding-top: 2px;
    font-size: 12px;
    font-weight: 500;
}

.university {
    position: absolute;
    left: 69%;
    top: 72%;
    transform: translate(-50%, -50%);
    text-align: start
}

.university .years {
    font-size: 10px;
    font-weight: 500;
}

.university .place-gpa {
    padding-top: 2px;
    font-size: 12px;
    font-weight: 500;
}


.exp {
    height: 250px;
}

.exp .detail {
    padding: 5% 10% 0 10%;
    font-size: 10px;
}


.certi {
    height: 400px;
}

.cont {
    height: 100px;
}

.cont .tel {
    position: absolute;
    bottom: 13%;
    left: 5%;
    font-size: 10px;
    font-weight: 500;
}

.cont .box-contact {
    position: absolute;
    text-align: end;
    bottom: 13%;
    right: 5%;
    font-size: 10px;
    font-weight: 500;
}

@media (min-width: 540px) {
    .ptf {
        margin: 0 0 0 15%;
        font-size: 50px;
        font-weight: 600;
        justify-content: start;
        align-items: start;
    }

    .ptf div {
        padding: 20% 0 0 0;
    }

    .pf {
        height: 100vh;
    }

    .pf img {
        height: 60vh;
        filter: drop-shadow(rgba(0, 0, 0, 0.25) 1rem 1rem 10px);
    }

    .title {
        font-size: 40px;
        font-weight: 500;
    }

    .fac {
        font-size: 30px;
        font-weight: 400;
    }

    .edu {
        height: 100vh;
    }

    .timeline {
        width: 500px;
        height: 400px;
    }

    .orage {
        width: 20px;
        height: 100px;
        left: 25%;
        top: 37%;
    }

    .orage .main-ball {
        width: 20px;
        height: 20px;
        left: 50%;
        top: 100%;
    }

    .orage .line-ball {
        width: 5px;
        height: 60px;
        left: 50%;
        top: 58%;
    }

    .orage .sub-ball {
        left: 50%;
        top: 20%;
    }

    .main-line {
        border-radius: 5px;
        width: 500px;
        height: 5px;
        background-color: #333;
    }

    .yellow {
        width: 20px;
        height: 100px;
        left: 55%;
        top: 62%;
    }

    .yellow .main-ball {
        left: 50%;
        top: 0;
    }

    .yellow .line-ball {
        width: 5px;
        height: 60px;
        left: 50%;
        top: 42%;
    }

    .yellow .sub-ball {
        left: 50%;
        top: 80%;
    }

    .high-school {
        left: 47%;
        top: 38%;
        text-align: start;
    }

    .high-school .years {
        font-size: 16px;
        font-weight: 500;
    }

    .high-school .place-gpa {
        padding-top: 1px;
        font-size: 18px;
        font-weight: 500;
    }

    .university {
        left: 71%;
        top: 62%;
        text-align: start
    }

    .university .years {
        font-size: 16px;
        font-weight: 500;
    }

    .university .place-gpa {
        padding-top: 1px;
        font-size: 18px;
        font-weight: 500;
    }

    .exp {
        height: 80vh;
    }

    .exp .detail {
        font-size: 18px;
    }

    .certi {
        height: 100vh;
    }

    .cont {
        height: 250px;
    }

    .cont .tel {
        font-size: 18px;
        font-weight: 500;
    }

    .cont .box-contact {
        font-size: 18px;
        font-weight: 500;
    }
}
</style> 
