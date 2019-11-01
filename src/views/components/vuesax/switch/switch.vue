<template>
  <vs-row vs-justify="center">
    <vs-col type="flex" vs-justify="center" vs-align="center" vs-lg="12" vs-xs="12">
      <!--
		/////////////////
		Default Switch
		/////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Default Switch
          <vs-button class="ml-auto p-0" @click="defaultswitch=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          To implement a switch element in the application, we add the component
          <code>vs-switch</code>.
        </p>

        <ul class="list-group list-group-horizontal-lg con-s">
          <li
            class="list-group-item rounded-0 py-2 list-group-item rounded-0 py-2 d-flex align-items-center"
          >
            <label for class="mr-2 mb-0">true / active</label>
            <vs-switch v-model="switch1" />
          </li>
          <li
            class="list-group-item rounded-0 py-2 list-group-item rounded-0 py-2 d-flex align-items-center"
          >
            <label for class="mr-2 mb-0">false / inactive</label>
            <vs-switch v-model="switch2" />
          </li>
          <li
            class="list-group-item rounded-0 py-2 list-group-item rounded-0 py-2 d-flex align-items-center"
          >
            <label for class="mr-2 mb-0">disabled / active</label>
            <vs-switch disabled="true" v-model="switch3" />
          </li>
          <li
            class="list-group-item rounded-0 py-2 list-group-item rounded-0 py-2 d-flex align-items-center"
          >
            <label for class="mr-2 mb-0">disabled / inactive</label>
            <vs-switch disabled="true" v-model="switch4" />
          </li>
        </ul>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="defaultswitch">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;ul class=&quot;con-s&quot;&gt;
            &lt;li&gt;
            &lt;label for=&quot;&quot;&gt;true / active&lt;/label&gt;
            &lt;vs-switch v-model=&quot;switch1&quot;/&gt;
            &lt;/li&gt;
            &lt;li&gt;
            &lt;label for=&quot;&quot;&gt;false / inactive&lt;/label&gt;
            &lt;vs-switch v-model=&quot;switch2&quot;/&gt;
            &lt;/li&gt;
            &lt;li&gt;
            &lt;label for=&quot;&quot;&gt;disabled / active&lt;/label&gt;
            &lt;vs-switch disabled=&quot;true&quot; v-model=&quot;switch3&quot;/&gt;
            &lt;/li&gt;
            &lt;li&gt;
            &lt;label for=&quot;&quot;&gt;disabled / inactive&lt;/label&gt;
            &lt;vs-switch disabled=&quot;true&quot; v-model=&quot;switch4&quot;/&gt;
            &lt;/li&gt;
            &lt;/ul&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            data(){
            return {
            switch1:true,
            switch2:false,
            switch3:true,
            switch4:false,
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
        Color Switch
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Color Switch
          <vs-button class="ml-auto p-0" @click="colorswitch=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p
          class="card-subtitle"
        >You can choose the default Switch. You are able to use the Main Colors or RGB and HEX colors.</p>

        <ul class="list-group list-group-horizontal-lg con-s">
          <li
            class="list-group-item rounded-0 py-2 list-group-item rounded-0 py-2 d-flex align-items-center"
          >
            <label for class="mr-2 mb-0">Primary</label>
            <vs-switch v-model="color1" />
          </li>
          <li
            class="list-group-item rounded-0 py-2 list-group-item rounded-0 py-2 d-flex align-items-center"
          >
            <label for class="mr-2 mb-0">Success</label>
            <vs-switch color="success" v-model="color2" />
          </li>
          <li
            class="list-group-item rounded-0 py-2 list-group-item rounded-0 py-2 d-flex align-items-center"
          >
            <label for class="mr-2 mb-0">Danger</label>
            <vs-switch color="danger" v-model="color3" />
          </li>
          <li
            class="list-group-item rounded-0 py-2 list-group-item rounded-0 py-2 d-flex align-items-center"
          >
            <label for class="mr-2 mb-0">Warning</label>
            <vs-switch color="warning" v-model="color4" />
          </li>
          <li
            class="list-group-item rounded-0 py-2 list-group-item rounded-0 py-2 d-flex align-items-center"
          >
            <label for class="mr-2 mb-0">Dark</label>
            <vs-switch color="Dark" v-model="color5" />
          </li>
          <li
            class="list-group-item rounded-0 py-2 list-group-item rounded-0 py-2 d-flex align-items-center"
          >
            <label for class="mr-2 mb-0">
              Color:
              <span>{{color}}</span>
            </label>
            <input v-model="color" type="color" class="mr-2" />
            <vs-switch :color="color" v-model="color6" />
          </li>
        </ul>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="colorswitch">
          <vs-prism>
            &lt;ul class=&quot;list-group list-group-horizontal-lg con-s&quot;&gt;
            &lt;li class=&quot;list-group-item rounded-0 py-2 list-group-item rounded-0 py-2 d-flex align-items-center&quot;&gt;
            &lt;label for=&quot;&quot; class=&quot;mr-2 mb-0&quot;&gt;Primary&lt;/label&gt;
            &lt;vs-switch v-model=&quot;color1&quot;/&gt;
            &lt;/li&gt;
            &lt;li class=&quot;list-group-item rounded-0 py-2 list-group-item rounded-0 py-2 d-flex align-items-center&quot;&gt;
            &lt;label for=&quot;&quot; class=&quot;mr-2 mb-0&quot;&gt;Success&lt;/label&gt;
            &lt;vs-switch color=&quot;success&quot; v-model=&quot;color2&quot;/&gt;
            &lt;/li&gt;
            &lt;li class=&quot;list-group-item rounded-0 py-2 list-group-item rounded-0 py-2 d-flex align-items-center&quot;&gt;
            &lt;label for=&quot;&quot; class=&quot;mr-2 mb-0&quot;&gt;Danger&lt;/label&gt;
            &lt;vs-switch color=&quot;danger&quot; v-model=&quot;color3&quot;/&gt;
            &lt;/li&gt;
            &lt;li class=&quot;list-group-item rounded-0 py-2 list-group-item rounded-0 py-2 d-flex align-items-center&quot;&gt;
            &lt;label for=&quot;&quot; class=&quot;mr-2 mb-0&quot;&gt;Warning&lt;/label&gt;
            &lt;vs-switch color=&quot;warning&quot; v-model=&quot;color4&quot;/&gt;
            &lt;/li&gt;
            &lt;li class=&quot;list-group-item rounded-0 py-2 list-group-item rounded-0 py-2 d-flex align-items-center&quot;&gt;
            &lt;label for=&quot;&quot; class=&quot;mr-2 mb-0&quot;&gt;Dark&lt;/label&gt;
            &lt;vs-switch color=&quot;Dark&quot; v-model=&quot;color5&quot;/&gt;
            &lt;/li&gt;
            &lt;li class=&quot;list-group-item rounded-0 py-2 list-group-item rounded-0 py-2 d-flex align-items-center&quot;&gt;
            &lt;label for=&quot;&quot; class=&quot;mr-2 mb-0&quot;&gt;Color: &lt;span&gt;{{color}}&lt;/span&gt;&lt;/label&gt;
            &lt;input v-model=&quot;color&quot; type=&quot;color&quot; class=&quot;mr-2&quot;&gt;
            &lt;vs-switch :color=&quot;color&quot; v-model=&quot;color6&quot;/&gt;
            &lt;/li&gt;
            &lt;/ul&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Text Switch
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Text Switch
          <vs-button class="ml-auto p-0" @click="textswitch=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can add a descriptive text with the slot
          <code>on</code> or
          <code>off</code>. You can also join the text with the icons.
        </p>

        <ul class="list-group list-group-horizontal-lg con-s">
          <li
            class="list-group-item rounded-0 py-2 list-group-item rounded-0 py-2 d-flex align-items-center"
          >
            <vs-switch v-model="text1">
              <span slot="on">On</span>
              <span slot="off">Off</span>
            </vs-switch>
          </li>
          <li
            class="list-group-item rounded-0 py-2 list-group-item rounded-0 py-2 d-flex align-items-center"
          >
            <vs-switch color="success" v-model="text2">
              <span slot="on">Accept</span>
              <span slot="off">Cancel</span>
            </vs-switch>
          </li>
          <li
            class="list-group-item rounded-0 py-2 list-group-item rounded-0 py-2 d-flex align-items-center"
          >
            <vs-switch color="danger" vs-icon-off="close" v-model="text3">
              <span slot="on">Remove</span>
            </vs-switch>
          </li>
          <li
            class="list-group-item rounded-0 py-2 list-group-item rounded-0 py-2 d-flex align-items-center"
          >
            <vs-switch color="warning" vs-icon-on="error_outline" v-model="text4">
              <span slot="off">Prevent</span>
            </vs-switch>
          </li>
          <li
            class="list-group-item rounded-0 py-2 list-group-item rounded-0 py-2 d-flex align-items-center"
          >
            <vs-switch color="dark" vs-icon-on="check_box" vs-icon-off="block" v-model="text5">
              <span slot="on">YES</span>
              <span slot="off">NO</span>
            </vs-switch>
          </li>
        </ul>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="textswitch">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;div class=&quot;centex&quot;&gt;
            &lt;vs-switch v-model=&quot;switch1&quot;&gt;
            &lt;span slot=&quot;on&quot;&gt;On&lt;/span&gt;
            &lt;span slot=&quot;off&quot;&gt;Off&lt;/span&gt;
            &lt;/vs-switch&gt;
            &lt;vs-switch color=&quot;success&quot; v-model=&quot;switch2&quot;&gt;
            &lt;span slot=&quot;on&quot;&gt;Accept&lt;/span&gt;
            &lt;span slot=&quot;off&quot;&gt;Cancel&lt;/span&gt;
            &lt;/vs-switch&gt;
            &lt;vs-switch color=&quot;danger&quot; vs-icon-off=&quot;close&quot; v-model=&quot;switch3&quot;&gt;
            &lt;span slot=&quot;on&quot;&gt;Remove&lt;/span&gt;
            &lt;/vs-switch&gt;
            &lt;vs-switch color=&quot;warning&quot; vs-icon-on=&quot;error_outline&quot; v-model=&quot;switch4&quot;&gt;
            &lt;span slot=&quot;off&quot;&gt;Prevent&lt;/span&gt;
            &lt;/vs-switch&gt;
            &lt;vs-switch color=&quot;dark&quot; vs-icon-on=&quot;check_box&quot; vs-icon-off=&quot;block&quot; v-model=&quot;switch5&quot;&gt;
            &lt;span slot=&quot;on&quot;&gt;YES&lt;/span&gt;
            &lt;span slot=&quot;off&quot;&gt;NO&lt;/span&gt;
            &lt;/vs-switch&gt;
            &lt;/div&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            data(){
            return {
            switch1:true,
            switch2:true,
            switch3:true,
            switch4:true,
            switch5:true,
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
        Icons Switch
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Icon Switch
          <vs-button class="ml-auto p-0" @click="iconswitch=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          We can add a representative icon inside our switch with the property
          <code>vs-icon</code>. If you only need to add the icon in one of the states you can do it with the property
          <code>vs-icon-on</code> or
          <code>vs-icon-off</code>
        </p>

        <ul class="list-group list-group-horizontal-lg con-s">
          <li
            class="list-group-item rounded-0 py-2 list-group-item rounded-0 py-2 d-flex align-items-center"
          >
            <label for class="mr-2 mb-0">Primary</label>
            <vs-switch v-model="icon1" vs-icon-off="notifications_none" vs-icon-on="done" />
          </li>
          <li
            class="list-group-item rounded-0 py-2 list-group-item rounded-0 py-2 d-flex align-items-center"
          >
            <label for class="mr-2 mb-0">Success</label>
            <vs-switch color="success" v-model="icon2" vs-icon="done" />
          </li>
          <li
            class="list-group-item rounded-0 py-2 list-group-item rounded-0 py-2 d-flex align-items-center"
          >
            <label for class="mr-2 mb-0">Danger</label>
            <vs-switch color="danger" v-model="icon3" vs-icon="close" />
          </li>
          <li
            class="list-group-item rounded-0 py-2 list-group-item rounded-0 py-2 d-flex align-items-center"
          >
            <label for class="mr-2 mb-0">Warning</label>
            <vs-switch color="warning" v-model="icon4" vs-icon="error_outline" />
          </li>
          <li
            class="list-group-item rounded-0 py-2 list-group-item rounded-0 py-2 d-flex align-items-center"
          >
            <label for class="mr-2 mb-0">Dark</label>
            <vs-switch color="dark" v-model="icon5" vs-icon="volume_off" />
          </li>
          <li
            class="list-group-item rounded-0 py-2 list-group-item rounded-0 py-2 d-flex align-items-center"
          >
            <label for class="mr-2 mb-0">rgb(color) / #color</label>
            <vs-switch color="rgb(51, 53, 83)" v-model="icon6" vs-icon="photo_camera" />
          </li>
        </ul>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="iconswitch">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;ul class=&quot;con-s&quot;&gt;
            &lt;li&gt;
            &lt;label for=&quot;&quot;&gt;Primary&lt;/label&gt;
            &lt;vs-switch v-model=&quot;switch1&quot; vs-icon-off=&quot;notifications_none&quot; vs-icon-on=&quot;done&quot;/&gt;
            &lt;/li&gt;
            &lt;li&gt;
            &lt;label for=&quot;&quot;&gt;Success&lt;/label&gt;
            &lt;vs-switch color=&quot;success&quot; v-model=&quot;switch2&quot; vs-icon=&quot;done&quot;/&gt;
            &lt;/li&gt;
            &lt;li&gt;
            &lt;label for=&quot;&quot;&gt;Danger&lt;/label&gt;
            &lt;vs-switch color=&quot;danger&quot; v-model=&quot;switch3&quot; vs-icon=&quot;close&quot;/&gt;
            &lt;/li&gt;
            &lt;li&gt;
            &lt;label for=&quot;&quot;&gt;Warning&lt;/label&gt;
            &lt;vs-switch color=&quot;warning&quot; v-model=&quot;switch4&quot; vs-icon=&quot;error_outline&quot;/&gt;
            &lt;/li&gt;
            &lt;li&gt;
            &lt;label for=&quot;&quot;&gt;Dark&lt;/label&gt;
            &lt;vs-switch color=&quot;dark&quot; v-model=&quot;switch5&quot; vs-icon=&quot;volume_off&quot;/&gt;
            &lt;/li&gt;
            &lt;li&gt;
            &lt;label for=&quot;&quot;&gt;rgb(color) / #color&lt;/label&gt;
            &lt;vs-switch color=&quot;rgb(51, 53, 83)&quot; v-model=&quot;switch6&quot; vs-icon=&quot;photo_camera&quot;/&gt;
            &lt;/li&gt;
            &lt;/ul&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            data(){
            return {
            switch1:false,
            switch2:false,
            switch3:false,
            switch4:false,
            switch5:false,
            switch6:false
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
        Array Value Switch
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Array Value Switch
          <vs-button class="ml-auto p-0" @click="arrayswitch=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p
          class="card-subtitle"
        >For saving the values in an array, you could simply pass it as a value.</p>

        <div class="d-flex align-items-center">
          <div class="p-3 shadow modelx mb-3 mb-md-0 w-25 font-weight-bold">{{switchArray}}</div>
          <ul class="list-group list-group-horizontal-lg con-s ml-3">
            <li
              class="list-group-item rounded-0 py-2 list-group-item rounded-0 py-2 d-flex align-items-center"
            >
              <vs-switch vs-type="success" v-model="switchArray" vs-value="luis">Luis</vs-switch>
            </li>
            <li
              class="list-group-item rounded-0 py-2 list-group-item rounded-0 py-2 d-flex align-items-center"
            >
              <vs-switch vs-type="success" v-model="switchArray" vs-value="carols">Carols</vs-switch>
            </li>
            <li
              class="list-group-item rounded-0 py-2 list-group-item rounded-0 py-2 d-flex align-items-center"
            >
              <vs-switch vs-type="success" v-model="switchArray" vs-value="summer">Summer</vs-switch>
            </li>
            <li
              class="list-group-item rounded-0 py-2 list-group-item rounded-0 py-2 d-flex align-items-center"
            >
              <vs-switch vs-type="success" v-model="switchArray" vs-value="lyon">Lyon</vs-switch>
            </li>
          </ul>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="arrayswitch">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;ul class=&quot;ul&quot;&gt;
            &lt;li class=&quot;modelx&quot;&gt;
            {{switchArray}}
            &lt;/li&gt;
            &lt;li&gt;
            &lt;vs-switch vs-type=&quot;success&quot; v-model=&quot;switchArray&quot; vs-value=&quot;luis&quot;&gt;Luis&lt;/vs-switch&gt;
            &lt;/li&gt;
            &lt;li&gt;
            &lt;vs-switch vs-type=&quot;success&quot; v-model=&quot;switchArray&quot; vs-value=&quot;carols&quot;&gt;Carols&lt;/vs-switch&gt;
            &lt;/li&gt;
            &lt;li&gt;
            &lt;vs-switch vs-type=&quot;success&quot; v-model=&quot;switchArray&quot; vs-value=&quot;summer&quot;&gt;Summer&lt;/vs-switch&gt;
            &lt;/li&gt;
            &lt;li&gt;
            &lt;vs-switch vs-type=&quot;success&quot; v-model=&quot;switchArray&quot; vs-value=&quot;lyon&quot;&gt;Lyon&lt;/vs-switch&gt;
            &lt;/li&gt;
            &lt;/ul&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            data(){
            return {
            switchArray:['luis'],
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
  name: "switch",
  data: () => ({
    title: "Switch",
    defaultswitch: false,
    switch1: true,
    switch2: false,
    switch3: true,
    switch4: false,
    colorswitch: false,
    color: "#5a3cc4",
    color1: true,
    color2: true,
    color3: true,
    color4: true,
    color5: true,
    color6: true,
    textswitch: false,
    text1: true,
    text2: true,
    text3: true,
    text4: true,
    text5: true,
    iconswitch: false,
    icon1: false,
    icon2: false,
    icon3: false,
    icon4: false,
    icon5: false,
    icon6: false,
    arrayswitch: false,
    switchArray: ["luis"]
  })
};
</script>