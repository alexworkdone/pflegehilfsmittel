<template>
  <div class="home-page">
    <section class="section-first">
      <div class="wrapper">
        <div class="row">
          <div class="col-6 col-lg-12 m-b-20">
            <div class="main-info">
              <h1>
                <span class="text-primary">Fulfillment</span> - Software, die
                Ihren täglichen Pflegehilfsmittel-Handel
                <span class="ellipse">unterstützt</span>
              </h1>

              <p class="sub-title">
                Von der Genehmigung, über die Logistik, bis zur Abrechnung -
                unsere Software unterstützt Sie in allen Bereichen Ihres
                Unternehmens. Effizienz und Produktivität sind unsere
                Prioritäten.
              </p>

              <div class="btns">
                <button class="btn btn-big btn-primary">Jetzt entdecken</button>
                <button class="btn btn-big btn-primary-light">
                  Demo - Boxenkonfigurator
                </button>
              </div>
            </div>
          </div>

          <div class="col-6 col-lg-12 m-b-20 relative">
            <div class="preview-video">
              <div class="preview-video-in">
                <img
                  class="img-main"
                  :src="require(`@images/img-main.png`)"
                  alt="Video ansehen preview"
                />

                <button class="btn btn-medium btn-primary" @click="showVideo">
                  <icon-play class="m-r-8" />
                  Video ansehen
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>

      <icon-plus class="bg-icon-top-left" />
      <icon-plus class="bg-icon-bottom-left" />
      <icon-plus class="bg-icon-top-right" />
      <icon-plus class="bg-icon-bottom-right" />
    </section>

    <section class="section-useful-articles">
      <div class="wrapper">
        <div class="box-articles">
          <h2 class="box-articles-title">Nützliche Artikel</h2>

          <div class="row">
            <div
              v-for="item in articles"
              :key="item.id"
              class="col-4 col-lg-6 col-md-12 m-b-20"
            >
              <article class="card-article">
                <div
                  class="card-article-image range-16x9"
                  :style="`background: url('${item.url}') no-repeat center; background-size: cover;`"
                />
                <h4 class="m-b-0">{{ item.title }}</h4>
                <p class="card-article-desc">{{ item.desc }}</p>
              </article>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="section-features-care">
      <div class="wrapper">
        <h2>Pflegehilfsmittelparadies Features im Überblick</h2>

        <div class="tabs-row-scroll">
          <div class="tabs-row">
            <div
              v-for="(tab, index) in tabs"
              :key="index + 1"
              class="tab icon-state"
              :class="{
                active: activeTabIndex === index + 1,
              }"
              @click="activeTabIndex = index + 1"
            >
              <div class="m-b-12">
                <component :is="tab.icon" />
              </div>

              <div class="text-1-m">{{ tab.name }}</div>
            </div>
          </div>
        </div>

        <transition name="tab">
          <div v-if="activeTabIndex === 1" key="activeTabIndex-1" class="row">
            <div class="col-6 col-md-12 m-b-32">
              <div class="h-full flex-v__center">
                <img
                  :src="require('@images/preview-table-and-page.png')"
                  alt="preview-table-and-page"
                />
              </div>
            </div>
            <div class="col-6 col-md-12 m-b-32">
              <div
                class="h-full flex-direction__column flex-h__center flex-v__start"
              >
                <h3>Das Überwachungs- & Whitelabelingsystem</h3>

                <p class="text-2 m-t-12 m-b-12">
                  Erhalten Sie automatisierte, stündliche Status-Updates zu
                  Ihrem Auftrag, inklusive automatischer Dokumentation und
                  Lieferbelegen. Unsere System-Schnittstellen ermöglichen eine
                  automatische Pflegehilfsmittelversorgung und sorgen für
                  vollständige Transparenz.
                </p>

                <p class="text-2">
                  Genießen Sie die Flexibilität, unser System in Ihrem eigenen
                  Design zu nutzen. Die Pakete und Lieferscheine werden in einem
                  White-Label-Format bereitgestellt, wodurch der Empfänger nicht
                  erkennen kann, dass wir hinter dem Service stehen.
                </p>

                <button class="btn-medium btn-primary m-t-48">
                  Kostenlosen Demotermin buchen
                </button>
              </div>
            </div>
          </div>
        </transition>

        <transition name="tab">
          <div v-if="activeTabIndex === 2" key="activeTabIndex-2" class="row">
            <div class="col-6 col-md-12 m-b-32">
              <div
                class="h-full flex-direction__column flex-h__center flex-v__start"
              >
                <h3>Das Überwachungs- & Whitelabelingsystem</h3>

                <p class="text-2 m-t-12 m-b-12">
                  Erhalten Sie automatisierte, stündliche Status-Updates zu
                  Ihrem Auftrag, inklusive automatischer Dokumentation und
                  Lieferbelegen. Unsere System-Schnittstellen ermöglichen eine
                  automatische Pflegehilfsmittelversorgung und sorgen für
                  vollständige Transparenz.
                </p>

                <p class="text-2">
                  Genießen Sie die Flexibilität, unser System in Ihrem eigenen
                  Design zu nutzen. Die Pakete und Lieferscheine werden in einem
                  White-Label-Format bereitgestellt, wodurch der Empfänger nicht
                  erkennen kann, dass wir hinter dem Service stehen.
                </p>

                <button class="btn-medium btn-primary m-t-48">
                  Kostenlosen Demotermin buchen
                </button>
              </div>
            </div>
            <div class="col-6 col-md-12 m-b-32">
              <div class="h-full flex-v__center">
                <img
                  :src="require('@images/preview-table-and-page.png')"
                  alt="preview-table-and-page"
                />
              </div>
            </div>
          </div>
        </transition>

        <transition name="tab">
          <div v-if="activeTabIndex === 3" key="activeTabIndex-3">
            <div class="col-4 col-lg-6 col-md-12 m-b-20">
              <article class="card-article">
                <div
                  class="card-article-image range-16x9"
                  :style="`background: url('${articles[0].url}') no-repeat center; background-size: cover;`"
                />
                <h4 class="m-b-0">{{ articles[0].title }}</h4>
                <p class="card-article-desc">{{ articles[0].desc }}</p>
              </article>
            </div>
          </div>
        </transition>

        <transition name="tab">
          <div v-if="activeTabIndex === 4" key="activeTabIndex-4">
            <div class="m-t-20 m-b-20">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Odit
              aliquid nisi inventore, laudantium dicta deserunt perspiciatis
              fuga, corrupti excepturi delectus voluptatum. Tenetur accusantium
              veniam voluptatem. Molestias praesentium tempora libero magni?
              Accusantium, consequuntur cupiditate. Aspernatur, sunt qui!
              Reprehenderit, voluptas laborum cum esse quibusdam labore soluta
              optio, nemo libero, deserunt ipsa! Nostrum maiores nam excepturi
              voluptates vitae, soluta veniam nemo animi cupiditate. Explicabo
              nisi laboriosam recusandae, sunt vel magnam illum omnis laborum,
              ea quisquam culpa ex fuga? Et at, nam enim voluptates, in earum
              necessitatibus, porro aliquam non repudiandae quo praesentium
              nisi. Blanditiis neque aspernatur sunt natus, ipsam aliquid
              delectus! Fugiat facere nostrum animi nam maiores possimus harum,
              ipsum debitis velit accusantium corrupti odit a, at hic, pariatur
              provident architecto illum sint? Eos ipsum cupiditate repellendus
              id, necessitatibus laboriosam officia eius dolore repudiandae quos
              maxime. Exercitationem, fugit? Quis a hic reprehenderit, impedit
              soluta aliquid quod? Suscipit amet animi quaerat atque quidem
              accusamus. Architecto laudantium illo veniam maxime, itaque fugit
              nemo esse porro vel, cum facilis debitis, accusantium modi eius
              voluptatem corporis similique aut nihil doloremque numquam sit
              nobis nam mollitia animi? Minima.
            </div>
          </div>
        </transition>
        <transition name="tab">
          <div v-if="activeTabIndex === 5" key="activeTabIndex-5">
            <div class="m-t-40 m-b-40">
              Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quis
              modi ipsam expedita? Unde praesentium voluptas dolore laborum! Qui
              incidunt dolore similique reiciendis libero cumque repellat!
              Quasi, perferendis? Vitae, illum rerum. Hic voluptatem saepe
              eveniet harum, nobis ab fugit ea impedit quisquam sunt numquam
              consequatur labore nemo blanditiis, excepturi tempore debitis
              consequuntur, illo modi. Tempore aperiam natus iure? Aspernatur,
              libero veritatis!
            </div>
          </div>
        </transition>
      </div>
    </section>

    <section class="section-new-function">
      <div class="wrapper">
        <div class="box-new-function">
          <div class="bg-icon">
            <icon-plus class="bg-icon-plus-1" />
            <icon-plus class="bg-icon-plus-2" />
          </div>

          <div class="row">
            <div class="col-5 col-lg-12">
              <div class="h-full flex-v__end flex-h__center">
                <img :src="require('@images/robot.png')" alt="robot" />
              </div>
            </div>

            <div class="col-7 col-lg-12">
              <div class="box-new-function-info">
                <h3>Nützliche Artikel</h3>

                <p class="text-2-m">
                  KI-gestützte Echtzeit-Beratung! Chatten Sie mit unserem
                  intelligenten Assistenten, der auf modernster KI-Technologie
                  basiert, und erhalten Sie sofortige Unterstützung und
                  persönliche Hilfe, wenn Sie sie brauchen. Erleben Sie noch
                  heute die Zukunft des Kundendienstes auf unserer Website!
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="section-target-group">
      <div class="wrapper">
        <div class="target-group-title-box">
          <div class="text-2-m text-primary m-b-8">SaaS-Software</div>

          <h2>Zielgruppe</h2>

          <h5 class="m-t-8">
            Pflegehilfsmittelparadies ist eine SaaS-Lösung mit allen Tools, die
            du benötigst, um ihren Handel von Pflegehilfsmitteln zur optimieren
            und somit für deutlich mehr Zeit sorgt.
          </h5>
        </div>

        <div class="white-box m-b-32">
          <div class="row">
            <div class="col-6 col-lg-12 m-b-16">
              <div class="h-full flex-v__center flex-h__center">
                <img
                  :src="require('@images/start-up-unternehmen.svg')"
                  alt="Start-Up-Unternehmen"
                />
              </div>
            </div>

            <div class="col-6 col-lg-12 m-b-16">
              <div
                class="h-full flex-direction__column flex-h__center flex-v__start"
              >
                <h4>Start-Up-Unternehmen</h4>

                <p class="m-t-12">
                  Unsere SaaS-Lösung stellt eine besonders gute Möglichkeit dar,
                  um Arbeitsabläufe einfach zu optimieren und zu automatisieren.
                </p>

                <p class="m-t-12">
                  Mit einer kosteneffizienten Nutzung ohne Anschaffungskosten,
                  einem umfangreich gestalteten System für schnelles und
                  einfaches Skalieren sowie einem flexiblen und einfach
                  gestalteten Dashboard für eine übersichtliche Nutzung, sind
                  wir der ideale Partner für den erfolgreichen Start Ihres
                  Unternehmens.
                </p>

                <ul class="start-up-list m-t-40">
                  <li>
                    <icon-lock />
                    Hohe Sicherheitsstandards zum Schutz sensibler Daten
                  </li>
                  <li>
                    <icon-time-stopwatch />
                    Schnelle Reaktion auf sich ändernde Anforderungen und
                    Bedürfnisse
                  </li>
                  <li>
                    <icon-scan-voice />
                    Pflegehilfsmittelversorgungen einfach und ideal skalieren
                  </li>
                </ul>
              </div>
            </div>
          </div>
        </div>

        <div class="row">
          <div class="col-6 col-lg-12 m-b-32">
            <div class="white-box h-full">
              <div class="row">
                <div class="col-5 col-md-12 m-b-16">
                  <div class="h-full flex-v__center flex-h__center">
                    <img-handler-handelsvertreter />
                  </div>
                </div>
                <div class="col-7 col-md-12 m-b-16">
                  <div
                    class="h-full flex-direction__column flex-h__center flex-v__start"
                  >
                    <h4>Händler & Handelsvertreter</h4>

                    <p class="m-t-12">
                      Werde unser Handelspartner und vertreibe unsere innovative
                      SaaS-Lösung. Profitiere Sie von einem attraktiven
                      Provisionsmodell und garantierten monatlichen Einnahmen.
                    </p>
                  </div>
                </div>
              </div>

              <ul class="start-up-list m-b-16">
                <li>
                  <icon-user-circle-group />
                  Beteiligung an den monatlichen anfallenden Wartungskosten.
                </li>
                <li>
                  <icon-award-certificate />
                  Einfache Integration von bereits bestehenden Daten und
                  Systemen
                </li>
                <li>
                  <icon-hierarchy-vertical-square />
                  Ideale Verkaufsgrundlage auf Grund von permanenter
                  Weiterentwicklung
                </li>
              </ul>
            </div>
          </div>

          <div class="col-6 col-lg-12 m-b-32">
            <div class="white-box h-full">
              <div class="row">
                <div class="col-5 col-md-12 m-b-16">
                  <div class="h-full flex-v__center flex-h__center">
                    <img-großhandel />
                  </div>
                </div>
                <div class="col-7 col-md-12 m-b-16">
                  <div
                    class="h-full flex-direction__column flex-h__center flex-v__start"
                  >
                    <h4>Großhandel</h4>

                    <p class="m-t-12">
                      Effizienz-Steigerung, weniger Arbeitsbelastung und
                      Kosteneffizienz - das sind nur einige Vorteile, die unsere
                      SAAS-Lösung für Großhändler bietet. Mit unseren und
                      automatisierten Prozessen können Sie Ihre Arbeitsabläufe
                      schnell und einfach optimieren.
                    </p>
                  </div>
                </div>
              </div>

              <ul class="start-up-list m-b-16">
                <li>
                  <icon-mega-phone />
                  erhöhte Rentabilität durch ausgeklügelte Automatismen.
                </li>
                <li>
                  <icon-security-check />
                  Übersichtlicher Zugriff auf alle Daten.
                </li>
                <li>
                  <icon-finger-pass />
                  Simple Implementierung von bereits bestehenden Systemen sowie
                  individuelle Programmierung
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="section-perfect-solution">
      <div class="wrapper">
        <div class="perfect-solution-title-box">
          <h2>Perfekte Lösung für Pflegehilfsmittelhänder</h2>

          <h5 class="m-t-8">
            Mit Pflegehilfsmittelparadies auf Erfolgskurs im
            Pflegehilfsmittelhandel Business!
          </h5>

          <button class="btn-medium btn-primary m-t-32">JETZT TESTEN</button>
        </div>

        <img
          :src="require('@images/mac-book.png')"
          alt="Perfekte Lösung für Pflegehilfsmittelhänder"
        />

        <div class="text-2 text-center text-primary m-t-20 p-b-28">
          30-tägiger kostenloser und unverbindlicher Test<br />
          Keine Kündigung erforderlich
        </div>
      </div>
    </section>

    <section class="section-we-here-for-you">
      <div class="wrapper">
        <div class="we-here-for-you-title-box">
          <div class="text-2-m text-primary m-b-8">SaaS-Software</div>

          <h2>Wir sind für dich da!</h2>

          <h5 class="m-t-8">
            Du brauchst Hilfe, möchtest ganz tief in die einzelnen Tool-Bereiche
            der Software eintauchen? Sprich uns einfach an!
          </h5>
        </div>

        <div class="contact-list">
          <div class="contact-list-item">
            <icon-align-back-rectangle />
            <div class="text-3">Nutze die Chat-Funktion</div>
            <div class="text-2-m text-primary">auf unserer Website</div>
          </div>

          <div class="contact-list-item">
            <icon-support />
            <div class="text-3">Rufe uns an</div>
            <div class="text-2-m text-primary">03379 - 316 44 0</div>
          </div>

          <div class="contact-list-item">
            <icon-email />
            <div class="text-3">Kontaktiere uns per Mail</div>
            <div class="text-2-m text-primary">verkauf@docdorado.de</div>
          </div>
        </div>
      </div>
    </section>

    <section class="section-write-to-us">
      <div class="wrapper">
        <div class="row">
          <div class="col-6 col-lg-12">
            <div class="write-to-us-title-box">
              <h2>Schreiben Sie uns</h2>

              <h5 class="text-3 m-t-20">
                Haben Sie noch Fragen oder wünschen ein persönliches Angebot?
                Dann zögern Sie nicht uns zu kontaktieren und wir melden uns bei
                Ihnen. Selbstverständlich können Sie auch ein persönliches
                Beratungsgespräch mit uns vereinbaren.
              </h5>
            </div>

            <form :action="sendForm">
              <div class="row">
                <div class="col-6 col-md-12">
                  <div
                    class="form-field required"
                    :class="{ 'field-error': vorname.isError }"
                  >
                    <label>Vorname</label>
                    <input
                      v-model="vorname.value"
                      type="text"
                      :placeholder="vorname.placeholder"
                      required
                      @input="validateVorname"
                    />
                    <div class="error">{{ vorname.textError }}</div>
                  </div>
                </div>

                <div class="col-6 col-md-12">
                  <div
                    class="form-field required"
                    :class="{ 'field-error': nachname.isError }"
                  >
                    <label>Nachname</label>
                    <input
                      v-model="nachname.value"
                      type="text"
                      :placeholder="nachname.placeholder"
                      required
                      @input="validateNachname"
                    />
                    <div class="error">{{ nachname.textError }}</div>
                  </div>
                </div>

                <div class="col-12">
                  <div
                    class="form-field required"
                    :class="{ 'field-error': email.isError }"
                  >
                    <label>E-Mailadresse</label>
                    <input
                      v-model="email.value"
                      type="email"
                      :placeholder="email.placeholder"
                      required
                      @input="validateEmail"
                    />
                    <div class="error">{{ email.textError }}</div>
                  </div>
                </div>

                <div class="col-6 col-md-12">
                  <div class="form-field">
                    <label>Unternehmen</label>
                    <input
                      v-model="unternehmen.value"
                      type="text"
                      :placeholder="unternehmen.placeholder"
                    />
                  </div>
                </div>

                <div class="col-6 col-md-12">
                  <div
                    class="form-field required"
                    :class="{ 'field-error': tel.isError }"
                  >
                    <label>Telefonnummer</label>
                    <input
                      v-model="tel.value"
                      type="text"
                      :placeholder="tel.placeholder"
                      required
                      @input="validateTel"
                    />
                    <div class="error">{{ tel.textError }}</div>
                  </div>
                </div>

                <div class="col-12">
                  <div
                    class="form-field flex__1 flex-direction__column"
                    :class="{ 'field-error': message.isError }"
                  >
                    <label for="message"> Ihre Nachricht </label>

                    <textarea
                      id="message"
                      v-model="message.value"
                      :placeholder="message.placeholder"
                      rows="1"
                      required
                      @input="validateMessage"
                    />

                    <div class="error">{{ message.textError }}</div>
                  </div>

                  <p class="hint m-t-28">
                    Die mit einem Stern (*) markierten Felder sind
                    Pflichtfelder.
                  </p>

                  <div class="checkbox">
                    <label for="defoult-type">
                      <div
                        class="checkbox-marker"
                        :class="{ selected: isCheckbox }"
                      />
                      <input
                        id="defoult-type"
                        v-model="isCheckbox"
                        type="checkbox"
                      />
                    </label>

                    <div>
                      <div class="text-2-m m-b-8">
                        Datenschutz<sup class="text-danger">*</sup>
                      </div>

                      <p class="text-3">
                        Ich habe die <a href="#">Datenschutzbestimmungen</a> zur
                        Kenntnis genommen und die
                        <a href="#">AGB gelesen</a> und bin mit ihnen
                        einverstanden.
                      </p>
                    </div>
                  </div>

                  <button
                    type="submit"
                    class="btn-medium btn-primary m-t-28 w-full"
                    :class="{
                      disabled: !validationAllFields,
                    }"
                  >
                    Absenden
                  </button>
                </div>
              </div>
            </form>
          </div>

          <div class="col-6 col-lg-12">
            <div class="contact-persons-box-wrap">
              <div class="schedule-box">
                <h3>Zeitplan</h3>

                <div class="flex-v__center">
                  <icon-clock class="m-r-24" />

                  <div class="text-3">
                    <div class="m-b-8">Mo - Do 8:00 bis 17 Uhr</div>
                    <div>Fr 8:00 bis 16:00</div>
                  </div>
                </div>
              </div>

              <div class="contact-persons-box">
                <h3 class="m-b-16">Ihre Ansprechpartner</h3>

                <div class="contact-person">
                  <img :src="require('@images/woman-1.png')" alt="woman" />

                  <div>
                    <h4>Vertrieb</h4>

                    <div class="text-2-m m-b-20">Petra Bödeker</div>

                    <div class="text-3 m-b-8">Tel: 03379 316 44 0</div>

                    <div class="text-3">boedeker@docdorado.de</div>
                  </div>
                </div>

                <div class="contact-person">
                  <img :src="require('@images/men-1.png')" alt="men" />

                  <div>
                    <h4>Geschäftsführer</h4>

                    <div class="text-2-m m-b-20">Fabian Steinbrück</div>

                    <div class="text-3 m-b-8">Tel: 03379 316 44 0</div>

                    <div class="text-3">steinbrueck@docdorado.de</div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <icon-plus class="bg-icon-bottom-left" />
      <icon-plus class="bg-icon-top-right" />
    </section>
  </div>
