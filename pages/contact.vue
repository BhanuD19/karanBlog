<template>
    <section class="contact-us">
        <div class="contact-us-heading">
            <h1>
                Stay in touch
            </h1>
        </div>
        <div class="contact-us-text">
            <span>
                <h3>
                    Stay updated with the community. Subscribe to my newsletters.
                </h3>
                <p>
                    Enter you email and subscribe to my weekly newsletter that throws light on my recent cases, some anecdotes to light up your career or just stay updated and connected with our community.
                </p>
            </span>
        </div>
        <div class="contact-us-form-element">
        <input type="text" placeholder="Enter your email!">
        <span><i class="fas fa-chevron-right"></i></span>
      </div>
    </section>
</template>

<style lang="scss" scoped>
.contact-us {
    &-heading{

    }

    &-text {

    }

    &-form-element {
        background: #808080;
        display: inline-block;
        width: 50%;

        input {
            padding: 0.5rem 0.7rem;
            border: none;
            background: transparent;
            font-family: Livvic;
            font-size: 1rem;
        }

        span {
            background: skyblue;
            padding: 0.5rem 0.7rem;
            cursor: pointer;
        }
    }

}
</style>