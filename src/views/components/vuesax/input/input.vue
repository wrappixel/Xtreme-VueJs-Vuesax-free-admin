<template>
  <vs-row vs-justify="center">
    <vs-col type="flex" vs-justify="center" vs-align="center" vs-lg="12" vs-xs="12">
      <!--
        /////////////////
        Default Inputs
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Default Inputs
          <vs-button class="ml-auto p-0" @click="defaulinputs=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          The input is a functional part in an application, For implementing it we have the
          <code>vs-input</code> component.
        </p>

        <div class="default-input d-flex align-items-center">
          <vs-input class="inputx" placeholder="Placeholder" v-model="value1" />
          <vs-input disabled class="inputx ml-3" placeholder="Disabled" v-model="value2" />
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="defaulinputs">
          <vs-prism>
            &lt;div class=&quot;default-input d-flex align-items-center&quot;&gt;
            &lt;vs-input class=&quot;inputx&quot; placeholder=&quot;Placeholder&quot; v-model=&quot;value1&quot;/&gt;
            &lt;vs-input disabled class=&quot;inputx ml-3&quot; placeholder=&quot;Disabled&quot; v-model=&quot;value2&quot;/&gt;
            &lt;/div&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Input Label
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Input Label
          <vs-button class="ml-auto p-0" @click="inputlabel=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          Add a label to the input with the property
          <code>label</code>.
        </p>

        <div class="default-input d-flex align-items-center">
          <vs-input label="Name" class="inputx" placeholder="Placeholder" v-model="fname" />
          <vs-input
            type="password"
            label="Password"
            class="inputx ml-3"
            placeholder="Password"
            v-model="password"
          />
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="inputlabel">
          <vs-prism>
            &lt;div class=&quot;default-input d-flex align-items-center&quot;&gt;
            &lt;vs-input label=&quot;Name&quot; class=&quot;inputx&quot; placeholder=&quot;Placeholder&quot; v-model=&quot;fname&quot;/&gt;
            &lt;vs-input type=&quot;password&quot; label=&quot;Password&quot; class=&quot;inputx ml-3&quot; placeholder=&quot;Password&quot; v-model=&quot;password&quot;/&gt;
            &lt;/div&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Input Label Placehlder
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Input Label Placehlder
          <vs-button class="ml-auto p-0" @click="inputlabelplace=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          The placeholder can become a label when the input is focused. Use the property
          <code>label-placeholder</code> for making this.
        </p>

        <div class="default-input d-flex align-items-center">
          <vs-input label-placeholder="Label-placeholder" v-model="lp1" />
          <vs-input
            disabled="true"
            class="ml-3"
            label-placeholder="Label-placeholder-disabled"
            v-model="lp2"
          />
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="inputlabelplace">
          <vs-prism>
            &lt;div class=&quot;default-input d-flex align-items-center&quot;&gt;
            &lt;vs-input label-placeholder=&quot;Label-placeholder&quot; v-model=&quot;lp1&quot;/&gt;
            &lt;vs-input disabled=&quot;true&quot; class=&quot;ml-3&quot; label-placeholder=&quot;Label-placeholder-disabled&quot; v-model=&quot;lp2&quot;/&gt;
            &lt;/div&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Input with Icons
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Input with Icons
          <vs-button class="ml-auto p-0" @click="inputicon=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          The input can have icons. Use the property
          <code>icon</code>. You can also also manipulate the icon's position with the property
          <code>icon-after</code>.
        </p>

        <vs-row>
          <vs-col vs-lg="4" vs-xs="12">
            <vs-input icon="search" placeholder="Search" class="mt-0" v-model="inputicon1" />
          </vs-col>
          <vs-col vs-lg="4" vs-xs="12">
            <vs-input
              icon-after="true"
              label-placeholder="icon-after"
              class="mt-3 mt-md-0"
              icon="mode_edit"
              placeholder="Nombre"
              v-model="inputicon2"
            />
          </vs-col>
          <vs-col vs-lg="4" vs-xs="12">
            <vs-input
              icon="add"
              label-placeholder="Label-placeholder"
              class="mt-3 mt-md-0"
              v-model="inputicon3"
            />
          </vs-col>
          <vs-col vs-lg="4" vs-xs="12">
            <vs-input
              icon-after="true"
              icon="shopping_cart"
              class="mt-3"
              label-placeholder="Label-placeholder"
              v-model="inputicon4"
            />
          </vs-col>
          <vs-col vs-lg="4" vs-xs="12">
            <vs-input
              disabled="true"
              icon="error_outline"
              class="mt-3"
              label-placeholder="icon-disabled"
              v-model="inputicon5"
            />
          </vs-col>
          <vs-col vs-lg="4" vs-xs="12">
            <vs-input
              icon-after="true"
              disabled="true"
              class="mt-3"
              icon="email"
              label-placeholder="icon-disabled"
              v-model="inputicon6"
            />
          </vs-col>
          <vs-col vs-lg="4" vs-xs="12">
            <vs-input
              icon-no-border
              icon="account_circle"
              class="mt-3"
              label-placeholder="icon-no-border"
              v-model="inputicon7"
            />
          </vs-col>
        </vs-row>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="inputicon">
          <vs-prism>
            &lt;vs-row&gt;
            &lt;vs-col vs-lg=&quot;4&quot; vs-xs=&quot;12&quot;&gt;
            &lt;vs-input icon=&quot;search&quot; placeholder=&quot;Search&quot; class=&quot;mt-0&quot; v-model=&quot;inputicon1&quot;/&gt;
            &lt;/vs-col&gt;
            &lt;vs-col vs-lg=&quot;4&quot; vs-xs=&quot;12&quot;&gt;
            &lt;vs-input icon-after=&quot;true&quot; label-placeholder=&quot;icon-after&quot; class=&quot;mt-3 mt-md-0&quot; icon=&quot;mode_edit&quot; placeholder=&quot;Nombre&quot; v-model=&quot;inputicon2&quot;/&gt;
            &lt;/vs-col&gt;
            &lt;vs-col vs-lg=&quot;4&quot; vs-xs=&quot;12&quot;&gt;
            &lt;vs-input icon=&quot;add&quot; label-placeholder=&quot;Label-placeholder&quot; class=&quot;mt-3 mt-md-0&quot; v-model=&quot;inputicon3&quot;/&gt;
            &lt;/vs-col&gt;
            &lt;vs-col vs-lg=&quot;4&quot; vs-xs=&quot;12&quot;&gt;
            &lt;vs-input icon-after=&quot;true&quot; icon=&quot;shopping_cart&quot; class=&quot;mt-3&quot; label-placeholder=&quot;Label-placeholder&quot; v-model=&quot;inputicon4&quot;/&gt;
            &lt;/vs-col&gt;
            &lt;vs-col vs-lg=&quot;4&quot; vs-xs=&quot;12&quot;&gt;
            &lt;vs-input disabled=&quot;true&quot; icon=&quot;error_outline&quot; class=&quot;mt-3&quot; label-placeholder=&quot;icon-disabled&quot; v-model=&quot;inputicon5&quot;/&gt;
            &lt;/vs-col&gt;
            &lt;vs-col vs-lg=&quot;4&quot; vs-xs=&quot;12&quot;&gt;
            &lt;vs-input icon-after=&quot;true&quot; disabled=&quot;true&quot; class=&quot;mt-3&quot; icon=&quot;email&quot; label-placeholder=&quot;icon-disabled&quot; v-model=&quot;inputicon6&quot;/&gt;
            &lt;/vs-col&gt;
            &lt;vs-col vs-lg=&quot;4&quot; vs-xs=&quot;12&quot;&gt;
            &lt;vs-input icon-no-border icon=&quot;account_circle&quot; class=&quot;mt-3&quot; label-placeholder=&quot;icon-no-border&quot; v-model=&quot;inputicon7&quot;/&gt;
            &lt;/vs-col&gt;
            &lt;/vs-row&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Input with Colors
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Input with Colors
          <vs-button class="ml-auto p-0" @click="inputcolor=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can change the color of the borders when the focus the input with the property
          <code>color</code>. You are able to use the Main Colors or RGB and HEX colors.
        </p>

        <vs-row>
          <vs-col vs-lg="4" vs-xs="12">
            <vs-input label-placeholder="Default" v-model="colorinput1" />
          </vs-col>
          <vs-col vs-lg="4" vs-xs="12">
            <vs-input color="success" label-placeholder="Success" v-model="colorinput2" />
          </vs-col>
          <vs-col vs-lg="4" vs-xs="12">
            <vs-input color="danger" label-placeholder="Danger" v-model="colorinput3" />
          </vs-col>
          <vs-col vs-lg="4" vs-xs="12">
            <vs-input color="warning" label-placeholder="Warning" v-model="colorinput4" />
          </vs-col>
          <vs-col vs-lg="4" vs-xs="12">
            <vs-input color="dark" label-placeholder="Dark" v-model="colorinput5" />
          </vs-col>
          <vs-col vs-lg="4" vs-xs="12">
            <vs-input
              color="rgb(213, 14, 151)"
              label-placeholder="RGB: rgb(213, 14, 151)"
              v-model="colorinput6"
            />
          </vs-col>
          <vs-col vs-lg="4" vs-xs="12">
            <vs-input color="#11e988" label-placeholder="HEX: #11e988" v-model="colorinput7" />
          </vs-col>
        </vs-row>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="inputcolor">
          <vs-prism>
            &lt;vs-row&gt;
            &lt;vs-col vs-lg=&quot;4&quot; vs-xs=&quot;12&quot;&gt;
            &lt;vs-input label-placeholder=&quot;Default&quot; v-model=&quot;colorinput1&quot;/&gt;
            &lt;/vs-col&gt;
            &lt;vs-col vs-lg=&quot;4&quot; vs-xs=&quot;12&quot;&gt;
            &lt;vs-input color=&quot;success&quot; label-placeholder=&quot;Success&quot; v-model=&quot;colorinput2&quot;/&gt;
            &lt;/vs-col&gt;
            &lt;vs-col vs-lg=&quot;4&quot; vs-xs=&quot;12&quot;&gt;
            &lt;vs-input color=&quot;danger&quot; label-placeholder=&quot;Danger&quot; v-model=&quot;colorinput3&quot;/&gt;
            &lt;/vs-col&gt;
            &lt;vs-col vs-lg=&quot;4&quot; vs-xs=&quot;12&quot;&gt;
            &lt;vs-input color=&quot;warning&quot; label-placeholder=&quot;Warning&quot; v-model=&quot;colorinput4&quot;/&gt;
            &lt;/vs-col&gt;
            &lt;vs-col vs-lg=&quot;4&quot; vs-xs=&quot;12&quot;&gt;
            &lt;vs-input color=&quot;dark&quot; label-placeholder=&quot;Dark&quot; v-model=&quot;colorinput5&quot;/&gt;
            &lt;/vs-col&gt;
            &lt;vs-col vs-lg=&quot;4&quot; vs-xs=&quot;12&quot;&gt;
            &lt;vs-input color=&quot;rgb(213, 14, 151)&quot; label-placeholder=&quot;RGB: rgb(213, 14, 151)&quot; v-model=&quot;colorinput6&quot;/&gt;
            &lt;/vs-col&gt;
            &lt;vs-col vs-lg=&quot;4&quot; vs-xs=&quot;12&quot;&gt;
            &lt;vs-input color=&quot;#11e988&quot; label-placeholder=&quot;HEX: #11e988&quot; v-model=&quot;colorinput7&quot;/&gt;
            &lt;/vs-col&gt;
            &lt;/vs-row&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Input with Validation
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Input with Validation
          <vs-button class="ml-auto p-0" @click="inputvalidation=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can add a state for example of in affirmative response to a validation with
          <code>success</code> and if it is necessary to add a description or help to the user you can do it with the property
          <code>description</code>
        </p>

        <vs-row>
          <vs-col vs-lg="4" vs-xs="12">
            <vs-input
              :success="true"
              success-text="The mail is valid"
              placeholder="Email Success"
              val-icon-success="done"
              v-model="value1"
            />
          </vs-col>
          <vs-col vs-lg="4" vs-xs="12">
            <vs-input
              :danger="true"
              danger-text="The password does not meet the standards"
              placeholder="Password Danger"
              val-icon-danger="clear"
              v-model="value2"
            />
          </vs-col>
          <vs-col vs-lg="4" vs-xs="12">
            <vs-input
              :warning="true"
              warning-text="The entered data could not be verified"
              placeholder="Date Warning"
              val-icon-warning="warning"
              v-model="value3"
            />
          </vs-col>
          <vs-col vs-lg="4" vs-xs="12">
            <vs-input
              description-text="Just enter the first two numbers of your phone"
              placeholder="Phone Description"
              v-model="value4"
            />
          </vs-col>
        </vs-row>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="inputvalidation">
          <vs-prism>
            &lt;vs-row&gt;
            &lt;vs-col vs-lg=&quot;4&quot; vs-xs=&quot;12&quot;&gt;
            &lt;vs-input
            :success=&quot;true&quot;
            success-text=&quot;The mail is valid&quot;
            placeholder=&quot;Email Success&quot;
            val-icon-success=&quot;done&quot;
            v-model=&quot;value1&quot;/&gt;
            &lt;/vs-col&gt;
            &lt;vs-col vs-lg=&quot;4&quot; vs-xs=&quot;12&quot;&gt;
            &lt;vs-input
            :danger=&quot;true&quot;
            danger-text=&quot;The password does not meet the standards&quot;
            placeholder=&quot;Password Danger&quot;
            val-icon-danger=&quot;clear&quot;
            v-model=&quot;value2&quot;/&gt;
            &lt;/vs-col&gt;
            &lt;vs-col vs-lg=&quot;4&quot; vs-xs=&quot;12&quot;&gt;
            &lt;vs-input
            :warning=&quot;true&quot;
            warning-text=&quot;The entered data could not be verified&quot;
            placeholder=&quot;Date Warning&quot;
            val-icon-warning=&quot;warning&quot;
            v-model=&quot;value3&quot;/&gt;
            &lt;/vs-col&gt;
            &lt;vs-col vs-lg=&quot;4&quot; vs-xs=&quot;12&quot;&gt;
            &lt;vs-input
            description-text=&quot;Just enter the first two numbers of your phone&quot;
            placeholder=&quot;Phone Description&quot;
            v-model=&quot;value4&quot;/&gt;
            &lt;/vs-col&gt;
            &lt;/vs-row&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Input with Size
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Input with Size
          <vs-button class="ml-auto p-0" @click="inputsize=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>

        <vs-row>
          <vs-col vs-lg="4" vs-xs="12">
            <vs-input size="large" placeholder="Size large" v-model="inputsize1" />
          </vs-col>
          <vs-col vs-lg="4" vs-xs="12">
            <vs-input size="default" placeholder="Size default" v-model="inputsize2" />
          </vs-col>
          <vs-col vs-lg="4" vs-xs="12">
            <vs-input size="small" placeholder="Size small" v-model="inputsize3" />
          </vs-col>
        </vs-row>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="inputsize">
          <vs-prism>
            &lt;vs-row&gt;
            &lt;vs-col vs-lg=&quot;4&quot; vs-xs=&quot;12&quot;&gt;
            &lt;vs-input size=&quot;large&quot; placeholder=&quot;Size large&quot; v-model=&quot;inputsize1&quot; /&gt;
            &lt;/vs-col&gt;
            &lt;vs-col vs-lg=&quot;4&quot; vs-xs=&quot;12&quot;&gt;
            &lt;vs-input size=&quot;default&quot; placeholder=&quot;Size default&quot; v-model=&quot;inputsize2&quot; /&gt;
            &lt;/vs-col&gt;
            &lt;vs-col vs-lg=&quot;4&quot; vs-xs=&quot;12&quot;&gt;
            &lt;vs-input size=&quot;small&quot; placeholder=&quot;Size small&quot; v-model=&quot;inputsize3&quot; /&gt;
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
  name: "input",
  data: () => ({
    title: "Input",
    defaulinputs: false,
    value1: "",
    value2: "",
    inputlabel: false,
    fname: "",
    password: "",
    inputlabelplace: false,
    lp1: "",
    lp2: "",
    inputicon: false,
    inputicon1: "",
    inputicon2: "",
    inputicon3: "",
    inputicon4: "",
    inputicon5: "",
    inputicon6: "",
    inputicon7: "",
    inputcolor: false,
    colorinput1: "",
    colorinput2: "",
    colorinput3: "",
    colorinput4: "",
    colorinput5: "",
    colorinput6: "",
    colorinput7: "",
    inputvalidation: false,
    inputsize: false,
    inputsize1: "",
    inputsize2: "",
    inputsize3: ""
  })
};
</script>


