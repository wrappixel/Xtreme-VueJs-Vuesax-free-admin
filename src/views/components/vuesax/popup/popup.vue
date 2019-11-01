<template>
  <vs-row vs-justify="center">
    <vs-col type="flex" vs-justify="center" vs-align="center" vs-lg="12" vs-xs="12">
      <!--
		/////////////////
		Default Popup
		/////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Default Popup
          <vs-button class="ml-auto p-0" @click="defaultpopup=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          To implement the popup we have the component
          <code>vs-popup</code>.
        </p>

        <div>
          <vs-button @click="popupActivo=true" color="primary" type="filled">Open Default popup</vs-button>
          <vs-popup class="holamundo" title="Lorem ipsum dolor sit amet" :active.sync="popupActivo">
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
          </vs-popup>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="defaultpopup">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;div class=&quot;centerx&quot;&gt;
            &lt;vs-button @click=&quot;popupActivo=true&quot; color=&quot;primary&quot; type=&quot;border&quot;&gt;Open Default popup&lt;/vs-button&gt;
            &lt;vs-popup class=&quot;holamundo&quot; title=&quot;Lorem ipsum dolor sit amet&quot; :active.sync=&quot;popupActivo&quot;&gt;
            &lt;p&gt;
            Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
            &lt;/p&gt;
            &lt;/vs-popup&gt;
            &lt;/div&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            data(){
            return {
            popupActivo:false,
            }
            }
            }
            &lt;/script&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
		/////////////////
		Inner Popup
		/////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Inner Popup
          <vs-button class="ml-auto p-0" @click="innerpopup=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">You can add one popup inside another.</p>

        <div class>
          <vs-button @click="popupActivo2=true" color="primary" type="filled">Open Popup</vs-button>
          <vs-popup classContent="popup-example" title="Popup Title" :active.sync="popupActivo2">
            <vs-input class="inputx mb-3 w-100" placeholder="Placeholder" v-model="value1" />
            <vs-input disabled class="inputx w-100" placeholder="Disabled" v-model="value2" />

            <p
              class="mt-2"
            >Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut</p>
            <vs-button @click="popupActivo3=true" color="primary" type="filled">Open Inner Popup</vs-button>
            <vs-popup title="Inner popup" :active.sync="popupActivo3">
              <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
            </vs-popup>
          </vs-popup>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="innerpopup">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;div class=&quot;centerx&quot;&gt;
            &lt;vs-button @click=&quot;popupActivo2=true&quot; color=&quot;primary&quot; type=&quot;filled&quot;&gt;Open Popup&lt;/vs-button&gt;
            &lt;vs-popup classContent=&quot;popup-example&quot; title=&quot;Lorem ipsum dolor sit amet&quot; :active.sync=&quot;popupActivo2&quot;&gt;
            &lt;vs-input class=&quot;inputx&quot; placeholder=&quot;Placeholder&quot; v-model=&quot;value1&quot;/&gt;
            &lt;vs-input disabled class=&quot;inputx&quot; placeholder=&quot;Disabled&quot; v-model=&quot;value2&quot;/&gt;
            &lt;p&gt;
            Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut
            &lt;/p&gt;
            &lt;vs-select
            label=&quot;Figuras&quot;
            v-model=&quot;select1&quot;
            &gt;
            &lt;vs-select-item :key=&quot;index&quot; :value=&quot;item.value&quot; :text=&quot;item.text&quot; v-for=&quot;item,index in options1&quot; /&gt;
            &lt;/vs-select&gt;
            &lt;vs-button @click=&quot;popupActivo3=true&quot; color=&quot;primary&quot; type=&quot;filled&quot;&gt;Open Inner Popup&lt;/vs-button&gt;
            &lt;vs-popup title=&quot;Inner popup&quot; :active.sync=&quot;popupActivo3&quot;&gt;
            &lt;p&gt;
            Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
            &lt;br&gt;&lt;br&gt;
            Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
            &lt;br&gt;&lt;br&gt;
            Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
            &lt;/p&gt;
            &lt;/vs-popup&gt;
            &lt;/vs-popup&gt;
            &lt;/div&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            data(){
            return {
            select1:3,
            options1:[
            {text:'IT',value:0},
            {text:'Blade Runner',value:2},
            {text:'Thor Ragnarok',value:3},
            ],
            value1:'',
            value2:'',
            popupActivo2:false,
            popupActivo3:false
            }
            }
            }
            &lt;/script&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
		/////////////////
		Full Screen Popup
		/////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Full Screen Popup
          <vs-button class="ml-auto p-0" @click="fullpopup=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          the popup can be full screen you just have to add the property
          <code>fullscreen</code>.
        </p>

        <div class>
          <vs-button @click="popupActivo4=true" color="primary" type="filled">Open fullscreen popup</vs-button>
          <vs-popup fullscreen title="Fullscreen" :active.sync="popupActivo4">
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
          </vs-popup>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="fullpopup">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;div class=&quot;centerx&quot;&gt;
            &lt;vs-button @click=&quot;popupActivo4=true&quot; color=&quot;danger&quot; type=&quot;border&quot;&gt;Open fullscreen popup&lt;/vs-button&gt;
            &lt;vs-popup fullscreen title=&quot;fullscreen&quot; :active.sync=&quot;popupActivo4&quot;&gt;
            &lt;p&gt;
            Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
            &lt;/p&gt;
            &lt;/vs-popup&gt;
            &lt;/div&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            data(){
            return {
            popupActivo4:false
            }
            }
            }
            &lt;/script&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
		/////////////////
		Background Popup
		/////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Background Popup
          <vs-button class="ml-auto p-0" @click="backpopup=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can change the background of the property with the property
          <code>background-color</code> or if you want to change the color of the popup you can use the property
          <code>background-color-popup</code>
        </p>

        <div class>
          <input v-model="colorx" type="color" class="mr-3" name value />
          <vs-button :color="colorx" @click="popupActivo5=true" type="filled">Open background popup</vs-button>

          <vs-popup
            style="color:rgb(255,255,255)"
            background-color="rgba(255,255,255,.6)"
            :background-color-popup="colorx"
            title="background"
            :active.sync="popupActivo5"
          >
            <p>
              Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
              <br />
              <br />e irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
            </p>
          </vs-popup>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="backpopup">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;div class=&quot;centerx&quot;&gt;
            &lt;input v-model=&quot;colorx&quot; type=&quot;color&quot; name=&quot;&quot; value=&quot;&quot;&gt;
            &lt;vs-button :color=&quot;colorx&quot; @click=&quot;popupActivo5=true&quot; type=&quot;filled&quot;&gt;Open background popup&lt;/vs-button&gt;
            &lt;vs-popup
            style=&quot;color:rgb(255,255,255)&quot;
            background-color=&quot;rgba(255,255,255,.6)&quot;
            :background-color-popup=&quot;colorx&quot; title=&quot;background&quot; :active.sync=&quot;popupActivo5&quot;&gt;
            &lt;p&gt;
            Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
            &lt;br&gt;
            &lt;br&gt;
            e irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
            &lt;/p&gt;
            &lt;/vs-popup&gt;
            &lt;/div&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            data(){
            return {
            colorx:&quot;#4a5153&quot;,
            popupActivo5:false
            }
            }
            }
            &lt;/script&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>
    </vs-col>
  </vs-row>
</template>

<script>
export default {
  name: "popup",
  data: () => ({
    title: "Popup",
    defaultpopup: false,
    popupActivo: false,
    select1: 3,
    options1: [
      { text: "IT", value: 0 },
      { text: "Blade Runner", value: 2 },
      { text: "Thor Ragnarok", value: 3 }
    ],
    value1: "",
    value2: "",
    popupActivo2: false,
    popupActivo3: false,
    innerpopup: false,
    fullpopup: false,
    popupActivo4: false,
    backpopup: false,
    colorx: "#4a5153",
    popupActivo5: false
  })
};
</script>

