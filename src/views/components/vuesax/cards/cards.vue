<template>
  <vs-row vs-justify="center">
    <vs-col type="flex" vs-justify="center" vs-align="center" vs-lg="12" vs-xs="12">
      <!--
        /////////////////
        Default Cards
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Default Cards
          <vs-button class="ml-auto p-0" @click="defaultcards=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          To add a card we have the
          <code>vs-card</code> component, for the internal structure we use several slots
          <code>(header, footer, media, ... )</code>
        </p>

        <vs-row vs-justify="center">
          <vs-col type="flex" vs-justify="center" vs-align="center" vs-w="6" vs-sm="12">
            <vs-card>
              <div slot="header">
                <h3>Hello world !</h3>
              </div>
              <div>
                <span>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</span>
              </div>
              <div slot="footer">
                <vs-row vs-justify="flex-end">
                  <vs-button class="mr-2" type="gradient" color="danger" icon="favorite"></vs-button>
                  <vs-button class="mr-2" color="primary" icon="turned_in_not"></vs-button>
                  <vs-button color="rgb(230,230,230)" color-text="rgb(50,50,50)" icon="settings"></vs-button>
                </vs-row>
              </div>
            </vs-card>
          </vs-col>
        </vs-row>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="defaultcards">
          <vs-prism>
            &lt;vs-row vs-justify=&quot;center&quot;&gt;
            &lt;vs-col type=&quot;flex&quot; vs-justify=&quot;center&quot; vs-align=&quot;center&quot; vs-w=&quot;6&quot; vs-sm=&quot;12&quot;&gt;
            &lt;vs-card&gt;
            &lt;div slot=&quot;header&quot;&gt;
            &lt;h3&gt;
            Hello world !
            &lt;/h3&gt;
            &lt;/div&gt;
            &lt;div&gt;
            &lt;span&gt;Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.&lt;/span&gt;
            &lt;/div&gt;
            &lt;div slot=&quot;footer&quot;&gt;
            &lt;vs-row vs-justify=&quot;flex-end&quot;&gt;
            &lt;vs-button class=&quot;mr-2&quot; type=&quot;gradient&quot; color=&quot;danger&quot; icon=&quot;favorite&quot;&gt;&lt;/vs-button&gt;
            &lt;vs-button class=&quot;mr-2&quot; color=&quot;primary&quot; icon=&quot;turned_in_not&quot;&gt;&lt;/vs-button&gt;
            &lt;vs-button color=&quot;rgb(230,230,230)&quot; color-text=&quot;rgb(50,50,50)&quot; icon=&quot;settings&quot;&gt;&lt;/vs-button&gt;
            &lt;/vs-row&gt;
            &lt;/div&gt;
            &lt;/vs-card&gt;
            &lt;/vs-col&gt;
            &lt;/vs-row&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Media Cards
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Media Cards
          <vs-button class="ml-auto p-0" @click="mediacards=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          There are cases in which you need to add an image or video on the card so we have the
          <code>slot="media"</code>
        </p>

        <vs-row vs-justify="center">
          <vs-col type="flex" vs-justify="center" vs-align="center" vs-w="6" vs-sm="12">
            <vs-card class="cardx">
              <div slot="header">
                <h3>Hello world !</h3>
              </div>
              <div slot="media">
                <img src="@/assets/images/big/img1.jpg" />
              </div>
              <div>
                <span>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</span>
              </div>
              <div slot="footer">
                <vs-row vs-justify="flex-end">
                  <vs-button class="mr-2" type="gradient" color="danger" icon="favorite"></vs-button>
                  <vs-button class="mr-2" color="primary" icon="turned_in_not"></vs-button>
                  <vs-button color="rgb(230,230,230)" color-text="rgb(50,50,50)" icon="settings"></vs-button>
                </vs-row>
              </div>
            </vs-card>
          </vs-col>
          <vs-col type="flex" vs-justify="center" vs-align="center" vs-w="6" vs-sm="12">
            <vs-card class="cardx">
              <div slot="header">
                <h3>Hello world !</h3>
              </div>
              <div slot="media">
                <img src="@/assets/images/big/img2.jpg" />
              </div>
              <div>
                <span>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</span>
              </div>
              <div slot="footer">
                <vs-row vs-justify="flex-end">
                  <vs-button class="mr-2" type="gradient" color="danger" icon="favorite"></vs-button>
                  <vs-button class="mr-2" color="primary" icon="turned_in_not"></vs-button>
                  <vs-button color="rgb(230,230,230)" color-text="rgb(50,50,50)" icon="settings"></vs-button>
                </vs-row>
              </div>
            </vs-card>
          </vs-col>
        </vs-row>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="mediacards">
          <vs-prism>
            &lt;vs-row vs-justify=&quot;center&quot;&gt;
            &lt;vs-col type=&quot;flex&quot; vs-justify=&quot;center&quot; vs-align=&quot;center&quot; vs-w=&quot;6&quot; vs-sm=&quot;12&quot;&gt;
            &lt;vs-card class=&quot;cardx&quot;&gt;
            &lt;div slot=&quot;header&quot;&gt;
            &lt;h3&gt;
            Hello world !
            &lt;/h3&gt;
            &lt;/div&gt;
            &lt;div slot=&quot;media&quot;&gt;
            &lt;img src=&quot;@/assets/images/big/img1.jpg&quot;&gt;
            &lt;/div&gt;
            &lt;div&gt;
            &lt;span&gt;Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.&lt;/span&gt;
            &lt;/div&gt;
            &lt;div slot=&quot;footer&quot;&gt;
            &lt;vs-row vs-justify=&quot;flex-end&quot;&gt;
            &lt;vs-button class=&quot;mr-2&quot; type=&quot;gradient&quot; color=&quot;danger&quot; icon=&quot;favorite&quot;&gt;&lt;/vs-button&gt;
            &lt;vs-button class=&quot;mr-2&quot; color=&quot;primary&quot; icon=&quot;turned_in_not&quot;&gt;&lt;/vs-button&gt;
            &lt;vs-button color=&quot;rgb(230,230,230)&quot; color-text=&quot;rgb(50,50,50)&quot; icon=&quot;settings&quot;&gt;&lt;/vs-button&gt;
            &lt;/vs-row&gt;
            &lt;/div&gt;
            &lt;/vs-card&gt;
            &lt;/vs-col&gt;
            &lt;vs-col type=&quot;flex&quot; vs-justify=&quot;center&quot; vs-align=&quot;center&quot; vs-w=&quot;6&quot; vs-sm=&quot;12&quot;&gt;
            &lt;vs-card class=&quot;cardx&quot;&gt;
            &lt;div slot=&quot;header&quot;&gt;
            &lt;h3&gt;
            Hello world !
            &lt;/h3&gt;
            &lt;/div&gt;
            &lt;div slot=&quot;media&quot;&gt;
            &lt;img src=&quot;@/assets/images/big/img2.jpg&quot;&gt;
            &lt;/div&gt;
            &lt;div&gt;
            &lt;span&gt;Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.&lt;/span&gt;
            &lt;/div&gt;
            &lt;div slot=&quot;footer&quot;&gt;
            &lt;vs-row vs-justify=&quot;flex-end&quot;&gt;
            &lt;vs-button class=&quot;mr-2&quot; type=&quot;gradient&quot; color=&quot;danger&quot; icon=&quot;favorite&quot;&gt;&lt;/vs-button&gt;
            &lt;vs-button class=&quot;mr-2&quot; color=&quot;primary&quot; icon=&quot;turned_in_not&quot;&gt;&lt;/vs-button&gt;
            &lt;vs-button color=&quot;rgb(230,230,230)&quot; color-text=&quot;rgb(50,50,50)&quot; icon=&quot;settings&quot;&gt;&lt;/vs-button&gt;
            &lt;/vs-row&gt;
            &lt;/div&gt;
            &lt;/vs-card&gt;
            &lt;/vs-col&gt;
            &lt;/vs-row&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Fixed Height Cards
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Fixed Height Cards
          <vs-button class="ml-auto p-0" @click="fixheightcards=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          If you need to set card with the same height, send the prop
          <code>fixed-height</code> and cards set to 100% of height.
        </p>
        <vs-row vs-justify="center">
          <vs-col type="flex" vs-justify="center" vs-align="center" vs-w="6" vs-sm="12">
            <vs-card class="cardx" fixedHeight>
              <div slot="header">
                <h3>Hello world !</h3>
              </div>
              <div slot="media">
                <img src="@/assets/images/big/img3.jpg" />
              </div>
              <div>
                <span>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</span>
                <span>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</span>
              </div>
              <div slot="footer">
                <vs-row vs-justify="flex-end">
                  <vs-button class="mr-2" type="gradient" color="danger" icon="favorite"></vs-button>
                  <vs-button class="mr-2" color="primary" icon="turned_in_not"></vs-button>
                  <vs-button color="rgb(230,230,230)" color-text="rgb(50,50,50)" icon="settings"></vs-button>
                </vs-row>
              </div>
            </vs-card>
          </vs-col>
          <vs-col type="flex" vs-justify="center" vs-align="center" vs-w="6" vs-sm="12">
            <vs-card class="cardx" fixedHeight>
              <div slot="header">
                <h3>Hello world !</h3>
              </div>
              <div slot="media">
                <img src="@/assets/images/big/img4.jpg" />
              </div>
              <div>
                <span>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</span>
              </div>
              <div slot="footer">
                <vs-row vs-justify="flex-end">
                  <vs-button class="mr-2" type="gradient" color="danger" icon="favorite"></vs-button>
                  <vs-button class="mr-2" color="primary" icon="turned_in_not"></vs-button>
                  <vs-button color="rgb(230,230,230)" color-text="rgb(50,50,50)" icon="settings"></vs-button>
                </vs-row>
              </div>
            </vs-card>
          </vs-col>
        </vs-row>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="fixheightcards">
          <vs-prism>
            &lt;vs-row vs-justify=&quot;center&quot;&gt;
            &lt;vs-col type=&quot;flex&quot; vs-justify=&quot;center&quot; vs-align=&quot;center&quot; vs-w=&quot;6&quot; vs-sm=&quot;12&quot;&gt;
            &lt;vs-card class=&quot;cardx&quot; fixedHeight&gt;
            &lt;div slot=&quot;header&quot;&gt;
            &lt;h3&gt;
            Hello world !
            &lt;/h3&gt;
            &lt;/div&gt;
            &lt;div slot=&quot;media&quot;&gt;
            &lt;img src=&quot;@/assets/images/big/img3.jpg&quot;&gt;
            &lt;/div&gt;
            &lt;div&gt;
            &lt;span&gt;Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.&lt;/span&gt;
            &lt;span&gt;Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.&lt;/span&gt;
            &lt;/div&gt;
            &lt;div slot=&quot;footer&quot;&gt;
            &lt;vs-row vs-justify=&quot;flex-end&quot;&gt;
            &lt;vs-button class=&quot;mr-2&quot; type=&quot;gradient&quot; color=&quot;danger&quot; icon=&quot;favorite&quot;&gt;&lt;/vs-button&gt;
            &lt;vs-button class=&quot;mr-2&quot; color=&quot;primary&quot; icon=&quot;turned_in_not&quot;&gt;&lt;/vs-button&gt;
            &lt;vs-button color=&quot;rgb(230,230,230)&quot; color-text=&quot;rgb(50,50,50)&quot; icon=&quot;settings&quot;&gt;&lt;/vs-button&gt;
            &lt;/vs-row&gt;
            &lt;/div&gt;
            &lt;/vs-card&gt;
            &lt;/vs-col&gt;
            &lt;vs-col type=&quot;flex&quot; vs-justify=&quot;center&quot; vs-align=&quot;center&quot; vs-w=&quot;6&quot; vs-sm=&quot;12&quot;&gt;
            &lt;vs-card class=&quot;cardx&quot; fixedHeight&gt;
            &lt;div slot=&quot;header&quot;&gt;
            &lt;h3&gt;
            Hello world !
            &lt;/h3&gt;
            &lt;/div&gt;
            &lt;div slot=&quot;media&quot;&gt;
            &lt;img src=&quot;@/assets/images/big/img4.jpg&quot;&gt;
            &lt;/div&gt;
            &lt;div&gt;
            &lt;span&gt;Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.&lt;/span&gt;
            &lt;/div&gt;
            &lt;div slot=&quot;footer&quot;&gt;
            &lt;vs-row vs-justify=&quot;flex-end&quot;&gt;
            &lt;vs-button class=&quot;mr-2&quot; type=&quot;gradient&quot; color=&quot;danger&quot; icon=&quot;favorite&quot;&gt;&lt;/vs-button&gt;
            &lt;vs-button class=&quot;mr-2&quot; color=&quot;primary&quot; icon=&quot;turned_in_not&quot;&gt;&lt;/vs-button&gt;
            &lt;vs-button color=&quot;rgb(230,230,230)&quot; color-text=&quot;rgb(50,50,50)&quot; icon=&quot;settings&quot;&gt;&lt;/vs-button&gt;
            &lt;/vs-row&gt;
            &lt;/div&gt;
            &lt;/vs-card&gt;
            &lt;/vs-col&gt;
            &lt;/vs-row&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Hover Cards
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Hover Cards
          <vs-button class="ml-auto p-0" @click="hovercards=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can add hover functionality with the property
          <code>actionable</code>.
        </p>
        <vs-row vs-justify="center">
          <vs-col type="flex" vs-justify="center" vs-align="center" vs-w="6" vs-sm="12">
            <vs-card actionable class="cardx">
              <div slot="header">
                <h3>Hello world !</h3>
              </div>
              <div slot="media">
                <img src="@/assets/images/big/img1.jpg" />
              </div>
              <div>
                <span>Lorem ipsum dolor sit amet, consectetur adipiscing elit</span>
              </div>
              <div slot="footer">
                <vs-row vs-justify="flex-end">
                  <vs-button class="mr-2" color="primary" type="gradient">View</vs-button>
                  <vs-button color="danger" type="gradient">Delete</vs-button>
                </vs-row>
              </div>
            </vs-card>
          </vs-col>
          <vs-col type="flex" vs-justify="center" vs-align="center" vs-w="6" vs-sm="12">
            <vs-card actionable class="cardx">
              <div slot="header">
                <h3>Hello world !</h3>
              </div>
              <div slot="media">
                <img src="@/assets/images/big/img2.jpg" />
              </div>
              <div>
                <span>Lorem ipsum dolor sit amet, consectetur adipiscing elit</span>
              </div>
              <div slot="footer">
                <vs-row vs-justify="flex-end">
                  <vs-button class="mr-2" color="primary" type="gradient">View</vs-button>
                  <vs-button color="danger" type="gradient">Delete</vs-button>
                </vs-row>
              </div>
            </vs-card>
          </vs-col>
        </vs-row>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="hovercards">
          <vs-prism>
            &lt;vs-row vs-justify=&quot;center&quot;&gt;
            &lt;vs-col type=&quot;flex&quot; vs-justify=&quot;center&quot; vs-align=&quot;center&quot; vs-w=&quot;6&quot; vs-sm=&quot;12&quot;&gt;
            &lt;vs-card actionable class=&quot;cardx&quot;&gt;
            &lt;div slot=&quot;header&quot;&gt;
            &lt;h3&gt;
            Hello world !
            &lt;/h3&gt;
            &lt;/div&gt;
            &lt;div slot=&quot;media&quot;&gt;
            &lt;img src=&quot;@/assets/images/big/img1.jpg&quot;&gt;
            &lt;/div&gt;
            &lt;div&gt;
            &lt;span&gt;Lorem ipsum dolor sit amet, consectetur adipiscing elit&lt;/span&gt;
            &lt;/div&gt;
            &lt;div slot=&quot;footer&quot;&gt;
            &lt;vs-row vs-justify=&quot;flex-end&quot;&gt;
            &lt;vs-button class=&quot;mr-2&quot; color=&quot;primary&quot; type=&quot;gradient&quot; &gt;View&lt;/vs-button&gt;
            &lt;vs-button color=&quot;danger&quot; type=&quot;gradient&quot;&gt;Delete&lt;/vs-button&gt;
            &lt;/vs-row&gt;
            &lt;/div&gt;
            &lt;/vs-card&gt;
            &lt;/vs-col&gt;
            &lt;vs-col type=&quot;flex&quot; vs-justify=&quot;center&quot; vs-align=&quot;center&quot; vs-w=&quot;6&quot; vs-sm=&quot;12&quot;&gt;
            &lt;vs-card actionable class=&quot;cardx&quot;&gt;
            &lt;div slot=&quot;header&quot;&gt;
            &lt;h3&gt;
            Hello world !
            &lt;/h3&gt;
            &lt;/div&gt;
            &lt;div slot=&quot;media&quot;&gt;
            &lt;img src=&quot;@/assets/images/big/img2.jpg&quot;&gt;
            &lt;/div&gt;
            &lt;div&gt;
            &lt;span&gt;Lorem ipsum dolor sit amet, consectetur adipiscing elit&lt;/span&gt;
            &lt;/div&gt;
            &lt;div slot=&quot;footer&quot;&gt;
            &lt;vs-row vs-justify=&quot;flex-end&quot;&gt;
            &lt;vs-button class=&quot;mr-2&quot; color=&quot;primary&quot; type=&quot;gradient&quot; &gt;View&lt;/vs-button&gt;
            &lt;vs-button color=&quot;danger&quot; type=&quot;gradient&quot; &gt;Delete&lt;/vs-button&gt;
            &lt;/vs-row&gt;
            &lt;/div&gt;
            &lt;/vs-card&gt;
            &lt;/vs-col&gt;
            &lt;/vs-row&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>
    </vs-col>
  </vs-row>
</template>

<script>
export default {
  name: "cards",
  data: () => ({
    title: "Cards",
    defaultcards: false,
    mediacards: false,
    fixheightcards: false,
    hovercards: false
  })
};
</script>


