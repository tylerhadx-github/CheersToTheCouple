<template>
  <div>
    <v-flex sm6 offset-sm3 xs12>
      <div v-html="Home"></div>
    </v-flex>

    <div id="Bride" style="scroll-margin:100px;"></div>
    <v-card>
      <v-card-title>
        <v-flex sm6 offset-sm3 xs12>
          <h3
            class="headline mb-0"
            style="text-align:center;font-family:'Lucida Bright' !important;"
          >
            Meet the Bride's Family
          </h3>
        </v-flex>
      </v-card-title>
      <v-card-text sm10 offset-sm1 xs12>
        <v-container fluid grid-list-md>
          <v-layout row wrap>
            <v-flex v-for="i in BrideFamily" :key="i">
              <v-card class="justify-center mx-auto text-xs-center">
                <v-avatar :tile="true" :size="250">
                  <v-img style="align-content:center" :src="i.image"></v-img>
                </v-avatar>
                <v-card-title primary-title style="justify-content:center">
                  <div>
                    <h3
                      class="headline mb-0"
                      style="font-family:'Lucida Bright' !important;text-align:center"
                    >
                      {{ i.title }}
                    </h3>
                  </div>
                </v-card-title>
              </v-card>
            </v-flex>
          </v-layout>
        </v-container>
      </v-card-text>
    </v-card>

    <div id="Groom" style="padding-top: 50px;"></div>
    <v-card>
      <v-card-title>
        <v-flex sm6 offset-sm3 xs12>
          <h3
            class="headline mb-0"
            style="text-align:center;font-family:'Lucida Bright' !important;"
          >
            Meet the Groom's family
          </h3>
        </v-flex>
      </v-card-title>
      <v-card-text sm10 offset-sm1 xs12>
        <v-container fluid grid-list-md>
          <v-layout row wrap>
            <v-flex v-for="i in GroomFamily" :key="i">
              <v-card class="justify-center mx-auto text-xs-center">
                <v-avatar :tile="true" :size="250">
                  <v-img :src="i.image"></v-img>
                </v-avatar>
                <v-card-title primary-title style="justify-content:center">
                  <div>
                    <h3
                      class="headline mb-0"
                      style="font-family:'Lucida Bright' !important;text-align:center"
                    >
                      {{ i.title }}
                    </h3>

                    <!--<div> {{ i.description }} </div>-->
                  </div>
                </v-card-title>
              </v-card>
            </v-flex>
          </v-layout>
        </v-container>
      </v-card-text>
    </v-card>

    <div id="RegistryDiv" style="scroll-margin:100px;padding-top:50px;"></div>
    <v-card id="Registry" style="scroll-margin:100px">
      <v-card-title>
        <v-flex sm6 offset-sm3 xs12>
          <h3
            class="headline mb-0"
            style="text-align:center;font-family:'Lucida Bright' !important;"
          >
            Registry
          </h3>
        </v-flex>
      </v-card-title>
      <v-card-text>
        <v-flex class="xs12">
          <div style="text-align:center">
            <v-btn
              color="yellow"
              href="https://amazon.com/wedding/share/cheerstothecouple"
              tile
            >
              <v-icon>fab fa-amazon</v-icon>
              Wedding Registry
            </v-btn>
          </div>
        </v-flex>
      </v-card-text>
    </v-card>

    <div id="WeddingVenue" style="scroll-margin:100px;padding-top:50px;"></div>
    <!--<v-card>
        <v-card-title>
            <v-flex sm6 offset-sm3 xs12>

                <h3 class="headline mb-0" style="text-align:center;font-family:'Lucida Bright' !important;">Schedule</h3>
            </v-flex>
        </v-card-title>
        <v-card-text style="text-align:center">
            <div>
                Wedding 4-5pm <a href="../Content/Tyler_Haddix__Elisabeth_Hofer_Wedding.ics">Add to Calendar</a>
            </div>

            <br />
        </v-card-text>
    </v-card>-->
    <v-card flat>
      <v-card-title>
        <v-flex sm6 offset-sm3 xs12>
          <h3
            class="headline mb-0"
            style="text-align:center;font-family:'Lucida Bright' !important;"
          >
            Wedding Venue
          </h3>
        </v-flex>
      </v-card-title>
      <v-card-text>
        <v-layout row wrap>
          <v-flex class="xs6">
            <div class="headline">Cathedral of Our Lady of Perpetual Help</div>
            <p class="pt-3">520 Cathedral Drive / Rapid City, SD 57701</p>

            <div>Ceremony at 4 o'clock in the afternoon</div>
            <div>Reception to follow 5-11pm</div>
            <v-container grid-list-sm fluid>
              <v-layout row wrap>
                <v-flex v-for="n in churchImages" :key="n" xs6 d-flex>
                  <v-card flat tile class="d-flex">
                    <v-img :src="n" aspect-ratio="1.6" class="grey lighten-2">
                      <template v-slot:placeholder>
                        <v-layout fill-height align-center justify-center ma-0>
                          <v-progress-circular
                            indeterminate
                            color="grey lighten-5"
                          ></v-progress-circular>
                        </v-layout>
                      </template>
                    </v-img>
                  </v-card>
                </v-flex>
              </v-layout>
            </v-container>
          </v-flex>
          <v-flex class="xs6 hidden-sm-and-down">
            <iframe
              src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d5733.939410731136!2d-103.2171898521845!3d44.06333418786988!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x877d4318dca9ff83%3A0xf7104a074835f28c!2sCathedral%20of%20Our%20Lady%20of%20Perpetual%20Help%20Church!5e0!3m2!1sen!2sus!4v1586754355009!5m2!1sen!2sus"
              :width="500 / 2"
              :height="500 / 2"
              frameborder="0"
              style="border:0;"
              allowfullscreen=""
              aria-hidden="false"
              tabindex="0"
            ></iframe>
          </v-flex>
        </v-layout>
        <v-flex class="xs12 hidden-md-and-up">
          <iframe
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d5733.939410731136!2d-103.2171898521845!3d44.06333418786988!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x877d4318dca9ff83%3A0xf7104a074835f28c!2sCathedral%20of%20Our%20Lady%20of%20Perpetual%20Help%20Church!5e0!3m2!1sen!2sus!4v1586754355009!5m2!1sen!2sus"
            :width="500"
            :height="500"
            frameborder="0"
            style="border:0;"
            allowfullscreen=""
            aria-hidden="false"
            tabindex="0"
          ></iframe>
        </v-flex>
      </v-card-text>
    </v-card>

    <div
      id="ReceptionVenue"
      style="scroll-margin:100px;padding-top:50px;"
    ></div>
    <v-card flat>
      <v-card-title>
        <v-flex sm6 offset-sm3 xs12>
          <h3
            class="headline mb-0"
            style="text-align:center;font-family:'Lucida Bright' !important;"
          >
            Reception Venue
          </h3>
        </v-flex>
      </v-card-title>
      <v-card-text>
        <v-layout row wrap>
          <v-flex class="xs6 ">
            <div class="headline">
              Blessed Sacrament Catholic Church
            </div>
            <p class="pt-3">4500 Jackson Boulevard / Rapid City, SD 57702</p>

            <div>Light Appetizers</div>
            <div>Beer and Wine</div>
            <div>Dinner at 6:30pm</div>
            <v-container grid-list-sm fluid>
              <v-layout row wrap>
                <v-flex v-for="n in bsImages" :key="n" xs8 d-flex>
                  <v-card flat tile class="d-flex">
                    <v-img
                      :src="n"
                      aspect-ratio="1.84615"
                      class="grey lighten-2"
                    >
                      <template v-slot:placeholder>
                        <v-layout fill-height align-center justify-center ma-0>
                          <v-progress-circular
                            indeterminate
                            color="grey lighten-5"
                          ></v-progress-circular>
                        </v-layout>
                      </template>
                    </v-img>
                  </v-card>
                </v-flex>
              </v-layout>
            </v-container>
          </v-flex>
          <v-flex class="xs6 hidden-sm-and-down">
            <iframe
              src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d11468.181529843847!2d-103.2944355!3d44.0617715!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x8637107982ff75c8!2sBlessed%20Sacrament%20Catholic%20Church!5e0!3m2!1sen!2sus!4v1593982756459!5m2!1sen!2sus"
              :width="500 / 2"
              :height="500 / 2"
              frameborder="0"
              style="border:0;"
              allowfullscreen=""
              aria-hidden="false"
              tabindex="0"
            ></iframe>
          </v-flex>
        </v-layout>
        <v-flex class="xs12 hidden-md-and-up">
          <iframe
            src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d11468.181529843847!2d-103.2944355!3d44.0617715!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x8637107982ff75c8!2sBlessed%20Sacrament%20Catholic%20Church!5e0!3m2!1sen!2sus!4v1593982756459!5m2!1sen!2sus"
            :width="500"
            :height="500"
            frameborder="0"
            style="border:0;"
            allowfullscreen=""
            aria-hidden="false"
            tabindex="0"
          ></iframe>
        </v-flex>
      </v-card-text>
    </v-card>

    <div id="Hotel" style="scroll-margin:100px;padding-top:50px;"></div>
    <v-card>
      <v-card-title>
        <v-flex sm6 offset-sm3 xs12>
          <h3
            class="headline mb-0"
            style="text-align:center;font-family:'Lucida Bright' !important;"
          >
            Hotel Information
          </h3>
        </v-flex>
      </v-card-title>
      <v-card-text>
        <v-layout row wrap>
          <v-flex class="xs6">
            <a
              href="https://www.marriott.com/events/start.mi?id=1592347247108&key=GRP"
              >Click Here for wedding block information</a
            >

            <div>
              Start Date: Thursday, October 8, 2020
            </div>
            <div>
              End Date: Saturday, October 10, 2020
            </div>
            <div>
              Last Day to Book: Wednesday, September 9, 2020
            </div>
            <div>
              Hotel offering your special group rate:
            </div>
            <div>
              Fairfield Inn & Suites Rapid City for 79 USD per night
            </div>
          </v-flex>
          <v-flex class="xs6 hidden-sm-and-down">
            <iframe
              src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d11461.08378359627!2d-103.1489259!3d44.098401!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x294e4ba1b22010bc!2sFairfield%20Inn%20%26%20Suites%20by%20Marriott%20Rapid%20City!5e0!3m2!1sen!2sus!4v1593983249628!5m2!1sen!2sus"
              :width="500 / 2"
              :height="500 / 2"
              frameborder="0"
              style="border:0;"
              allowfullscreen=""
              aria-hidden="false"
              tabindex="0"
            ></iframe>
          </v-flex>
        </v-layout>
        <v-flex class="xs12 hidden-md-and-up">
          <iframe
            src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d11461.08378359627!2d-103.1489259!3d44.098401!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x294e4ba1b22010bc!2sFairfield%20Inn%20%26%20Suites%20by%20Marriott%20Rapid%20City!5e0!3m2!1sen!2sus!4v1593983249628!5m2!1sen!2sus"
            :width="500"
            :height="500"
            frameborder="0"
            style="border:0;"
            allowfullscreen=""
            aria-hidden="false"
            tabindex="0"
          ></iframe>
        </v-flex>
      </v-card-text>
    </v-card>

    <v-card id="Interest" style="scroll-margin:100px;padding-top:50px;">
      <v-card-title>
        <v-flex sm6 offset-sm3 xs12>
          <h3
            class="headline mb-0"
            style="text-align:center;font-family:'Lucida Bright' !important;"
          >
            Local Attractions
          </h3>
        </v-flex>
      </v-card-title>
      <v-card-text>
        <v-layout row wrap>
          <v-flex class="xs6 hidden-sm-and-down">
            <v-container grid-list-sm fluid>
              <v-layout row wrap>
                <v-flex v-for="n in placesImages" :key="n" xs4 d-flex>
                  <v-card flat tile class="d-flex">
                    <v-card-title>{{ n.name }}</v-card-title>

                    <v-img :src="n.url" aspect-ratio="1" class="grey lighten-2">
                      <template v-slot:placeholder>
                        <v-layout fill-height align-center justify-center ma-0>
                          <v-progress-circular
                            indeterminate
                            color="grey lighten-5"
                          ></v-progress-circular>
                        </v-layout>
                      </template>
                    </v-img>
                  </v-card>
                </v-flex>
              </v-layout>
            </v-container>
          </v-flex>
          <v-flex class="xs6 hidden-sm-and-down">
            <v-icon color="red">stars</v-icon> The couple's favorite places.
            <br />
            <v-icon color="blue">location_on</v-icon> The touristy things
            <iframe
              src="https://www.google.com/maps/d/u/1/embed?mid=1wxREjsK_T_ZFBISaTHaRZaaq852vlQta"
              :width="500/ 2"
              :height="500 / 2"
              frameborder="0"
              style="border:0;"
              allowfullscreen=""
              aria-hidden="false"
              tabindex="0"
            ></iframe>
          </v-flex>
        </v-layout>
        <v-flex
          class="xs12 hidden-md-and-up"
          style="justify-content:center;text-align:center"
        >
          <v-icon color="red">stars</v-icon> The couple's favorite places.
          <br />
          <v-icon color="blue">location_on</v-icon> The touristy things
          <iframe
            src="https://www.google.com/maps/d/u/1/embed?mid=1wxREjsK_T_ZFBISaTHaRZaaq852vlQta"
            :width="500"
            :height="500"
          ></iframe>
        </v-flex>
      </v-card-text>
    </v-card>

    <div id="Photos" style="scroll-margin:100px;padding-top:50px;"></div>
    <v-card>
      <v-card-text>
        <div class="elfsight-app-e435b29b-176d-4e00-a99c-bcb82354e5fa"></div>
      </v-card-text>
    </v-card>

    <div id="Song" style="scroll-margin:100px;padding-top:50px"></div>
    <v-card id="SongRequest" style="scroll-margin:100px;">
      <v-card-title>
        <v-flex sm6 offset-sm3 xs12 justify-center>
          <h3
            class="headline mb-0"
            style="text-align:center;font-family:'Lucida Bright' !important;"
          >
            Help the couple throw a great reception by sharing the best dancing
            tunes:
          </h3>
          <div class="text-xs-center">
            <v-btn @click="requestSong = !requestSong">Request a Song!</v-btn>
            <!-- The Queue -->
          </div>
          <div class="text-xs-center">
            <v-btn @click="queue = !queue">The Queue</v-btn>
            <!-- The Queue -->
          </div>
        </v-flex>
      </v-card-title>
      <v-card-text>
        <v-flex class="xs8 offset-xs3 hidden-sm-and-down">
          <div v-if="requestSong">
            <iframe
              src="https://docs.google.com/forms/d/e/1FAIpQLSeDfX0PgYpmAt3Lt7qurJE4PgwgBcnxdlukaqQy1E36vimhSA/viewform?embedded=true"
              :width="800"
              :height="500 / 2"
              frameborder="0"
              marginheight="0"
              marginwidth="0"
              >Loading…</iframe
            >
          </div>
        </v-flex>
        <v-flex class="xs12 hidden-md-and-up">
          <div v-if="requestSong">
            <iframe
              src="https://docs.google.com/forms/d/e/1FAIpQLSeDfX0PgYpmAt3Lt7qurJE4PgwgBcnxdlukaqQy1E36vimhSA/viewform?embedded=true"
              :width="400"
              :height="500 / 2"
              frameborder="0"
              marginheight="0"
              marginwidth="0"
              >Loading…</iframe
            >
          </div>
        </v-flex>

        <v-flex class="xs8 offset-xs3 hidden-sm-and-down">
          <div v-if="queue">
            <iframe
              src="https://open.spotify.com/embed/user/spotify/playlist/1tQF9rff6vXq5qNSWubcFx?si=fVFkU0j0R8WIib8Da42B0Q"
              :width="800"
              :height="500 / 2"
              frameborder="0"
              marginheight="0"
              marginwidth="0"
              >Loading…</iframe
            >
          </div>
        </v-flex>
        <v-flex class="xs12 hidden-md-and-up">
          <div v-if="queue">
            <iframe
              src="https://open.spotify.com/embed/user/spotify/playlist/1tQF9rff6vXq5qNSWubcFx?si=fVFkU0j0R8WIib8Da42B0Qg"
              :width="400"
              :height="500 / 2"
              frameborder="0"
              marginheight="0"
              marginwidth="0"
              >Loading…</iframe
            >
          </div>
        </v-flex>
      </v-card-text>
    </v-card>

    <div id="Notes" style="scroll-margin:100px;padding-top:50px;"></div>
    <v-card id="NotesRequest" style="scroll-margin:100px;">
      <v-card-title>
        <v-flex sm6 offset-sm3 xs12 justify-center>
          <h3
            class="headline mb-0"
            style="text-align:center;font-family:'Lucida Bright' !important;"
          >
            Leave a toast for the couple!
          </h3>
          <div class="text-xs-center">
            <v-btn @click="NotesRequest = !NotesRequest">Cheers</v-btn>
          </div>
        </v-flex>
      </v-card-title>
      <v-card-text>
        <v-flex class="xs8 offset-xs3 hidden-sm-and-down">
          <div v-if="NotesRequest">
            <iframe
              src="https://docs.google.com/forms/d/e/1FAIpQLSdCfBEtvEdcj4EfB48M47HX_F8DmCCmHKBL4dK3rxn_yKmMxQ/viewform?embedded=true"
              :width="800"
              :height="500 / 2"
              frameborder="0"
              marginheight="0"
              marginwidth="0"
              >Loading…</iframe
            >
          </div>
        </v-flex>
        <v-flex class="xs12 hidden-md-and-up">
          <div v-if="NotesRequest">
            <iframe
              src="https://docs.google.com/forms/d/e/1FAIpQLSdCfBEtvEdcj4EfB48M47HX_F8DmCCmHKBL4dK3rxn_yKmMxQ/viewform?embedded=true"
              :width="400"
              :height="500"
              frameborder="0"
              marginheight="0"
              marginwidth="0"
              >Loading…</iframe
            >
          </div>
        </v-flex>
      </v-card-text>
    </v-card>

    <div id="FAQ" style="scroll-margin:100px;padding-top:50px;"></div>
    <v-card id="FAQ" style="scroll-margin:100px;">
      <v-card-title>
        <v-flex sm6 offset-sm3 xs12 justify-center>
          <h3
            class="headline mb-0"
            style="text-align:center;font-family:'Lucida Bright' !important;"
          >
            Frequently Asked Questions
          </h3>
        </v-flex>
      </v-card-title>
      <v-card-text>
        <v-expansion-panel>
          <v-expansion-panel-content v-for="(item, i) in FAQ" :key="i">
            <template v-slot:header>
              <div v-html="item.title"></div>
            </template>
            <v-card>
              <v-card-text>
                <div v-html="item.description"></div>
              </v-card-text>
            </v-card>
          </v-expansion-panel-content>
        </v-expansion-panel>
      </v-card-text>
    </v-card>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      Home: "",
      requestSong: false,
      NotesRequest: false,
      queue: false,
      FAQ: [
        {
          title: "HAS COVID-19 CHANGED THE WEDDING PLANS?",
          description:
            "This is a crazy time. We completely understand if you are uncomfortable attending because of COVID. If you are uncomfortable with anything less than strict social distancing we invite you to join virtually, and we look forward to enjoying your company in the future. Happily, our church will be able to live stream the ceremony. Check back here closer to October 9th.",
          faqid: 1
        },
        {
          title: "WILL THERE BE ADJUSTMENTS FOR SOCIAL DISTANCING?",
          description:
            "Guests will be sitting every-other pew. Please sit one family to a pew. The parish recommends wearing a mask. At the reception, hand sanitizer will be available; however, we are allowing our guests to social distance according to their comfort level.",
          faqid: 2
        },
        {
          title: "ARE KIDS INVITED?",
          description:
            "Please! We hope to have a day filled with the type of energy and merriment that children bring to events. We love kids!",
          faqid: 3
        },
        {
          title: "WHAT IS THE DRESSCODE?",
          description:
            "Festive attire - let's get ready to EAT, DRINK, and be MARRIED!",
          faqid: 4
        }
      ],
      BrideFamily: [
        {
          image: "https://ourwedding.sirv.com/lonnylinda.webp",
          title: "Lonny and Linda Hofer",
          description: "Bride's Parents"
        },
        {
          image: "https://ourwedding.sirv.com/adam.webp",
          title: "Fr. Adam Hofer",
          description: "Brother"
        },
        {
          image: "https://ourwedding.sirv.com/michael2.webp",
          title: "Michael Hofer",
          description: "Brother"
        },
        {
          image: "https://ourwedding.sirv.com/johnnybrittany.webp",
          title: "Johnny and Brittany Hofer",
          description: "Brother"
        },
        {
          image: "https://ourwedding.sirv.com/marianne.webp",
          title: "Marianne Hofer",
          description: "Sister"
        }
      ],
      GroomFamily: [
        {
          image: "https://ourwedding.sirv.com/davidsue.webp",
          title: "David and Sue Haddix",
          description: "Groom's Parents"
        },

        {
          image: "https://ourwedding.sirv.com/dylankourt.webp",
          title: "Dylan and Kourtney Haddix",
          description: "Brother and Sister-in-law"
        }
      ],
      churchImages: [
        "https://ourwedding.sirv.com/olph.webp"
        //'https://scontent.ffsd3-1.fna.fbcdn.net/v/t1.0-9/92214930_2518148995068489_9115814021264572416_o.jpg?_nc_cat=109&_nc_sid=dd9801&_nc_ohc=RW6dzLZc6SMAX9igLdM&_nc_ht=scontent.ffsd3-1.fna&oh=4eb59987fc6621fed435bad0270f9719&oe=5EE5A9ED',
        //'https://scontent.ffsd3-1.fna.fbcdn.net/v/t1.0-9/p720x720/36913854_2058067304409996_1992187221238611968_o.jpg?_nc_cat=108&_nc_sid=dd9801&_nc_ohc=NV4-QNXu3XQAX_J2OrF&_nc_ht=scontent.ffsd3-1.fna&_nc_tp=6&oh=cfb6e9bd5cea95f72c6d6fba5f01e0a5&oe=5EE3FE73'
      ],

      bsImages: ["https://ourwedding.sirv.com/bsc.webp"],
      placesImages: [
        {
          name: "Devils Tower",
          url:
            "https://www.nps.gov/common/uploads/grid_builder/deto/crop16_9/893914AB-C506-A2AD-D41690FD11B7B348.jpg?width=307&quality=90&mode=crop"
        },

        {
          name: "Roughlock Falls",
          url:
            "https://www.blackhillsbadlands.com/sites/default/files/styles/bhb40_page_hero/public/photos/parks-monuments/roughlock-falls-nature-area/roughlockfalls-fall080192.jpg?itok=_XPXR2eM"
        },
        {
          name: "Devils Bathtub",
          url:
            "http://enjoyingsouthdakota.com/wp-content/uploads/2014/09/devils-bathtub-south-dakota-in-spearfish-canyon_thumb.jpg"
        },
        {
          name: "Jewel Cave",
          url:
            "https://lh3.googleusercontent.com/p/AF1QipP8VcQ7rBKMOqeNb04JM7n7ZwcTYnIYhtTrwzUI=s1600-h2268"
        }
      ]
    };
  },
  methods: {
    toAttractions() {
      window.location = "https://www.blackhillsbadlands.com/attractions";
    },
    computed: {
      windowSize: function() {
        return { x: 500, y: 500 };
      }
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
