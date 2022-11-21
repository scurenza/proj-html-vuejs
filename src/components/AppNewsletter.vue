<script>
export default {
    name: "AppNewsletter",
    data() {
        return {
            title: "Suscribe our newsletter",
            text: "There are many variations of passages of Lorem Ipsum available, but the majority have suffered alteration in some form, by injected humour, or randomised words"
        }
    }
}
</script>

<template>
    <div class="newsletter">
        <div class="newsletter-container d-flex align-items-center justify-content-between">
            <div class="text text-light d-flex flex-column justify-content-center">
               <h5>{{ title }}</h5> 
               <p>{{ text }}</p>
            </div>
            <div class="my-input d-flex flex-column justify-content-center">
                <P class="text-light">YOUR E-MAIL ADDRESS</P>
                <div>
                        <input type="text" placeholder="Enter your E-mail" class="align-middle">
                        <button class="search">
                            <a href="/subscribe">
                                <span class="text-light">SUBSCRIBE</span>
                            </a>
                        </button>
                    </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

.newsletter {
    width: 100%;
    height: 15vh;
    margin: 3rem 0;

    background-color: $primary-color;

    &-container{
        width: 70%;
        height: 100%;
        margin: 0 auto;

        .text,
        .my-input{
            width: 45%;
            height: 100%;
        }

        .text h5{
            margin-bottom: .5rem;
        }

        .text p{
            margin: 0;
            font-size: .9rem;
        }

        .my-input {
            input {
                width: 300px;
                height: 45px;
                border: none;
                &::placeholder {
                    font-size: .8rem;
                    padding-left: .5rem;
                }

            }
            button {
                height: 45px;
                border: none;
                // min-width: 95px;
                padding: .4rem 1.2rem;
                font-size: .9rem;

                background-color: $button-color;
            }
            p{
                font-size: .9rem;
            }
        }
    }
}
</style>