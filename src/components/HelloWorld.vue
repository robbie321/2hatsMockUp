<template>
  <div>
    <div class="jumbotron">
      <v-layout row>
        <v-flex xs8 md4 sm8>
          <h1 class="logoText">
            <img
              style="width: 10%; height:auto;"
              src="https://img.icons8.com/ios/50/FFFFFF/maple-leaf.png"
            />
            MOKUZAI
          </h1>
        </v-flex>

        <v-flex text-right>
          <v-btn small text style="margin-top:-40px;">
            <v-icon style="font-size:15px" color="white">fas fa-search</v-icon>
          </v-btn>
          <v-btn small text style="margin-top:-40px">
            <v-icon style="font-size:15px;" color="white">fas fa-bars</v-icon>
          </v-btn>
        </v-flex>
      </v-layout>

      <v-container>
        <v-layout class="fullScreen">
          <v-flex xs11 md9>
            <h1 class="headerText">Great design is eliminating all unnecessary details</h1>
            <br />
            <h1 class="headerTagText">-MINH D. TRAN</h1>
          </v-flex>
        </v-layout>
      </v-container>
    </div>

    <v-container>
      <v-layout justify-center row>
        <v-btn class="ItemOrder" text>MOST POPULAR</v-btn>
        <v-btn class="ItemOrder" text>LOWEST PRICE</v-btn>
        <v-btn class="ItemOrder" text>HIGHEST PRICE</v-btn>
      </v-layout>
      <div class="block">
        <v-layout justify-center row wrap class="items">
          <v-flex xs10 sm8 md3 v-for="item in ITEMS" :key="item.price">
            <v-container>
              <v-card class="cardMargin" flat color="white">
                <v-container fluid>
                  <v-layout row>
                    <v-flex xs12 sm10 md12>
                      <v-img :src="item.image"></v-img>
                    </v-flex>
                  </v-layout>
                </v-container>
              </v-card>
              <div>
                <v-card-text class="ItemTitle">
                  {{item.title}}
                  <br />
                  <span class="price">$ {{item.price}}</span>
                </v-card-text>
              </div>
            </v-container>
          </v-flex>
        </v-layout>
      </div>
      <v-layout justify-center row>
        <v-btn id="btn" v-on:click="click()" x-small text>1</v-btn>
        <v-btn id="btn" x-small text>2</v-btn>
        <v-btn id="btn" x-small text>3</v-btn>
        <v-btn id="btn" x-small text>4</v-btn>
      </v-layout>
    </v-container>
  </div>
</template>

