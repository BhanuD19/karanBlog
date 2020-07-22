<template>
    <section id="about-us">
        
        <div class="d-flex align-items-center mt-2">
          <i class="fas fa-chevron-circle-left nav-carousel" id="nav-left" @click="moveCarousel(-1)" :disabled="atHeadOfList" />
          <div class="card-carousel pt-2">
            <div class="card-carousel--overflow-container">
              <div class="card-carousel-cards" :style="{ transform: 'translateX' + '(' + currentOffset + 'px' + ')'}">

                <b-card
                  class="about-us"
                  id="profile-img"
                  img-alt="Profile-image"
                  img-src="/profile-sm.jpg"
                  img-top
                  text-variant="white"
                  data-aos="fade-right" data-aos-delay="200"
                >
                  <i class="fas fa-external-link-alt external-link-icon icon" />
                  <b-card-text>
                    <h3>Welcome</h3>
                    <p>Hear my story through my blog</p>
                  </b-card-text>
                </b-card>

                <b-card
                  class="about-us"
                  img-alt="icon"
                  img-src=""
                  img-top
                  tag="article"
                  title="My Story"
                  data-aos="fade-in" data-aos-delay="200"
                >
                  <i class="fas fa-external-link-alt external-link-icon icon" />
                  <b-card-text>
                    <p>Karan Chandna, eccenteric and accomplished Chartered Accountant and lawyer. </p>
                    <p>Standing infront of an 8+ years career which includes advising clients in diverse areas like- Comapanies act matters, business tax and regulatory matters which encompasses corporate tax, income tax, Goods and services tax as well as tax due to dilligence and audit and assurance services.</p>
                  </b-card-text>
                </b-card>
                <b-card
                  class="about-us"
                  img-alt="icon"
                  img-src=""
                  img-top
                  tag="article"
                  title="Career Achievements"
                  data-aos="fade-left" data-aos-delay="200"
                >
                  <i class="fas fa-external-link-alt external-link-icon icon" />
                  <b-card-text>
                      <p>Gaining a vast clientelle and assisting and helping them with thier financial needs.
                      &nbsp;Involved in preparation of client specific GST presentation.</p>
                      <p>With a vast clientelle spanning to more than 100 favourable orders from various authorities with regards to Service tax audit, service tax and gst refund claims, income tax assessments, customs, directorate of revenue intelligence, anti evasion department, special valuation branch and many other top tier jobs pertaining to his field.</p>
                  </b-card-text>
                </b-card>
                
                <b-card
                  class="about-us"
                  img-alt="Icon"
                  img-src=""
                  img-top
                  tag="article"
                  title="Professional Journey"
                >
                  <i class="fas fa-external-link-alt external-link-icon icon" />
                  <b-card-text>
                      <p>Karan's job profile is laden with many accolades and different kinds of jobs. His most notable fields of working in all these years has been of auditing, direct tax and indirect taxation, income tax, companies act, service tax, Value added tax, central excise, customs & goods and services tax.</p>
                      <p>Alongside helping clients individually Karan is also associated with a tier one Chartered Accountant firm, based at New Delhi as a consultant, and is rendering professional services.</p>
                  </b-card-text>
                </b-card>
              </div>
            </div>
          </div>
          <i class="fas fa-chevron-circle-right nav-carousel" id="nav-right" @click="moveCarousel(1)" :disabled="atEndOfList"/>
        </div>
        
      </section>
</template>