</template>

<script>
import IconPlay from '@images/components/icon-play.vue'
import IconPlus from '@images/components/icon-plus.vue'
import IconEditToolZoomOut from '@images/tabs/edit-tool-zoom-out.vue'
import IconContentEditDraft from '@images/tabs/content-edit-draft.vue'
import IconClipboardCheck from '@images/tabs/clipboard-check.vue'
import IconSettingSlider from '@images/tabs/setting-slider.vue'
import IconClipboardList from '@images/tabs/clipboard-list.vue'
import IconLock from '@images/components/icon-lock.vue'
import IconTimeStopwatch from '@images/components/icon-time-stopwatch.vue'
import IconScanVoice from '@images/components/icon-scan-voice.vue'
import ImgHandlerHandelsvertreter from '@images/components/img-handler-handelsvertreter.vue'
import IconUserCircleGroup from '@images/components/icon-user-circle-group.vue'
import IconAwardCertificate from '@images/components/icon-award-certificate.vue'
import IconHierarchyVerticalSquare from '@images/components/icon-hierarchy-vertical-square.vue'

import ImgGroßhandel from '@images/components/img-großhandel.vue'
import IconMegaPhone from '@images/components/icon-mega-phone.vue'
import IconSecurityCheck from '@images/components/icon-security-check.vue'
import IconFingerPass from '@images/components/icon-finger-pass.vue'