<script>
export default {
  data: () => ({
    ITEMS: [
      {
        title: "Walnut Speakers & Amp",
        price: 599,
        image:
          "https://firebasestorage.googleapis.com/v0/b/production2hats.appspot.com/o/studentPortal%2Fassessment-web-design%2Fwalnut_speakers.png?alt=media&token=d93fffb6-934f-4e5b-894f-53dd76f12758"
      },
      {
        title: "Maple Lamp",
        price: 109,
        image:
          "https://firebasestorage.googleapis.com/v0/b/production2hats.appspot.com/o/studentPortal%2Fassessment-web-design%2Fmaple_lamp.png?alt=media&token=dbf69300-4590-4490-ab14-82c901b50e9f"
      },
      {
        title: "Walnut Planter",
        price: 39,
        image:
          "https://firebasestorage.googleapis.com/v0/b/production2hats.appspot.com/o/studentPortal%2Fassessment-web-design%2Fwalnut_planter.png?alt=media&token=b7692959-ef86-474d-8166-5db596de1c0a"
      },
      {
        title: "M18 Chair, Grey Wool Felt",
        price: 330,
        image:
          "https://firebasestorage.googleapis.com/v0/b/production2hats.appspot.com/o/studentPortal%2Fassessment-web-design%2Fm18_chair.png?alt=media&token=e85dfda9-3354-4917-8b29-5fc10967ac79"
      },
      {
        title: "Pliot Stool, Black",
        price: 265,
        image:
          "https://firebasestorage.googleapis.com/v0/b/production2hats.appspot.com/o/studentPortal%2Fassessment-web-design%2Fpilot_stool.png?alt=media&token=e2dde4e8-60ba-476a-b208-4d5d2e7e96e5"
      },
      {
        title: "B&O BeoPlay A9 - Rose Gold",
        price: 2999,
        image:
          "https://firebasestorage.googleapis.com/v0/b/production2hats.appspot.com/o/studentPortal%2Fassessment-web-design%2Fbeoplay.png?alt=media&token=d5529aa4-0489-4b2b-987d-6ae27c9391bf"
      },
      {
        title: "Joey Roth CRM-001 Ceramic",
        price: 495,
        image:
          "https://firebasestorage.googleapis.com/v0/b/production2hats.appspot.com/o/studentPortal%2Fassessment-web-design%2Fjoey_roth.png?alt=media&token=d4a1b728-e23d-41e6-bee2-7e186ba99d78"
      },
      {
        title: "V5BT Bamboo Speaker",
        price: 200,
        image:
          "https://firebasestorage.googleapis.com/v0/b/production2hats.appspot.com/o/studentPortal%2Fassessment-web-design%2Fv5bt_bamboo.png?alt=media&token=9427be8b-ed72-4707-91bb-00a78f755c4f"
      },
      {
        title: "Walnut iPhone Case",
        price: 79,
        image:
          "https://firebasestorage.googleapis.com/v0/b/production2hats.appspot.com/o/studentPortal%2Fassessment-web-design%2Fwalnut_iphone.png?alt=media&token=582a2057-44c8-4188-a4c8-18ed150989df"
      },
      {
        title: "Walnut Watch (Round)",
        price: 239,
        image:
          "https://firebasestorage.googleapis.com/v0/b/production2hats.appspot.com/o/studentPortal%2Fassessment-web-design%2Fwalnut_watch.png?alt=media&token=7b6cff3c-6a0e-4249-bebb-d3bb1978bc70"
      },
      {
        title: "Polk Audio Wireless",
        price: 705,
        image:
          "https://firebasestorage.googleapis.com/v0/b/production2hats.appspot.com/o/studentPortal%2Fassessment-web-design%2Fpolk_audio.png?alt=media&token=bf4f68f5-e9c6-4a75-bc35-aacb55986a63"
      },
      {
        title: "Zebra Series Varberg Table",
        price: 89,
        image:
          "https://firebasestorage.googleapis.com/v0/b/production2hats.appspot.com/o/studentPortal%2Fassessment-web-design%2Fzebra_series.png?alt=media&token=92a63799-6e87-44ce-8c15-68f3d160d3be"
      },
      {
        title: "POTS Pedestal Set",
        price: 67,
        image:
          "https://firebasestorage.googleapis.com/v0/b/production2hats.appspot.com/o/studentPortal%2Fassessment-web-design%2Fpots_pedestal.png?alt=media&token=1b21646c-5d4d-41d7-8cf0-212e1a5dab0d"
      },
      {
        title: "SoundLink Bluetooth Mobile",
        price: 300,
        image:
          "https://firebasestorage.googleapis.com/v0/b/production2hats.appspot.com/o/studentPortal%2Fassessment-web-design%2Fsoundlink_bluetooth.png?alt=media&token=5d8029fc-1760-4b22-b293-9ac29eb3d251"
      },
      {
        title: 'Wall Clock OJ Black 31.5"',
        price: 100,
        image:
          "https://firebasestorage.googleapis.com/v0/b/production2hats.appspot.com/o/studentPortal%2Fassessment-web-design%2Fwall_clock.png?alt=media&token=41a3acb0-6b08-4146-9706-f22ac05905c0"
      },
      {
        title: "Cherry Wood Graph 3-Pack",
        price: 10,
        image:
          "https://firebasestorage.googleapis.com/v0/b/production2hats.appspot.com/o/studentPortal%2Fassessment-web-design%2Fcherry_wood.png?alt=media&token=a70a9ac4-21a1-4933-8a41-f214debcff57"
      }
    ]
  }),
  methods: {
    click() {
      let button = document.getElementById("btn");
      button.style.borderBottom = "1px";
      // button.style.border = "solid";
    }
  }
};
</script>
<style scoped>
.jumbotron {
  background: white;
  background-image: url(https://firebasestorage.googleapis.com/v0/b/production2hats.appspot.com/o/studentPortal%2Fassessment-web-design%2Fhero.png?alt=media&token=83f29b93-3c2e-4e50-8641-0eda16a0d960);
  background-size: cover;
  max-width: 100%;
  height: auto;
  border: 20px;
  border-style: solid;
  border-color: white;
  /* max-width: 100%; */
  /* margin: 0 auto; */
}

@media screen and (max-width: 700px) {
  .cardMargin {
    margin-bottom: 2px;
    border-radius: 20px;
  }
}
.push-spaces {
  height: 500px;
  width: 100%;
}
@media screen and (max-width: 700px) {
  .block {
    width: 300px;
    margin: auto;
  }
}
@media screen and (min-width: 800px) {
  .block {
    width: 850px;
    margin: auto;
  }
}
@media screen and (min-width: 800px) {
  .ItemTitle {
    font-family: "Raleway", sans-serif;
    font-size: 1vw;
  }
}
@media screen and (max-width: 799px) {
  .ItemTitle {
    font-family: "Raleway", sans-serif;
    font-size: 4vw;
  }
}
.price {
  font-family: "Courier New", Courier, monospace;
  color: #7e7e7e;
}
.headerText {
  font-family: "Raleway", sans-serif;
  margin-top: 80px;
  letter-spacing: 3px;
  color: white;
  font-size: 4vw;
}
.headerTagText {
  font-family: "Noticia Text", serif;
  margin-bottom: 150px;
  letter-spacing: 3px;
  color: grey;
  font-size: 1.5vw;
}
.logoText {
  margin-top: -20px;
  letter-spacing: 8px;
  color: white;
  font-size: 2vw;
}
@media screen and (min-width: 800px) {
  .fullScreen {
    margin-left: 120px;
  }
}

.ItemOrder {
  margin-bottom: 50px;
  margin-top: -40px;
}
</style>
