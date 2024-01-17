<template>
  <v-card>
    <div @mouseleave="showText = false">
      <v-row style="background-color: rgb(102, 48, 143)">
        <v-col
          :cols="changecol ? '4' : '12'"
          sm="4"
          style="
            align-items: center;
            display: flex;
            background-color: rgb(102, 48, 143);
          "
          @mouseenter="showText = false"
        >
          <div style="">
            <v-img
              class="iconend"
              src="https://iblaos.com/iblaos/image/logo.svg"
              style="
                width: 300px;
                height: 100px;
                object-fit: cover;
                max-width: none !important;
                display: block;
              "
            >
            </v-img>
          </div>
        </v-col>

        <v-col
          v-if="show"
          cols="12"
          sm="8"
          style="background-color: rgb(102, 48, 143)"
        >
          <!-- <v-col
          v-if="show"
          class="mx-0"
          style="display: flex; align-items: center; justify-content: center; height: 100%; magin-top:0px"
        > -->
          <div
            style="
              height: 100%;
              display: flex;
              align-items: center;
              justify-content: center;
            "
            class="grid"
          >
            <div
              style="height: 100px; background-color: rgb(102, 48, 143)"
              text
              disabled="true"
              @mouseenter="showText = false"
            >
              <v-col class="wrapper"> </v-col>
            </div>

            <v-btn
              class="about-btn"
              style="height: 100px; color: transparent"
              text
              @mouseenter="showText = 'About'"
            >
              <div class="wrapper">
                <div style="padding-bottom: 10px; color: white" fontsize>
                  About
                </div>
                <div style="color: #aca8a8; text-transform: uppercase">
                  i<span style="text-transform: lowercase"
                    >ndoChina
                    <span style="text-transform: uppercase">B</span>ank</span
                  >
                </div>
              </div>
              <v-icon
                v-if="showText === 'About'"
                size="50"
                color="rgb(255, 128, 0)"
                style="
                  position: fixed;
                  z-index: 100;
                  top: 70px;
                  width: 50px;
                  max-width: 100%;
                "
                >mdi-triangle-small-up</v-icon
              >
            </v-btn>

            <v-btn
              class="about-btn"
              style="height: 100px; color: transparent"
              text
              @mouseenter="showText = 'personal'"
            >
              <div class="wrapper">
                <div style="padding-bottom: 10px; color: white" fontsize>
                  Personal
                </div>
                <div style="color: #aca8a8; text-transform: uppercase">
                  <span style="text-transform: lowercase">
                    <span style="text-transform: uppercase">B</span>anking</span
                  >
                </div>
              </div>
              <v-icon
                v-if="showText === 'personal'"
                size="50"
                color="rgb(255, 128, 0)"
                style="
                  position: fixed;
                  z-index: 100;
                  top: 70px;
                  width: 50px;
                  max-width: 100%;
                "
                >mdi-triangle-small-up</v-icon
              >
            </v-btn>
            <v-btn
              class="about-btn"
              style="height: 100px; color: transparent"
              text
              @mouseenter="showText = 'corporate'"
            >
              <div class="wrapper">
                <div style="padding-bottom: 10px; color: white" fontsize>
                  corporate
                </div>
                <div style="color: #aca8a8; text-transform: uppercase">
                  <span style="text-transform: lowercase">
                    <span style="text-transform: uppercase">B</span>anking</span
                  >
                </div>
              </div>
              <v-icon
                v-if="showText === 'corporate'"
                size="50"
                color="rgb(255, 128, 0)"
                style="
                  position: fixed;
                  z-index: 100;
                  top: 70px;
                  width: 50px;
                  max-width: 100%;
                "
                >mdi-triangle-small-up</v-icon
              >
            </v-btn>
            <v-btn
              class="about-btn"
              style="height: 100px; color: transparent"
              text
              @mouseenter="showText = 'premier'"
            >
              <div class="wrapper">
                <div style="padding-bottom: 10px; color: white" fontsize>
                  premier
                </div>
                <div style="color: #aca8a8; text-transform: uppercase">
                  <span style="text-transform: lowercase">
                    <span style="text-transform: uppercase">B</span>anking</span
                  >
                </div>
              </div>
              <v-icon
                v-if="showText === 'premier'"
                size="50"
                color="rgb(255, 128, 0)"
                style="
                  position: fixed;
                  z-index: 100;
                  top: 70px;
                  width: 50px;
                  max-width: 100%;
                "
                >mdi-triangle-small-up</v-icon
              >
            </v-btn>
            <v-btn
              class="about-btn"
              style="height: 100px; color: white"
              text
              @mouseenter="showText = false"
            >
              <div class="wrapper">
                <div style="padding-bottom: 10px" fontsize>reward</div>
                <div style="color: #aca8a8; text-transform: uppercase">
                  P<span style="text-transform: lowercase">rogram</span>
                </div>
              </div>
            </v-btn>
            <v-btn
              class="about-btn"
              style="height: 100%; color: white"
              text
              @mouseenter="showText = false"
            >
              <div class="wrapper">
                <div style="padding-bottom: 10px" fontsize>cool</div>
                <div style="color: #aca8a8; text-transform: uppercase">
                  L<span style="text-transform: lowercase">ifestyle </span>
                </div>
              </div>
            </v-btn>
          </div>
        </v-col>
        <v-col
          v-if="!show"
          class="iconend"
          style="
            display: flex;
            align-items: center;
            justify-content: flex-end;
            width: 300px;
            height: 123px;
            background-color: ;
          "
          :cols="changecol ? '8' : '12'"
          sm="8"
        >
          <!-- <div 
          style="
            height: 100%;
            display: flex;
            justify-content: flex-end;
            background-color:yellow


          "
          class="btn-end"
        > -->
          <v-btn
            style="
              box-shadow: none;
              background-color: rgb(102, 48, 143);
              border-radius: 5px;
              border: 1px solid;
            "
            @click="
              buttomdetail === true
                ? (buttomdetail = false)
                : (buttomdetail = true)
            "
          >
            <v-icon size="30">mdi-view-sequential</v-icon>
          </v-btn>
          <!-- </div> -->
        </v-col>
        <!-- </v-col> -->
      </v-row>
      <div>
        <v-card flat class="red-background">
          <v-main>
            <v-col
              v-if="
                showText == 'About' ||
                showText == 'Personal' ||
                showText == 'Corporate' ||
                showText == 'Premier'
              "
              class="pa-0"
              :style="{
                top: showText ? '80px' : 'auto',
                position: showText ? 'fixed' : 'relative',
                zIndex: 10,
              }"
            >
              <div class="pa-0">
                <v-col class="pa-0">
                  <v-row>
                    <v-col
                      cols="12"
                      class="pa-0"
                      style="height: 1px; width: 100%"
                    >
                      <v-row>
                        <v-col cols="4"> </v-col>
                        <v-col cols="8">
                          <v-row>
                            <v-col cols="2">
                              <v-icon
                                v-if="showText === 'About'"
                                size="50"
                                color="rgb(255, 128, 0)"
                                style="
                                  position: fixed;
                                  z-index: 100;
                                  top: 80px;
                                  width: 50px;
                                  max-width: 100%;
                                  margin-left: 55%;
                                "
                                >mdi-triangle-small-up</v-icon
                              >
                            </v-col>
                            <v-col cols="2">
                              <v-icon
                                v-if="showText == 'Personal'"
                                size="50"
                                color="rgb(255, 128, 0)"
                                style="
                                  bottom: 20%;
                                  width: 50px;
                                  margin-left: 25%;
                                "
                                >mdi-triangle-small-up</v-icon
                              >
                            </v-col>
                            <v-col cols="2">
                              <v-icon
                                v-if="showText == 'Corporate'"
                                size="50"
                                color="rgb(255, 128, 0)"
                                style="bottom: 20%; width: 50px"
                                >mdi-triangle-small-up</v-icon
                              >
                            </v-col>
                            <v-col cols="2">
                              <v-icon
                                v-if="showText == 'Premier'"
                                size="50"
                                color="rgb(255, 128, 0)"
                                style="bottom: 20%; width: 50px; right: 40%"
                                >mdi-triangle-small-up</v-icon
                              >
                            </v-col>
                          </v-row>
                        </v-col>
                      </v-row>
                    </v-col>
                  </v-row>
                </v-col>
              </div>
            </v-col>
          </v-main>
        </v-card>
        <div
          v-if="showText != false"
          style="position: fixed; z-index: 100; width: 100%"
        >
          <v-card
            class="green-background"
            flat
            style="position: relative; background-color: red"
          >
          </v-card>
          <v-card
            class="white-background"
            style="position: relative; z-index: -1"
          >
            <v-card-text>
              <v-container>
                <v-row>
                  <v-col> hhhh </v-col>
                </v-row>
              </v-container>
            </v-card-text>
          </v-card>
        </div>
        <div v-if="buttomdetail" style="position: fixed; z-index: 100; width: 100%">
          <v-list style="background-color: #664283">
            <v-list-group
              v-for="item in items"
              :key="item.title"
              v-model="item.active"
              style="border-bottom: 1px solid #bbb4b4"
              no-action
            >
              <template #activator>
                <v-list-item-content>
                  <v-list-item-title style="color: #fff">{{
                    item.title
                  }}</v-list-item-title>
                </v-list-item-content>
              </template>

              <v-list-item v-for="child in item.items" :key="child.title" style="padding:0px;">
                <v-list-item-content style="background-color: #fff">
                  <v-list-item-title
                    ><v-icon>{{ item.action }}</v-icon
                    >{{ child.title }}</v-list-item-title
                  >
                </v-list-item-content>
              </v-list-item>
            </v-list-group>
          </v-list>
        </div>
      </div>
    </div>

    <main></main>
  </v-card>