import IconAlignBackRectangle from '@images/components/icon-align-back-rectangle.vue'
import IconEmail from '@images/components/icon-email.vue'
import IconSupport from '@images/components/icon-support.vue'
import IconClock from '@images/components/icon-clock.vue'

export default {
  name: 'IndexPage',

  components: {
    IconPlay,
    IconPlus,
    IconEditToolZoomOut,
    IconContentEditDraft,
    IconClipboardCheck,
    IconSettingSlider,
    IconClipboardList,
    IconLock,
    IconTimeStopwatch,
    IconScanVoice,
    ImgHandlerHandelsvertreter,
    IconUserCircleGroup,
    IconAwardCertificate,
    IconHierarchyVerticalSquare,
    ImgGroßhandel,
    IconMegaPhone,
    IconSecurityCheck,
    IconFingerPass,
    IconAlignBackRectangle,
    IconEmail,
    IconSupport,
    IconClock,
  },

  data() {
    return {
      articles: [
        {
          id: 'article1',
          url: require('@images/image-articles-1.png'),
          title: 'GKV Vertrag Pflegehilfsmittel',
          desc: 'Alles, was Sie über die Neuerungen in PG54 und PG51 wissen müssen',
        },
        {
          id: 'article2',
          url: require('@images/image-articles-2.png'),
          title: 'Anpassung & Innovation',
          desc: 'Pflegehilfsmittel im Zeitalter des demografischen Wandels',
        },
        {
          id: 'article3',
          url: require('@images/image-articles-3.png'),
          title: 'Ein umfassender Leitfaden',
          desc: 'Essentielle Pflegehilfsmittel für Alzheimer, Parkinson und Arthritis',
        },
      ],

      activeTabIndex: 1,
      tabs: [
        {
          icon: 'icon-edit-tool-zoom-out',
          name: 'Überwachung & Whitelabeling',
        },
        {
          icon: 'icon-content-edit-draft',
          name: 'Abrechnung',
        },
        {
          icon: 'icon-clipboard-check',
          name: 'Elektronischer Kostenvoranschlag',
        },
        {
          icon: 'icon-setting-slider',
          name: 'Individual Programmierung',
        },
        {
          icon: 'icon-clipboard-list',
          name: 'Reporting',
        },
      ],

      vorname: {
        value: '',
        placeholder: 'Vorname placeholder',
        textError: 'Nicht leer',
        isError: false,
      },

      nachname: {
        value: '',
        placeholder: 'Nachname placeholder',
        textError: 'Nicht leer',
        isError: false,
      },

      email: {
        value: '',
        placeholder: 'Senden Sie uns eine Email',
        textError: 'Nicht leer oder ungültig',
        isError: false,
      },

      unternehmen: {
        value: '',
        placeholder: 'Unternehmen placeholder',
      },

      tel: {
        value: '',
        placeholder: 'Telefonnummer placeholder',
        textError: 'Nicht leer',
        isError: false,
      },

      message: {
        value: '',
        placeholder: '',
        textError: 'Nicht leer',
        isError: false,
      },

      isCheckbox: false,
    }
  },

  computed: {
    validationAllFields() {
      return (
        this.vorname.value.length &&
        !this.vorname.isError &&
        this.nachname.value.length &&
        !this.nachname.isError &&
        this.email.value.length &&
        !this.email.isError &&
        this.tel.value.length &&
        !this.tel.isError &&
        this.message.value.length &&
        !this.message.isError &&
        this.isCheckbox
      )
    },
  },

  methods: {
    showVideo() {
      console.log('showVideo ->')
    },

    validateVorname() {
      this.vorname.isError = !this.vorname.value.length
    },

    validateNachname() {
      this.nachname.isError = !this.nachname.value.length
    },

    validateEmail() {
      const emailRegExp = /^[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,}$/
      this.email.isError = !emailRegExp.test(this.email.value)
    },

    validateTel() {
      this.tel.isError = !this.tel.value.length
    },

    validateMessage() {
      this.message.isError = !this.message.value.length
    },

    sendForm(data) {
      console.log('sendForm ->', data)
    },
  },
}
</script>
