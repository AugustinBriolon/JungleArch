<template>
    <div class="footer">
        <div class="footer flex justify-between items-center w-full mt-0" href="footer">
            <div class="footer_date">
                <nuxt-img  src="/images/logos/logo-jungleArch.png" class="ml-24 mb-5"></nuxt-img>

                <div class="ml-24">
                    <p class="text-white text-sm">Lundi 07:00 - 23:00</p>
                    <p class="text-white text-sm">Mardi 07:00 - 23:00</p>
                    <p class="text-white text-sm">Mercredi 07:00 - 00:00</p>
                    <p class="text-white text-sm">Jeudi 07:00 - 00:00</p>
                    <p class="text-white text-sm">Vendredi 07:00 - 00:00</p>
                </div>

                <div class="footer_contact mt-10 flex items-center ml-24">
                        <nuxt-img  src="/images/logos/facebook-f.png"  class="h-3 w-auto mr-2"></nuxt-img>
                        <nuxt-img  src="/images/logos/trip-f.png" class="h-3 w-auto mr-2"></nuxt-img>
                        <nuxt-img  src="/images/logos/instagram.png" class="h-3 w-auto mr-2"></nuxt-img>
                </div>

                <div class="footer_contact mt-4 flex  items-center ml-24">
                    <nuxt-img  src="/images/logos/location-dot.png" class="h-3 w-auto mr-2"></nuxt-img>
                    <p class="text-white text-sm">589 Terrasses de l’Arche, 92000 Nanterre, La Defense France</p>
                </div>

                <div class="footer_contact mt-4 flex  items-center ml-24">
                    <nuxt-img  src="/images/logos/envelope.png" class="h-3 w-auto mr-2"></nuxt-img>
                    <p class="text-white text-sm">junglearch-arena@hotmail.com</p>
                </div>

                <div class="footer_contact mt-4 flex  items-center ml-24">
                    <nuxt-img  src="/images/logos/phone.png" class="h-3 w-auto mr-2"></nuxt-img>
                    <p class="text-white text-sm">+33 1 47 25 45 97</p>
                </div>

            </div>

            <div class="map m-11">
                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2623.0169671527765!2d2.2236280507417265!3d48.89601380591008!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47e664f64077e4dd%3A0x820b46994b550007!2sJungle%20Arch!5e0!3m2!1sfr!2sfr!4v1663751356118!5m2!1sfr!2sfr" width="480" height="440" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
            </div>
        </div>
        <p class="credit text-center pb-4 text-white text-sm">© Jungle Arch  | Touts droits réservés </p>
    </div>

</template>

<script>

    

</script>

<style>

    .footer{
        background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('/images/backgrounds/hero.png');
        background-size: cover;
        background-position: center;
        background-repeat: no-repeat;
    }

</style>