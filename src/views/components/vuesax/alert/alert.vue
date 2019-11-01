<template>
  <vs-row vs-justify="center">
    <vs-col type="flex" vs-justify="center" vs-align="center" vs-lg="12" vs-xs="12">
      <!--
        /////////////////
        Default alert
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Default Alert
          <vs-button class="ml-auto p-0" @click="defaultalert=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          To add a notification use the
          <code>vs-alert</code> component. For the main parameter, pass the
          <code>active</code> property that determines if the alert is visible or not.
        </p>
        <vs-alert
          active="true"
        >Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat</vs-alert>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="defaultalert">
          <vs-prism>
            &lt;vs-alert active=&quot;true&quot;&gt;
            Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut
            &lt;/vs-alert&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>
      <!--
        /////////////////
        Title alert
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Title Alert
          <vs-button class="ml-auto p-0" @click="titlealert=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          Add a title to the alert with the property
          <code>title</code>.
        </p>
        <vs-alert
          title="Lorem ipsum dolor sit amet"
          color="rgb(231, 154, 23)"
          active="true"
        >Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat</vs-alert>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="titlealert">
          <vs-prism>
            &lt;vs-alert title=&quot;Lorem ipsum dolor sit amet&quot; color=&quot;rgb(231, 154, 23)&quot; active=&quot;true&quot;&gt;
            Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat
            &lt;/vs-alert&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>
      <!--
        /////////////////
        Color alert
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Color Alert
          <vs-button class="ml-auto p-0" @click="coloralert=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can change the color of the alert with the property
          <code>color</code>. You are able to use the Main Colors or RGB and HEX colors.
        </p>
        <vs-alert
          color="primary"
          title="Primary"
          active="true"
          class="mb-3"
        >Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris</vs-alert>
        <vs-alert
          title="Success"
          active="true"
          color="success"
          class="mb-3"
        >Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat</vs-alert>
        <vs-alert
          title="Danger"
          active="true"
          color="danger"
          class="mb-3"
        >Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</vs-alert>
        <vs-alert
          title="Danger"
          active="true"
          color="warning"
          class="mb-3"
        >Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</vs-alert>
        <vs-alert
          title="Dark"
          active="true"
          color="dark"
          class="mb-3"
        >Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat</vs-alert>
        <vs-alert
          title="RGB"
          active="true"
          color="rgb(41, 147, 138)"
          class="mb-3"
        >Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat</vs-alert>
        <vs-alert
          title="HEX"
          active="true"
          color="#842993"
        >Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat</vs-alert>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="coloralert">
          <vs-prism>
            &lt;vs-alert color=&quot;primary&quot; title=&quot;Primary&quot; active=&quot;true&quot; class=&quot;mb-3&quot;&gt;
            Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris
            &lt;/vs-alert&gt;
            &lt;vs-alert title=&quot;Success&quot; active=&quot;true&quot; color=&quot;success&quot; class=&quot;mb-3&quot;&gt;
            Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat
            &lt;/vs-alert&gt;
            &lt;vs-alert title=&quot;Danger&quot; active=&quot;true&quot; color=&quot;danger&quot; class=&quot;mb-3&quot;&gt;
            Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
            &lt;/vs-alert&gt;
            &lt;vs-alert title=&quot;Danger&quot; active=&quot;true&quot; color=&quot;warning&quot; class=&quot;mb-3&quot;&gt;
            Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
            &lt;/vs-alert&gt;
            &lt;vs-alert title=&quot;Dark&quot; active=&quot;true&quot; color=&quot;dark&quot; class=&quot;mb-3&quot;&gt;
            Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat
            &lt;/vs-alert&gt;
            &lt;vs-alert title=&quot;RGB&quot; active=&quot;true&quot; color=&quot;rgb(41, 147, 138)&quot; class=&quot;mb-3&quot;&gt;
            Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat
            &lt;/vs-alert&gt;
            &lt;vs-alert title=&quot;HEX&quot; active=&quot;true&quot; color=&quot;#842993&quot;&gt;
            Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat
            &lt;/vs-alert&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>
      <!--
        /////////////////
        Closable alert
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Closable Alert
          <vs-button class="ml-auto p-0" @click="closablealert=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can show and hide the alert by means of
          <code>active.sync</code> and a Boolean bind as value. The property to determine if the alert can be closed is
          <code>closable</code>.
        </p>
        <div class="centerx">
          <vs-button
            @click="active1=!active1"
            color="primary"
            type="filled"
          >{{!active1?'Open Alert':'Close Alert'}}</vs-button>
          <vs-alert
            :active.sync="active1"
            closable
            close-icon="close"
          >Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat</vs-alert>
        </div>
        <p
          class="card-subtitle mt-3"
        >You can also change the icon used for the close buton on the alerts.</p>
        <div class="centerx">
          <vs-button
            @click="active2=!active2"
            color="primary"
            type="filled"
          >{{!active2?'Open Alert':'Close Alert'}}</vs-button>
          <vs-alert :active.sync="active2" closable close-icon="cancel">
            Lorem ip
            sum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat
          </vs-alert>
        </div>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="closablealert">
          <vs-prism>
            &lt;div class=&quot;centerx&quot;&gt;
            &lt;vs-button @click=&quot;active1=!active1&quot; color=&quot;primary&quot; type=&quot;filled&quot;&gt;{{!active1?'Open Alert':'Close Alert'}}&lt;/vs-button&gt;
            &lt;vs-alert
            :active.sync=&quot;active1&quot;
            closable
            close-icon=&quot;close&quot;&gt;
            Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat
            &lt;/vs-alert&gt;
            &lt;/div&gt;
            &lt;div class=&quot;centerx&quot;&gt;
            &lt;vs-button @click=&quot;active2=!active2&quot; color=&quot;primary&quot; type=&quot;filled&quot;&gt;{{!active2?'Open Alert':'Close Alert'}}&lt;/vs-button&gt;
            &lt;vs-alert
            :active.sync=&quot;active2&quot;
            closable
            close-icon=&quot;cancel&quot;&gt;
            Lorem ip
            sum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat
            &lt;/vs-alert&gt;
            &lt;/div&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>
      <!--
        /////////////////
        Example Use of alert
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Example Use of Alert
          <vs-button class="ml-auto p-0" @click="examplealert=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          An example would be to have an input and when a condition is met show the
          <code>vs-alert</code>.
        </p>
        <div class="centerx default-input">
          <vs-input
            class="inputx mb-3"
            vs-label="Enter only numbers"
            placeholder="0123456789"
            v-model="value1"
          />
          <vs-alert :active="inputValid" color="danger" icon="new_releases">
            <span>
              the value is
              <b>invalid</b> you can only enter numbers
            </span>
          </vs-alert>
        </div>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="examplealert">
          <vs-prism>
            &lt;div class=&quot;centerx&quot;&gt;
            &lt;input vs-label=&quot;Enter only numbers&quot; vs-placeholder=&quot;0123456789&quot; v-model=&quot;value1&quot;/&gt;
            &lt;vs-alert :active=&quot;inputValid&quot; color=&quot;danger&quot; icon=&quot;new_releases&quot; &gt;
            &lt;span&gt;the value is &lt;b&gt;invalid&lt;/b&gt; you can only enter numbers&lt;/span&gt;
            &lt;/vs-alert&gt;
            &lt;/div&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>
    </vs-col>
  </vs-row>
</template>

<script>
export default {
  name: "alert",
  data: () => ({
    title: "Alert",
    defaultalert: false,
    titlealert: false,
    coloralert: false,
    closablealert: false,
    active1: true,
    active2: true,
    examplealert: false,
    value1: ""
  }),
  computed: {
    inputValid() {
      if (/^\d+$/.test(this.value1)) {
        return false;
      } else {
        return true;
      }
    }
  }
};
</script>


