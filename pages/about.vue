<template>
    <main>
        <section class="fullpage">
           
            <div class="fullpage-text" data-aos="zoom-in" data-aos-delay="200">
                <span>
                    <h1> WELCOME TO MY BLOG </h1>
                    <h3> This is my place to <br/> share my experiences with <br/>my audience and connect <br/> better with my clients </h3>
                </span>
            </div>
        </section>

        <section class="about-us" data-aos="fade-up" data-aos-delay="200">
            <div class="about-us-text">
                <h1>
                    Karan Chandna Associates
                </h1>
                <span>
                    <p>Karan Chandna, eccenteric and accomplished Chartered Accountant and lawyer. </p>
                    <p>Standing infront of an 8+ years career which includes advising clients in diverse areas like- Comapanies act matters, business tax and regulatory matters which encompasses corporate tax, income tax, Goods and services tax as well as tax due to dilligence and audit and assurance services.</p>
                    <p>Gaining a vast clientelle and assisting and helping them with thier financial needs.
                      &nbsp;Involved in preparation of client specific GST presentation.</p>
                    <p>With a vast clientelle spanning to more than 100 favourable orders from various authorities with regards to Service tax audit, service tax and gst refund claims, income tax assessments, customs, directorate of revenue intelligence, anti evasion department, special valuation branch and many other top tier jobs pertaining to his field.</p>
                    <p>Karan's job profile is laden with many accolades and different kinds of jobs. His most notable fields of working in all these years has been of auditing, direct tax and indirect taxation, income tax, companies act, service tax, Value added tax, central excise, customs & goods and services tax.</p>
                    <p>Alongside helping clients individually Karan is also associated with a tier one Chartered Accountant firm, based at New Delhi as a consultant, and is rendering professional services.</p>
                </span>
            </div>
            <div class="about-us-image-holder">
            </div>
        </section>

        <section class="testimonials" data-aos="fade-up" data-aos-delay="100">
            <div class="testimonials-carousel">
                <testimonial-carousel></testimonial-carousel>
            </div>
        </section>
    </main>
</template>

<script>
import TestimonialCarousel from '~/components/TestimonialCarousel.vue'

export default {
    components: {
        TestimonialCarousel
    }
}
</script>
<style lang="scss" scoped>

section {
    margin-bottom: 5rem;
}

.fullpage {

    background-image:url(/about-us-background.jpg);
    background-size: cover;
    background-position-x: 150px;
    height: 760px;

    &-text{
        padding-right: 10rem;
        margin: 0rem auto;

        h1 {
            padding-top: 10rem;;
            padding-left: 10rem;
        }

        h3 {
            margin-top: 1rem;
            padding-left: 3rem;
            line-height: 2.5rem;
        }
    }
}

.about-us {
    display: grid;
    grid-template-columns: 2fr 1fr;
    margin-right: 1rem;
    margin-left: 1rem;
    box-shadow: 0 10px 20px rgba(0,0,0,0.19), 0 6px 6px rgba(0,0,0,0.23);
    border-radius: 0.5rem;


    &-text {
        padding: 2rem ;
    }

    &-image-holder {
        background: url('/profile-about.jpg');
        background-size: cover;
    }
}

.testimonials {
    &-carousel {
        padding-left: 10rem;
    }
}
</style>