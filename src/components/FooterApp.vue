<script>
import Feature from "./CardApp.vue"
import DcComicsLinksApp from "./links/DcComicsLinksApp.vue"
import ShopLinksApp from "./links/ShopLinksApp.vue"
import DcLinksApp from "./links/DcLinksApp.vue"
import SitesLinksApp from "./links/SitesLinksApp.vue"
import ButtonApp from "../components/ButtonApp.vue"
import FollowApp from "../components/FollowApp.vue"
import { store } from "../data/store"

export default {
    data() {
        return {
            store,

            cards: [
                {
                    text: 'DIGITAL COMICS',
                    img: 'buy-comics-digital-comics.png'
                },
                {
                    text: 'DC MERCHANDISE',
                    img: 'buy-comics-merchandise.png'
                },
                {
                    text: 'SUBSCRIPTION',
                    img: 'buy-comics-subscription.png'
                },
                {
                    text: 'COMIC SHOP LOCATOR',
                    img: 'buy-comics-shop-locator.png'
                },
                {
                    text: 'DC POWER VISA',
                    img: 'buy-comics-power-visa.svg'
                },
            ],

            social: [
                {
                    img: 'footer-facebook.png'
                },
                {
                    img: 'footer-periscope.png'
                },
                {
                    img: 'footer-pinterest.png'
                },
                {
                    img: 'footer-twitter.png'
                },
                {
                    img: 'footer-youtube'
                },
            ]
        }
    },

    components: {
        Feature,
        DcComicsLinksApp,
        ShopLinksApp,
        DcLinksApp,
        SitesLinksApp,
        ButtonApp,
        FollowApp
    }
}
</script>

<template>
    <footer>
        <section class="feature">
            <div class="container">
                <div class="row justify-content-between">
                    <div v-for="card in cards" class="col-auto">
                        <Feature :figure="card.img" :text="card.text" />
                    </div>
                </div>
            </div>
        </section>

        <section class="sectionlinks">
            <div class="container">
                <div class="row flex-column flex-wrap">
                    <div class="col-auto">
                        <ul>
                            <h5>
                                DC COMICS
                            </h5>
                            <DcComicsLinksApp v-for="link in store.DcComicsLinks" :name="link.name" />
                        </ul>
                    </div>
                    <div class="col-auto">
                        <ul>
                            <h5>
                                SHOP
                            </h5>
                            <ShopLinksApp v-for="link in store.ShopLinks" :name="link.name" />
                        </ul>
                    </div>
                    <div class="col-auto">
                        <ul>
                            <h5>
                                DC
                            </h5>
                            <DcLinksApp v-for="link in store.DcLinks" :name="link.name" />
                        </ul>
                    </div>
                    <div class="col-auto">
                        <ul>
                            <h5>
                                SITES
                            </h5>
                            <SitesLinksApp v-for="link in store.SitesLinks" :name="link.name" />
                        </ul>
                    </div>
                </div>
            </div>
        </section>

        <section class="socialsection py-4">
            <div class="container">
                <div class="row justify-content-between align-items-center">
                    <div class="col-auto">
                        <ButtonApp />
                    </div>
                    <div class="col-auto">
                        <FollowApp :socialimg="social" />
                    </div>
                </div>
            </div>
        </section>
    </footer>
</template>

<style lang="scss" scoped>
footer {}

.feature {
    background-color: #0C7CEC;
    color: white;
}

h5 {
    color: white;
}

.sectionlinks {
    background-image: url(../assets/img/footer-bg.jpg);

    div {
        max-height: 400px;
    }
}

.socialsection {
    background-color: #222222;
}
</style>