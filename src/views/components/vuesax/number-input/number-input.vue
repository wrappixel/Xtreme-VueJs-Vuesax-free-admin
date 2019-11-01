<template>
  <vs-row vs-justify="center">
    <vs-col type="flex" vs-justify="center" vs-align="center" vs-lg="12" vs-xs="12">
      <!--
		/////////////////
		Default Number Input
		/////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Default Number Input
          <vs-button class="ml-auto p-0" @click="defaultnumint=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          If you need to add a component that handles a single number, use the
          <code>component</code> vs-input-number. You can also change the increment and decrement button icons using the properties
          <code>icon-inc</code> and
          <code>icon-dec</code> respectively.
        </p>

        <ul class="list-group list-group-horizontal-lg">
          <li class="list-group-item rounded-0 py-2">
            <vs-input-number class v-model="number" />
          </li>
          <li class="list-group-item rounded-0 py-2">
            <vs-input-number :disabled="true" v-model="number1" />
          </li>
          <li class="list-group-item rounded-0 py-2">
            <vs-input-number v-model="number2" icon-inc="expand_less" icon-dec="expand_more" />
          </li>
        </ul>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="defaultnumint">
          <vs-prism>
            &lt;ul class=&quot;list-group list-group-horizontal-lg&quot;&gt;
            &lt;li class=&quot;list-group-item rounded-0 py-2&quot;&gt;
            &lt;vs-input-number class=&quot;&quot; v-model=&quot;number&quot;/&gt;
            &lt;/li&gt;
            &lt;li class=&quot;list-group-item rounded-0 py-2&quot;&gt;
            &lt;vs-input-number :disabled=&quot;true&quot; v-model=&quot;number1&quot;/&gt;
            &lt;/li&gt;
            &lt;li class=&quot;list-group-item rounded-0 py-2&quot;&gt;
            &lt;vs-input-number v-model=&quot;number2&quot; icon-inc=&quot;expand_less&quot; icon-dec=&quot;expand_more&quot;/&gt;
            &lt;/li&gt;
            &lt;/ul&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
		/////////////////
		Color Number Input
		/////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Color Number Input
          <vs-button class="ml-auto p-0" @click="colornumint=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can change the color of the Input-Number with the property
          <code>color</code>. You are able to use the Main Colors or RGB and HEX colors.
        </p>

        <ul class="list-group list-group-horizontal-lg">
          <li class="list-group-item rounded-0 py-2">
            <vs-input-number color="danger" v-model="color1" />
          </li>
          <li class="list-group-item rounded-0 py-2">
            <vs-input-number color="success" v-model="color2" />
          </li>
          <li class="list-group-item rounded-0 py-2">
            <vs-input-number color="warning" v-model="color3" />
          </li>
          <li class="list-group-item rounded-0 py-2">
            <vs-input-number color="dark" v-model="color4" />
          </li>
          <li class="list-group-item rounded-0 py-2">
            <vs-input-number color="rgb(218, 24, 94)" v-model="color5" />
          </li>
          <li class="list-group-item rounded-0 py-2">
            <vs-input-number color="#ad3af9" v-model="color6" />
          </li>
        </ul>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="colornumint">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;div class=&quot;centerx&quot;&gt;
            &lt;vs-input-number color=&quot;danger&quot; v-model=&quot;number1&quot;/&gt;
            &lt;vs-input-number color=&quot;success&quot; v-model=&quot;number2&quot;/&gt;
            &lt;vs-input-number color=&quot;warning&quot; v-model=&quot;number3&quot;/&gt;
            &lt;vs-input-number color=&quot;dark&quot; v-model=&quot;number4&quot;/&gt;
            &lt;vs-input-number color=&quot;rgb(218, 24, 94)&quot; v-model=&quot;number5&quot;/&gt;
            &lt;vs-input-number color=&quot;#ad3af9&quot; v-model=&quot;number6&quot;/&gt;
            &lt;/div&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            data(){
            return {
            number1:196,
            number2:88,
            number3:25,
            number4:12,
            number5:590,
            number6:32,
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
		Min-Max Number Input
		/////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Min-Max Number Input
          <vs-button class="ml-auto p-0" @click="minmaxnumint=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can restrict the maximum number or the minimum with the properties
          <code>vs-min, vs-max</code>.
        </p>

        <ul class="list-group list-group-horizontal-lg">
          <li class="list-group-item rounded-0 py-2">
            <vs-input-number min="13" max="21" v-model="minmaxnumber" />
          </li>
        </ul>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="minmaxnumint">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;div class=&quot;centerx&quot;&gt;
            &lt;vs-input-number min=&quot;13&quot; max=&quot;21&quot; v-model=&quot;number1&quot;/&gt;
            &lt;/div&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            data(){
            return {
            number1:21,
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
		Size Number Input
		/////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Size Number Input
          <vs-button class="ml-auto p-0" @click="sizenumint=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          To change the size of the component, you can use the property
          <code>vs-size</code>. The allowed values are:
          <code>medium</code>,
          <code>small</code>, and
          <code>mini</code>.
        </p>

        <ul class="list-group list-group-horizontal-lg">
          <li class="list-group-item rounded-0 py-2">
            <vs-input-number v-model="size0" />
          </li>
          <li class="list-group-item rounded-0 py-2">
            <vs-input-number size="medium" v-model="size1" />
          </li>
          <li class="list-group-item rounded-0 py-2">
            <vs-input-number size="small" v-model="size2" />
          </li>
          <li class="list-group-item rounded-0 py-2">
            <vs-input-number size="mini" v-model="size3" />
          </li>
        </ul>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="sizenumint">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;div class=&quot;centerx&quot;&gt;
            &lt;vs-input-number v-model=&quot;number0&quot;/&gt;
            &lt;vs-input-number size=&quot;medium&quot; v-model=&quot;number1&quot;/&gt;
            &lt;vs-input-number size=&quot;small&quot; v-model=&quot;number2&quot;/&gt;
            &lt;vs-input-number size=&quot;mini&quot; v-model=&quot;number3&quot;/&gt;
            &lt;/div&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            data(){
            return {
            number0:95,
            number1:21,
            number2:67,
            number3:2
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
		Step Number Input
		/////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Step Number Input
          <vs-button class="ml-auto p-0" @click="stepnumint=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          To change the number to be added or decreased of the component, you can use the property
          <code>step</code>.
        </p>

        <ul class="list-group list-group-horizontal">
          <li class="list-group-item rounded-0 py-2">
            <vs-input-number v-model="step1" :step="5" />
          </li>
        </ul>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="stepnumint">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;div class=&quot;centerx&quot;&gt;
            &lt;vs-input-number v-model=&quot;number0&quot; :step=&quot;5&quot;/&gt;
            &lt;/div&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            data(){
            return {
            number0:5
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
		Decimal Number Input
		/////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Decimal Number Input
          <vs-button class="ml-auto p-0" @click="decnumint=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">Number Input also supports decimal values.</p>

        <ul class="list-group list-group-horizontal">
          <li class="list-group-item rounded-0 py-2">
            <vs-input-number v-model="dec1" :step="1.43" />
          </li>
        </ul>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="decnumint">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;div class=&quot;centerx&quot;&gt;
            &lt;vs-input-number v-model=&quot;number0&quot; :step=&quot;1.43&quot;/&gt;
            &lt;/div&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            data(){
            return {
            number0:1.98
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
		Label Number Input
		/////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Label Number Input
          <vs-button class="ml-auto p-0" @click="lblnumint=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">Number Input supports adding labels for number inputs.</p>

        <ul class="list-group list-group-horizontal">
          <li class="list-group-item rounded-0 py-2">
            <vs-input-number v-model="lbl1" label="passengers:" />
          </li>
        </ul>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="lblnumint">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;div class=&quot;centerx&quot;&gt;
            &lt;vs-input-number v-model=&quot;number0&quot; label=&quot;passengers:&quot;/&gt;
            &lt;/div&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            data(){
            return {
            number0:1
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
  name: "notification",
  data: () => ({
    title: "Notification",
    defaultnumint: false,
    number: 34,
    number1: 48,
    number2: 50,
    colornumint: false,
    color1: 196,
    color2: 88,
    color3: 25,
    color4: 12,
    color5: 590,
    color6: 32,
    minmaxnumint: false,
    minmaxnumber: 21,
    sizenumint: false,
    size0: 95,
    size1: 21,
    size2: 67,
    size3: 2,
    stepnumint: false,
    step1: 5,
    decnumint: false,
    dec1: 1.98,
    lblnumint: false,
    lbl1: 1
  })
};
</script>