</template>
<script>
export default {
  data() {
    return {
      showText: false,
      show: false,
      changecol: false,
      buttomdetail: false,
      items: [
        {
          action: 'mdi-ticket',
          items: [{ title: 'List Item' }],
          title: 'About Indochaina Bank',
        },
        {
          action: 'mdi-silverware-fork-knife',
          active: true,
          items: [
            { title: 'Breakfast & brunch' },
            { title: 'New American' },
            { title: 'Sushi' },
          ],
          title: 'Dining',
        },
        {
          action: 'mdi-school',
          items: [{ title: 'List Item' }],
          title: 'Education',
        },
        {
          action: 'mdi-human-male-female-child',
          items: [{ title: 'List Item' }],
          title: 'Family',
        },
        {
          action: 'mdi-bottle-tonic-plus',
          items: [{ title: 'List Item' }],
          title: 'Health',
        },
        {
          action: 'mdi-briefcase',
          items: [{ title: 'List Item' }],
          title: 'Office',
        },
        {
          action: 'mdi-tag',
          items: [{ title: 'List Item' }],
          title: 'Promotions',
        },
      ],
    }
  },
  mounted() {
    // Update 'show' property on component mount
    this.updateShowProperty()
    this.updateChangecolProperty()
    // Listen for window resize events and update 'show' property accordingly
    window.addEventListener('resize', this.updateShowProperty)
    window.addEventListener('resize', this.updateChangecolProperty)
  },
  beforeDestroy() {
    // Remove the window resize event listener to prevent memory leaks
    window.removeEventListener('resize', this.updateShowProperty)
    window.removeEventListener('resize', this.updateChangecolProperty)
  },
  methods: {
    updateShowProperty() {
      // Update 'show' property based on window width
      this.show = window.innerWidth > 1160
      if (this.show === false) {
        this.showText = false
        this.buttomdetail = false
      }
    },
    updateChangecolProperty() {
      this.changecol = window.innerWidth > 400
    },
  },
}
</script>
<style scoped>
.green-background {
  background-color: green;
  width: 100%;
  height: 1.5vh;
  z-index: 100;
  border-bottom-right-radius: 0%;
  border-bottom-left-radius: 0%;
}
.grid {
  height: 100px; /* Set a fixed height to prevent increase */
  max-height: 100px; /* Add max-height to enforce the fixed height */
  overflow: hidden;
}
@media (max-width: 389px) {
  .iconend {
    justify-content: flex-start !important;
  }
}
@media (max-width: 500px) {
}
</style>