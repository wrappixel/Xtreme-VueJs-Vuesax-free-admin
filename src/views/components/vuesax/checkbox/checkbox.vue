<template>
  <vs-row vs-justify="center">
    <vs-col type="flex" vs-justify="center" vs-align="center" vs-lg="12" vs-xs="12">
      <!--
        /////////////////
        Checkbox State
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Checkbox State
          <vs-button class="ml-auto p-0" @click="statecheckbox=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          To add a checkBox, we have the
          <code>vs-checkbox</code> component which expects a principal parameter
          <code>v-model</code> that would be our value.
        </p>
        <div class="mb-3">
          <vs-checkbox class="justify-content-start" v-model="checkBox1">Primary - active</vs-checkbox>
        </div>
        <div class="mb-3">
          <vs-checkbox class="justify-content-start" v-model="checkBox2">Primary - inactive</vs-checkbox>
        </div>
        <div class="mb-3">
          <vs-checkbox
            class="justify-content-start"
            disabled="true"
            v-model="checkBox3"
          >Primary - active - disabled</vs-checkbox>
        </div>
        <div>
          <vs-checkbox
            class="justify-content-start"
            disabled="true"
            v-model="checkBox4"
          >Primary - inactive - disabled</vs-checkbox>
        </div>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="statecheckbox">
          <vs-prism>
            &lt;div class=&quot;mb-3&quot;&gt;
            &lt;vs-checkbox class=&quot;justify-content-start&quot; v-model=&quot;checkBox1&quot;&gt;Primary - active&lt;/vs-checkbox&gt;
            &lt;/div&gt;
            &lt;div class=&quot;mb-3&quot;&gt;
            &lt;vs-checkbox class=&quot;justify-content-start&quot; v-model=&quot;checkBox2&quot;&gt;Primary - inactive&lt;/vs-checkbox&gt;
            &lt;/div&gt;
            &lt;div class=&quot;mb-3&quot;&gt;
            &lt;vs-checkbox class=&quot;justify-content-start&quot; disabled=&quot;true&quot; v-model=&quot;checkBox3&quot;&gt;Primary - active - disabled&lt;/vs-checkbox&gt;
            &lt;/div&gt;
            &lt;div&gt;
            &lt;vs-checkbox class=&quot;justify-content-start&quot; disabled=&quot;true&quot; v-model=&quot;checkBox4&quot;&gt;Primary - inactive - disabled&lt;/vs-checkbox&gt;
            &lt;/div&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Checkbox Colors
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Checkbox Colors
          <vs-button class="ml-auto p-0" @click="colorcheckbox=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can change the color of the checkBox with the property
          <code>color</code>. You are able to use the Main Colors or RGB and HEX colors.
        </p>
        <ul class="list-inline mb-0">
          <li class="mb-3 mb-lg-0 list-inline-item">
            <vs-checkbox class="justify-content-start" v-model="checkBox11">Primary</vs-checkbox>
          </li>
          <li class="mb-3 mb-lg-0 list-inline-item">
            <vs-checkbox class="justify-content-start" color="success" v-model="checkBox22">Success</vs-checkbox>
          </li>
          <li class="mb-3 mb-lg-0 list-inline-item">
            <vs-checkbox class="justify-content-start" color="danger" v-model="checkBox33">Danger</vs-checkbox>
          </li>
          <li class="mb-3 mb-lg-0 list-inline-item">
            <vs-checkbox class="justify-content-start" color="warning" v-model="checkBox44">Warning</vs-checkbox>
          </li>
          <li class="mb-3 mb-lg-0 list-inline-item">
            <vs-checkbox class="justify-content-start" color="dark" v-model="checkBox55">Dark</vs-checkbox>
          </li>
          <li class="mb-3 mb-lg-0 list-inline-item">
            <vs-checkbox
              class="justify-content-start"
              color="rgb(38, 187, 174)"
              v-model="checkBox66"
            >Color RGB</vs-checkbox>
          </li>
          <li class="mb-3 mb-lg-0 list-inline-item">
            <vs-checkbox
              class="justify-content-start"
              color="#720ea8"
              v-model="checkBox77"
            >Color HEX</vs-checkbox>
          </li>
        </ul>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="colorcheckbox">
          <vs-prism>
            &lt;ul class=&quot;list-inline&quot;&gt;
            &lt;li class=&quot;mb-3 mb-lg-0 list-inline-item&quot;&gt;
            &lt;vs-checkbox class=&quot;justify-content-start&quot; v-model=&quot;checkBox11&quot;&gt;Primary&lt;/vs-checkbox&gt;
            &lt;/li&gt;
            &lt;li class=&quot;mb-3 mb-lg-0 list-inline-item&quot;&gt;
            &lt;vs-checkbox class=&quot;justify-content-start&quot; color=&quot;success&quot; v-model=&quot;checkBox22&quot;&gt;Success&lt;/vs-checkbox&gt;
            &lt;/li&gt;
            &lt;li class=&quot;mb-3 mb-lg-0 list-inline-item&quot;&gt;
            &lt;vs-checkbox class=&quot;justify-content-start&quot; color=&quot;danger&quot; v-model=&quot;checkBox33&quot;&gt;Danger&lt;/vs-checkbox&gt;
            &lt;/li&gt;
            &lt;li class=&quot;mb-3 mb-lg-0 list-inline-item&quot;&gt;
            &lt;vs-checkbox class=&quot;justify-content-start&quot; color=&quot;warning&quot; v-model=&quot;checkBox44&quot;&gt;Warning&lt;/vs-checkbox&gt;
            &lt;/li&gt;
            &lt;li class=&quot;mb-3 mb-lg-0 list-inline-item&quot;&gt;
            &lt;vs-checkbox class=&quot;justify-content-start&quot; color=&quot;dark&quot; v-model=&quot;checkBox55&quot;&gt;Dark&lt;/vs-checkbox&gt;
            &lt;/li&gt;
            &lt;li class=&quot;mb-3 mb-lg-0 list-inline-item&quot;&gt;
            &lt;vs-checkbox class=&quot;justify-content-start&quot; color=&quot;rgb(38, 187, 174)&quot; v-model=&quot;checkBox66&quot;&gt;Color RGB&lt;/vs-checkbox&gt;
            &lt;/li&gt;
            &lt;li class=&quot;mb-3 mb-lg-0 list-inline-item&quot;&gt;
            &lt;vs-checkbox class=&quot;justify-content-start&quot; color=&quot;#720ea8&quot; v-model=&quot;checkBox77&quot;&gt;Color HEX&lt;/vs-checkbox&gt;
            &lt;/li&gt;
            &lt;/ul&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Checkbox Boolean Value
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Checkbox Boolean Value
          <vs-button class="ml-auto p-0" @click="booleancheckbox=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          In most cases you will need a boolean data type while working with checkBoxes. For making this possible you have to link a boolean value in
          <code>v-model</code>.
        </p>
        <ul class="list-inline mb-0">
          <li class="list-inline-item">
            <vs-checkbox v-model="checkBoxone">{{checkBox1}}</vs-checkbox>
          </li>
          <li class="list-inline-item">
            <vs-checkbox v-model="checkBoxtwo">{{checkBox2}}</vs-checkbox>
          </li>
        </ul>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="booleancheckbox">
          <vs-prism>
            &lt;ul class=&quot;list-inline mb-0&quot;&gt;
            &lt;li class=&quot;list-inline-item&quot;&gt;
            &lt;vs-checkbox v-model=&quot;checkBoxone&quot;&gt;{{checkBox1}}&lt;/vs-checkbox&gt;
            &lt;/li&gt;
            &lt;li class=&quot;list-inline-item&quot;&gt;
            &lt;vs-checkbox v-model=&quot;checkBoxtwo&quot;&gt;{{checkBox2}}&lt;/vs-checkbox&gt;
            &lt;/li&gt;
            &lt;/ul&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Checkbox String Value
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Checkbox String Value
          <vs-button class="ml-auto p-0" @click="stringcheckbox=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can pass as a value a string by giving it as a value of the property
          <code>vs-value</code>.
        </p>
        <ul class="ul list-inline mb-0 d-flex align-items-center">
          <li
            class="modelx list-inline-item p-2 shadow border-bottom border-primary"
          >{{checkBoxOne==null?'null':checkBoxOne}}</li>
          <li class="list-inline-item">
            <vs-checkbox v-model="checkBoxOne" vs-value="Luis Daniel">Luis Daniel</vs-checkbox>
          </li>
        </ul>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="stringcheckbox">
          <vs-prism>
            &lt;ul class=&quot;ul list-inline mb-0 d-flex align-items-center&quot;&gt;
            &lt;li class=&quot;modelx list-inline-item p-2 shadow border-bottom border-primary&quot;&gt;
            {{checkBoxOne==null?'null':checkBoxOne}}
            &lt;/li&gt;
            &lt;li class=&quot;list-inline-item&quot;&gt;
            &lt;vs-checkbox v-model=&quot;checkBoxOne&quot; vs-value=&quot;Luis Daniel&quot; &gt;Luis Daniel&lt;/vs-checkbox&gt;
            &lt;/li&gt;
            &lt;/ul&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Checkbox Array Values
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Checkbox Array Values
          <vs-button class="ml-auto p-0" @click="arraycheckbox=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can pass as a value a string by giving it as a value of the property
          <code>vs-value</code>.
        </p>
        <ul class="list-inline mb-0 list-alignment d-inline-block d-lg-flex align-items-center">
          <li class="list-inline-item shadow border-bottom border-primary pb-2 px-3">{{checkarray1}}</li>
          <li class="list-inline-item">
            <vs-checkbox v-model="checkarray1" vs-value="luis">Luis</vs-checkbox>
          </li>
          <li class="list-inline-item">
            <vs-checkbox v-model="checkarray1" vs-value="carols">Carols</vs-checkbox>
          </li>
          <li class="list-inline-item">
            <vs-checkbox v-model="checkarray1" vs-value="summer">Summer</vs-checkbox>
          </li>
          <li class="list-inline-item">
            <vs-checkbox v-model="checkarray1" vs-value="lyon">Lyon</vs-checkbox>
          </li>
        </ul>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="arraycheckbox">
          <vs-prism>
            &lt;ul class=&quot;list-inline mb-0 list-alignment d-inline-block d-lg-flex align-items-center&quot;&gt;
            &lt;li class=&quot;list-inline-item shadow border-bottom border-primary pb-2 px-3&quot;&gt;
            {{checkarray1}}
            &lt;/li&gt;
            &lt;li class=&quot;list-inline-item&quot;&gt;
            &lt;vs-checkbox v-model=&quot;checkarray1&quot; vs-value=&quot;luis&quot;&gt;Luis&lt;/vs-checkbox&gt;
            &lt;/li&gt;
            &lt;li class=&quot;list-inline-item&quot;&gt;
            &lt;vs-checkbox v-model=&quot;checkarray1&quot; vs-value=&quot;carols&quot;&gt;Carols&lt;/vs-checkbox&gt;
            &lt;/li&gt;
            &lt;li class=&quot;list-inline-item&quot;&gt;
            &lt;vs-checkbox v-model=&quot;checkarray1&quot; vs-value=&quot;summer&quot;&gt;Summer&lt;/vs-checkbox&gt;
            &lt;/li&gt;
            &lt;li class=&quot;list-inline-item&quot;&gt;
            &lt;vs-checkbox v-model=&quot;checkarray1&quot; vs-value=&quot;lyon&quot;&gt;Lyon&lt;/vs-checkbox&gt;
            &lt;/li&gt;
            &lt;/ul&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Checkbox Change Icon
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Checkbox Change Icon
          <vs-button class="ml-auto p-0" @click="iconcheckbox=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          Sometimes we want to change the internal icon inside the checkbox. To do so, we have the property
          <code>icon</code>.
        </p>
        <ul class="list-inline mb-0 list-alignment d-inline-block d-lg-flex align-items-center">
          <li class="list-inline-item">
            <vs-checkbox v-model="checkicon1">Primary</vs-checkbox>
          </li>
          <li class="list-inline-item">
            <vs-checkbox icon="sms" color="success" v-model="checkicon2">SMS</vs-checkbox>
          </li>
          <li class="list-inline-item">
            <vs-checkbox icon="close" color="danger" v-model="checkicon3">Cancel</vs-checkbox>
          </li>
          <li class="list-inline-item">
            <vs-checkbox icon="attach_file" color="warning" v-model="checkicon4">File</vs-checkbox>
          </li>
          <li class="list-inline-item">
            <vs-checkbox icon="format_bold" color="dark" v-model="checkicon5">Bold</vs-checkbox>
          </li>
          <li class="list-inline-item">
            <vs-checkbox
              icon="location_searching"
              color="rgb(38, 187, 174)"
              v-model="checkicon6"
            >Location</vs-checkbox>
          </li>
          <li class="list-inline-item">
            <vs-checkbox icon="camera_alt" color="#720ea8" v-model="checkicon7">Camera</vs-checkbox>
          </li>
        </ul>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="iconcheckbox">
          <vs-prism>
            &lt;ul class=&quot;list-inline mb-0 list-alignment d-inline-block d-lg-flex align-items-center&quot;&gt;
            &lt;li class=&quot;list-inline-item&quot;&gt;
            &lt;vs-checkbox v-model=&quot;checkicon1&quot;&gt;Primary&lt;/vs-checkbox&gt;
            &lt;/li&gt;
            &lt;li class=&quot;list-inline-item&quot;&gt;
            &lt;vs-checkbox icon=&quot;sms&quot; color=&quot;success&quot; v-model=&quot;checkicon2&quot;&gt;SMS&lt;/vs-checkbox&gt;
            &lt;/li&gt;
            &lt;li class=&quot;list-inline-item&quot;&gt;
            &lt;vs-checkbox icon=&quot;close&quot; color=&quot;danger&quot; v-model=&quot;checkicon3&quot;&gt;Cancel&lt;/vs-checkbox&gt;
            &lt;/li&gt;
            &lt;li class=&quot;list-inline-item&quot;&gt;
            &lt;vs-checkbox icon=&quot;attach_file&quot; color=&quot;warning&quot; v-model=&quot;checkicon4&quot;&gt;File&lt;/vs-checkbox&gt;
            &lt;/li&gt;
            &lt;li class=&quot;list-inline-item&quot;&gt;
            &lt;vs-checkbox icon=&quot;format_bold&quot; color=&quot;dark&quot; v-model=&quot;checkicon5&quot;&gt;Bold&lt;/vs-checkbox&gt;
            &lt;/li&gt;
            &lt;li class=&quot;list-inline-item&quot;&gt;
            &lt;vs-checkbox icon=&quot;location_searching&quot; color=&quot;rgb(38, 187, 174)&quot; v-model=&quot;checkicon6&quot;&gt;Location&lt;/vs-checkbox&gt;
            &lt;/li&gt;
            &lt;li class=&quot;list-inline-item&quot;&gt;
            &lt;vs-checkbox icon=&quot;camera_alt&quot; color=&quot;#720ea8&quot; v-model=&quot;checkicon7&quot;&gt;Camera&lt;/vs-checkbox&gt;
            &lt;/li&gt;
            &lt;/ul&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>
    </vs-col>
  </vs-row>
</template>

<script>
export default {
  name: "checkbox",
  data: () => ({
    title: "Checkbox",
    statecheckbox: false,
    checkBox1: true,
    checkBox2: false,
    checkBox3: true,
    checkBox4: false,
    colorcheckbox: false,
    checkBox11: true,
    checkBox22: true,
    checkBox33: true,
    checkBox44: true,
    checkBox55: true,
    checkBox66: true,
    checkBox77: true,
    booleancheckbox: false,
    checkBoxtwo: true,
    checkBoxone: false,
    stringcheckbox: false,
    checkBoxOne: null,
    arraycheckbox: false,
    checkarray1: ["luis"],
    iconcheckbox: false,
    checkicon1: true,
    checkicon2: true,
    checkicon3: true,
    checkicon4: true,
    checkicon5: true,
    checkicon6: true,
    checkicon7: true
  })
};
</script>


