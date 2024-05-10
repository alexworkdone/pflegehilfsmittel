<template>
  <footer class="footer">
    <div class="wrapper">
      <div class="footer-content">
        <div class="logo-description">
          <img
            class="logo"
            :src="require(`@images/logo-white.png`)"
            alt="logo white"
          />

          <p class="footer-description">
            Spezialisten in der Versorgung von Pflegehilfsmittelhändlern. Durch
            Digitalisierung optimieren wir Prozesse und bieten erstklassigen
            Service.
          </p>
        </div>

        <div class="footer-contact">
          <div class="text-1-b m-b-16">Kontakt</div>
          <p>Docdorado GmbH</p>
          <p>Im Schäwe 23, 14547 Beelitz</p>
          <p>03379 / 316 44 0</p>
          <p>verkauf@docdorado.de</p>
        </div>

        <div class="footer-links">
          <div class="text-1-b m-b-16">Links</div>
          <p><a href="#">Impressum</a></p>
          <p><a href="#">AGB</a></p>
          <p><a href="#">Datenschutz</a></p>
        </div>

        <div class="footer-social">
          <a href="#" class="icon-link">
            <icon-in />
          </a>
          <a href="#" class="icon-link">
            <icon-facebook />
          </a>
          <a href="#" class="icon-link">
            <icon-youtube />
          </a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import IconIn from '@images/components/icon-in.vue'
import IconFacebook from '@images/components/icon-facebook.vue'
import IconYoutube from '@images/components/icon-youtube.vue'

export default {
  name: 'PBFooter',

  components: {
    IconIn,
    IconFacebook,
    IconYoutube,
  },
}
</script>