<script>
export default {
    data() {
            return {
                currentOffset: 0,
                windowSize: 4,
                paginationFactor: 270,
                clientWidth: 1024
            }
    },

    mounted() {
        this.clientWidth = window.innerWidth
    },
    computed: {
            atEndOfList() {
              if(this.clientWidth < 770 ) {
                this.windowSize = 2
              }
              if(this.clientWidth < 520) {
                this.paginationFactor = 292
              }
                return this.currentOffset <= (this.paginationFactor * -1) * (5 - this.windowSize);
            },
            atHeadOfList() {
                return this.currentOffset === 0;
            },
    },

    methods: {
            moveCarousel(direction) {
                // Find a more elegant way to express the :style. consider using props to make it truly generic
                if (direction === 1 && !this.atEndOfList) {
                    this.currentOffset -= this.paginationFactor;
                } else if (direction === -1 && !this.atHeadOfList) {
                    this.currentOffset += this.paginationFactor;
                }
            },
    }
}
</script>
<style lang= "scss" scoped>
@import "~assets/scss/functions";

  $sky: linear-gradient(120deg, #a1c4fd 0%, #c2e9fb 100%); 
 .card-carousel--overflow-container {
    overflow: hidden;
  }

  .card-carousel {
    display: flex;
    justify-content: center;
  }


  .card-carousel-cards {
    display: flex;
    transition: transform 150ms ease-out;
    transform: translatex(0px);

    #profile-img {
      width: rem(640);

      @media only screen and (max-width: 520px) {
        width: rem(300);
        height: rem(420);
      }
    }

    .card {
      width: rem(300);
      height: rem(420);
      z-index: 3;
      box-shadow: 0 10px 20px rgba(0,0,0,0.19), 0 6px 6px rgba(0,0,0,0.23);
      margin: 1rem;
      border-radius: 0.5rem;

      a {
        background-color: $sky;
        border: none;
      }

      .card-img-top {
        position: relative;
        top:-32px;
        align-self: center;
        width: 270px;
        height: 270px;
        border-radius: 10rem;
        padding: 1rem;
      }

      .card-body {

        h4 {
          font-family: "Open Sans";
          font-weight: 600;
        }

        p {
          font-size: 0.7rem;
          font-weight: 300;
        }

        a {
          position: absolute;
          bottom: 12px;
          margin:0 0 0.3rem 4rem;
        }

        .external-link-icon {
          position: absolute;
          right: 10px;
          top: 10px;
          visibility: hidden;
          transition: visibility 200ms, opacity 275ms ease-in;
        }

        &:hover {
          h4 {
            color: #327ACB;
            transition: color 275ms;
          }
          .external-link-icon{
            opacity: 0.5;
            visibility: visible;

          }
        }
      }
    }

  }
.nav-carousel {
    display: inline-block;
    font-size: 3rem;
    position:absolute;
    background-color:#327ACB;
    color:white;
    box-shadow: 0 2px 16px 0 rgba(32,33,36,0.07), 0 26px 38px 0 rgba(32,33,36,0.09);
    border-radius:2rem;
    z-index: 1000;
    visibility: visible;
    opacity: 1;
    cursor: pointer;
    transition: visibility 0s, opacity 275ms ease-in;
    &[disabled] {
      opacity: 0;
      visibility: hidden;
    }
  }


  #nav-left {
    left: 1px;
    margin-left: 3rem;

    @media only screen and (max-width: 520px) {
      margin-left: 0%;
    }
  }

  #nav-right {
    right: 1px;
    margin-right: 3rem;

    
    @media only screen and (max-width: 520px) {
      margin-right: 0%;
    }
  }

  .fade-in-enter {
    opacity: 0.1;
  }

  .fade-in-enter-to {
    opacity: 1;
  }

  .fade-in-enter-active {
    transition: opacity 200ms ease-out;
  }

  .fade-in-left-enter {
    opacity: 0;
    transform: translateX(-20px);
  }

  .fade-in-left-enter-to {
    opacity: 1;
    transform: translateX(0);
  }
  .fade-in-left-enter-active {
    transition: opacity, transform 200ms ease-out;
  }

  
  .fade-in-left-enter {
    opacity: 0;
    transform: translateX(20px);
  }

  .fade-in-left-enter-to {
    opacity: 1;
    transform: translateX(0);
  }
  .fade-in-left-enter-active {
    transition: opacity, transform 200ms ease-out;
  }

  
  .fade-in-down-enter {
    opacity: 0;
    transform: translateY(-20px);
  }

  .fade-in-down-enter-to {
    opacity: 1;
    transform: translateY(0);
  }
  .fade-in-down-enter-active {
    transition: opacity, transform 200ms ease-out;
  }

</style>