<template>
  <vs-row vs-justify="center">
    <vs-col type="flex" vs-justify="center" vs-align="center" vs-lg="12" vs-xs="12">
      <!--
		/////////////////
		Default Radio
		/////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Default Radio
          <vs-button class="ml-auto p-0" @click="defaultradio=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          To implement a radio button you just add the
          <code>vs-radio</code> component and add a
          <code>v-model</code>.
        </p>

        <div class="modelx shadow bg-light w-25 p-3 mb-3 text-center font-weight-bold">{{radios1}}</div>
        <ul class="list-group list-group-horizontal-lg">
          <li class="list-group-item rounded-0 py-2">
            <vs-radio class="mb-0" v-model="radios1" vs-name="radios1" vs-value="luis">Luis</vs-radio>
          </li>
          <li class="list-group-item rounded-0 py-2">
            <vs-radio class="mb-0" v-model="radios1" vs-name="radios1" vs-value="carols">Carols</vs-radio>
          </li>
          <li class="list-group-item rounded-0 py-2">
            <vs-radio class="mb-0" v-model="radios1" vs-name="radios1" vs-value="summer">Summer</vs-radio>
          </li>
          <li class="list-group-item rounded-0 py-2">
            <vs-radio
              class="mb-0"
              disabled="true"
              v-model="radios1"
              vs-name="radios1"
              vs-value="lyon"
            >Lyon - disabled</vs-radio>
          </li>
        </ul>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="defaultradio">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;ul class=&quot;leftx&quot;&gt;
            &lt;li class=&quot;modelx&quot;&gt;
            {{radios1}}
            &lt;/li&gt;
            &lt;li&gt;
            &lt;vs-radio v-model=&quot;radios1&quot; vs-name=&quot;radios1&quot; vs-value=&quot;luis&quot;&gt;Luis&lt;/vs-radio&gt;
            &lt;/li&gt;
            &lt;li&gt;
            &lt;vs-radio v-model=&quot;radios1&quot; vs-name=&quot;radios1&quot; vs-value=&quot;carols&quot;&gt;Carols&lt;/vs-radio&gt;
            &lt;/li&gt;
            &lt;li&gt;
            &lt;vs-radio v-model=&quot;radios1&quot; vs-name=&quot;radios1&quot; vs-value=&quot;summer&quot;&gt;Summer&lt;/vs-radio&gt;
            &lt;/li&gt;
            &lt;li&gt;
            &lt;vs-radio disabled=&quot;true&quot; v-model=&quot;radios1&quot; vs-name=&quot;radios1&quot; vs-value=&quot;lyon&quot;&gt;Lyon - disabled&lt;/vs-radio&gt;
            &lt;/li&gt;
            &lt;/ul&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            data(){
            return {
            radios1:'luis',
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
		Radio Colors
		/////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Radio Colors
          <vs-button class="ml-auto p-0" @click="colorradio=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can change the color with the property
          <code>color</code>. You are able to use the Main Colors or RGB and HEX colors.
        </p>

        <div class="modelx shadow bg-light w-25 p-3 mb-3 text-center font-weight-bold">{{radios2}}</div>
        <ul class="list-group list-group-horizontal-lg">
          <li class="list-group-item rounded-0 py-2">
            <vs-radio class="mb-0" v-model="radios2" vs-value="primary">Primary</vs-radio>
          </li>
          <li class="list-group-item rounded-0 py-2">
            <vs-radio class="mb-0" color="success" v-model="radios2" vs-value="Success">Success</vs-radio>
          </li>
          <li class="list-group-item rounded-0 py-2">
            <vs-radio class="mb-0" color="danger" v-model="radios2" vs-value="Danger">Danger</vs-radio>
          </li>
          <li class="list-group-item rounded-0 py-2">
            <vs-radio class="mb-0" color="warning" v-model="radios2" vs-value="Warning">Warning</vs-radio>
          </li>
          <li class="list-group-item rounded-0 py-2">
            <vs-radio class="mb-0" color="dark" v-model="radios2" vs-value="Dark">Dark</vs-radio>
          </li>
          <li class="list-group-item rounded-0 py-2">
            <vs-radio class="mb-0" color="rgb(87, 251, 187)" v-model="radios2" vs-value="RGB">RGB</vs-radio>
          </li>
          <li class="list-group-item rounded-0 py-2">
            <vs-radio class="mb-0" color="#e48346" v-model="radios2" vs-value="HEX">HEX</vs-radio>
          </li>
        </ul>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="colorradio">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;div class=&quot;&quot;&gt;
            &lt;ul class=&quot;leftx&quot;&gt;
            &lt;li class=&quot;modelx&quot;&gt;
            {{radios2}}
            &lt;/li&gt;
            &lt;li&gt;
            &lt;vs-radio v-model=&quot;radios2&quot; vs-value=&quot;primary&quot;&gt;Primary&lt;/vs-radio&gt;
            &lt;/li&gt;
            &lt;li&gt;
            &lt;vs-radio color=&quot;success&quot; v-model=&quot;radios2&quot; vs-value=&quot;Success&quot;&gt;Success&lt;/vs-radio&gt;
            &lt;/li&gt;
            &lt;li&gt;
            &lt;vs-radio color=&quot;danger&quot; v-model=&quot;radios2&quot; vs-value=&quot;Danger&quot;&gt;Danger&lt;/vs-radio&gt;
            &lt;/li&gt;
            &lt;li&gt;
            &lt;vs-radio color=&quot;warning&quot; v-model=&quot;radios2&quot; vs-value=&quot;Warning&quot;&gt;Warning&lt;/vs-radio&gt;
            &lt;/li&gt;
            &lt;li&gt;
            &lt;vs-radio color=&quot;dark&quot; v-model=&quot;radios2&quot; vs-value=&quot;Dark&quot;&gt;Dark&lt;/vs-radio&gt;
            &lt;/li&gt;
            &lt;li&gt;
            &lt;vs-radio color=&quot;rgb(87, 251, 187)&quot; v-model=&quot;radios2&quot; vs-value=&quot;RGB&quot;&gt;RGB&lt;/vs-radio&gt;
            &lt;/li&gt;
            &lt;li&gt;
            &lt;vs-radio color=&quot;#e48346&quot; v-model=&quot;radios2&quot; vs-value=&quot;HEX&quot;&gt;HEX&lt;/vs-radio&gt;
            &lt;/li&gt;
            &lt;/ul&gt;
            &lt;/div&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            data(){
            return {
            radios2:'primary',
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
  name: "radio",
  data: () => ({
    title: "Radio",
    defaultradio: false,
    radios1: "luis",
    colorradio: false,
    radios2: "primary"
  })
};
</script>

