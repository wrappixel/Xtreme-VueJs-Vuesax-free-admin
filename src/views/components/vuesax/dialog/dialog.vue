<template>
  <vs-row vs-justify="center">
    <vs-col type="flex" vs-justify="center" vs-align="center" vs-lg="12" vs-xs="12">
      <!--
        /////////////////
        With Alert
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Alert
          <vs-button class="ml-auto p-0" @click="defaultalert=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          To generate a dialog we have the global function
          <code>$vs.dialog</code> the parameters to generate the dialog are
        </p>

        <vs-row>
          <vs-col vs-lg="8" vs-xs="12">
            <vs-list>
              <vs-list-item title="title" subtitle="title of the dialogue - String"></vs-list-item>
              <vs-list-item title="text" subtitle="internal text of the dialog - String"></vs-list-item>
              <vs-list-item title="color" subtitle="color of the component - Colors, RGB, HEX"></vs-list-item>
              <vs-list-item
                title="accept"
                subtitle="function that executes the user accept the dialog - Function"
              ></vs-list-item>
              <vs-list-item
                title="cancel"
                subtitle="function that executes the user to cancel the dialog (if it is a confirm type) - Function"
              ></vs-list-item>
              <vs-list-item
                title="type"
                subtitle="determines the type of dialog (alert or confirm) - alert, confirm"
              ></vs-list-item>
              <vs-list-item
                title="buttonAccept"
                subtitle="determines the type of accept button - Boolean"
              ></vs-list-item>
              <vs-list-item
                title="buttonCancel"
                subtitle="determines the type of cancel button - Boolean"
              ></vs-list-item>
            </vs-list>
          </vs-col>
        </vs-row>

        <div class="m-3 btn-alignment">
          <vs-button @click="openAlert('primary')" color="primary" type="flat">Alert Primary</vs-button>
          <vs-button @click="openAlert('success')" color="success" type="flat">Alert Success</vs-button>
          <vs-button @click="openAlert('danger')" color="danger" type="flat">Alert Danger</vs-button>
          <vs-button @click="openAlert('warning')" color="warning" type="flat">Alert Warning</vs-button>
          <vs-button @click="openAlert('dark')" color="dark" type="flat">Alert Dark</vs-button>
          <vs-button @click="openAlert(null)" color="primary" type="gradient">Alert Color RGB | HEX</vs-button>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="defaultalert">
          <vs-prism>
            &lt;div class=&quot;m-3 btn-alignment&quot;&gt;
            &lt;vs-button @click=&quot;openAlert('primary')&quot; color=&quot;primary&quot; type=&quot;flat&quot;&gt;Alert Primary&lt;/vs-button&gt;
            &lt;vs-button @click=&quot;openAlert('success')&quot; color=&quot;success&quot; type=&quot;flat&quot;&gt;Alert Success&lt;/vs-button&gt;
            &lt;vs-button @click=&quot;openAlert('danger')&quot; color=&quot;danger&quot; type=&quot;flat&quot;&gt;Alert Danger&lt;/vs-button&gt;
            &lt;vs-button @click=&quot;openAlert('warning')&quot; color=&quot;warning&quot; type=&quot;flat&quot;&gt;Alert Warning&lt;/vs-button&gt;
            &lt;vs-button @click=&quot;openAlert('dark')&quot; color=&quot;dark&quot; type=&quot;flat&quot;&gt;Alert Dark&lt;/vs-button&gt;
            &lt;vs-button @click=&quot;openAlert(null)&quot; color=&quot;primary&quot; type=&quot;gradient&quot;&gt;Alert Color RGB | HEX&lt;/vs-button&gt;
            &lt;/div&gt;
            &lt;script&gt;
            export default {
            data:()=&gt;({
            colorAlert:'primary',
            titleAlert:'Alert',
            activeAlert:false,
            valueInput:'',
            }),
            methods:{
            openAlert(color){
            this.colorAlert = color || this.getColorRandom()
            this.$vs.dialog({
            color:this.colorAlert,
            title: `Dialog - ${this.colorAlert}`,
            text: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.',
            accept:this.acceptAlert
            })
            },
            acceptAlert(){
            this.$vs.notify({
            color:this.colorAlert,
            title:'Accept Selected',
            text:'Lorem ipsum dolor sit amet, consectetur'
            })
            },
            getColorRandom(){
            function getRandomInt(min, max) {
            return Math.floor(Math.random() * (max - min)) + min;
            }
            return `rgb(${getRandomInt(0,255)},${getRandomInt(0,255)},${getRandomInt(0,255)})`
            },
            }
            }
            &lt;/script&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        With Confirm Alert
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Confirm Alert
          <vs-button class="ml-auto p-0" @click="confirmalert=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p
          class="card-subtitle"
        >If you need a dialog of type confirm you can do it just by changing the type as a parameter inside the main function.</p>

        <div>
          <vs-button @click="openConfirm()" color="primary" type="gradient">Alert Primary</vs-button>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="confirmalert">
          <vs-prism>
            &lt;div&gt;
            &lt;vs-button @click=&quot;openConfirm()&quot; color=&quot;danger&quot; type=&quot;gradient&quot;&gt;Alert Primary&lt;/vs-button&gt;
            &lt;/div&gt;
            &lt;script&gt;
            export default {
            data: () =&gt; ({
            activeConfirm: false
            }),
            methods: {
            openConfirm() {
            this.$vs.dialog({
            type: 'confirm',
            color: 'danger',
            title: `Confirm`,
            text: 'Cake sesame snaps cupcake gingerbread danish I love gingerbread. Apple pie pie jujubes chupa chups.',
            accept: this.acceptAlert
            })
            },
            acceptAlert() {
            this.$vs.notify({
            color: 'danger',
            title: 'Deleted image',
            text: 'The selected image was successfully deleted'
            })
            },
            }
            }
            &lt;/script&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        With Promt Alert
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Promt Alert
          <vs-button class="ml-auto p-0" @click="promtalert=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          To add a dialog of type prompt we have a global function a completely independent component
          <code>vs-prompt</code>. This allows more flexibility with the input and ability to add any type of input and components.
        </p>

        <vs-row>
          <vs-col vs-lg="6" vs-xs="12">
            <div class="d-flex align-items-center">
              <vs-button @click="activePrompt = true" color="primary" type="border">Run prompt</vs-button>
              <div class="modelx bg-light p-3 shadow ml-3 rounded-pill">
                <span
                  class="text-primary font-weight-bold border-bottom pb-1 border-primary mr-3"
                >Security Code Here:</span>
                {{val==null?'null':val}}
              </div>
            </div>
          </vs-col>
          <vs-col vs-lg="6" vs-xs="12">
            <div class="d-flex align-items-center">
              <vs-button
                @click="activePrompt2 = true"
                color="primary"
                type="border"
              >Run prompt inputs</vs-button>
              <div class="modelx bg-light p-3 shadow ml-3 rounded-pill">
                <span
                  class="text-primary font-weight-bold border-bottom pb-1 border-primary mr-3"
                >Name Here:</span>
                <span class="mr-3 border-right pr-3">{{valMultipe.value1}}</span>

                <span
                  class="text-primary font-weight-bold border-bottom pb-1 border-primary mr-3"
                >Last Name Here:</span>
                {{valMultipe.value2}}
              </div>
            </div>
          </vs-col>
        </vs-row>

        <vs-prompt
          @cancel="val=''"
          @accept="acceptAlert3"
          @close="close"
          :active.sync="activePrompt"
        >
          <div class="p-2 pb-0">
            Enter the security code
            <vs-input placeholder="Code" class="mb-3" v-model="val" />
            <vs-select class="selectExample" label="Figuras" v-model="select1">
              <vs-select-item
                :key="index"
                :value="item.value"
                :text="item.text"
                v-for="(item,index) in options1"
              />
            </vs-select>
          </div>
        </vs-prompt>

        <vs-prompt
          color="danger"
          @cancel="valMultipe.value1='',valMultipe.value2=''"
          @accept="acceptAlert3"
          @close="close"
          :is-valid="validName"
          :active.sync="activePrompt2"
        >
          <div class="con-exemple-prompt">
            Enter your first and last name to
            <b>continue</b>.
            <vs-input placeholder="Name" class="mb-3" v-model="valMultipe.value1" />
            <vs-input placeholder="Last Name" class="mb-3" v-model="valMultipe.value2" />

            <vs-alert
              :active="!validName"
              color="danger"
              icon="new_releases"
            >Fields can not be empty please enter the data</vs-alert>
          </div>
        </vs-prompt>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="promtalert">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;div class=&quot;centerx con-exemple-prompt&quot;&gt;
            &lt;!-- &lt;vs-button @click=&quot;openPrompt&quot; color=&quot;primary&quot; type=&quot;border&quot;&gt;Run prompt&lt;/vs-button&gt; --&gt;
            &lt;div class=&quot;modelx&quot;&gt;
            {{val==null?'null':val}}
            &lt;/div&gt;
            &lt;vs-button @click=&quot;activePrompt = true&quot; color=&quot;primary&quot; type=&quot;border&quot;&gt;Run prompt&lt;/vs-button&gt;
            &lt;div class=&quot;modelx&quot;&gt;
            {{valMultipe.value1}}
            {{valMultipe.value2}}
            &lt;/div&gt;
            &lt;vs-button @click=&quot;activePrompt2 = true&quot; color=&quot;primary&quot; type=&quot;border&quot;&gt;Run prompt inputs&lt;/vs-button&gt;
            &lt;vs-prompt
            @cancel=&quot;val=''&quot;
            @accept=&quot;acceptAlert&quot;
            @close=&quot;close&quot;
            :active.sync=&quot;activePrompt&quot;&gt;
            &lt;div class=&quot;con-exemple-prompt&quot;&gt;
            Enter the security code
            &lt;vs-input placeholder=&quot;Code&quot; placeholder=&quot;Code&quot; v-model=&quot;val&quot;/&gt;
            &lt;vs-select
            class=&quot;selectExample&quot;
            label=&quot;Figuras&quot;
            v-model=&quot;select1&quot;
            &gt;
            &lt;vs-select-item :key=&quot;index&quot; :value=&quot;item.value&quot; :text=&quot;item.text&quot; v-for=&quot;item,index in options1&quot; /&gt;
            &lt;/vs-select&gt;
            &lt;/div&gt;
            &lt;/vs-prompt&gt;
            &lt;vs-prompt
            color=&quot;danger&quot;
            @cancel=&quot;valMultipe.value1='',valMultipe.value2=''&quot;
            @accept=&quot;acceptAlert&quot;
            @close=&quot;close&quot;
            :is-valid=&quot;validName&quot;
            :active.sync=&quot;activePrompt2&quot;&gt;
            &lt;div class=&quot;con-exemple-prompt&quot;&gt;
            Enter your first and last name to &lt;b&gt;continue&lt;/b&gt;.
            &lt;vs-input placeholder=&quot;Name&quot; v-model=&quot;valMultipe.value1&quot;/&gt;
            &lt;vs-input placeholder=&quot;Last Name&quot; v-model=&quot;valMultipe.value2&quot;/&gt;
            &lt;vs-alert :active=&quot;!validName&quot; color=&quot;danger&quot; icon=&quot;new_releases&quot; &gt;
            Fields can not be empty please enter the data
            &lt;/vs-alert&gt;
            &lt;/div&gt;
            &lt;/vs-prompt&gt;
            &lt;/div&gt;
            &lt;/template&gt;
            &lt;script&gt;
            import Vue from 'vue'
            export default {
            data(){
            return {
            select1:2,
            options1:[
            {text:'IT',value:0},
            {text:'Blade Runner',value:2},
            {text:'Thor Ragnarok',value:3},
            ],
            activePrompt:false,
            activePrompt2:false,
            val:'',
            valMultipe:{
            value1:'',
            value2:''
            },
            }
            },
            computed:{
            validName(){
            return (this.valMultipe.value1.length &gt; 0 &amp;&amp; this.valMultipe.value2.length &gt; 0)
            }
            },
            methods:{
            acceptAlert(color){
            this.$vs.notify({
            color:'success',
            title:'Accept Selected',
            text:'Lorem ipsum dolor sit amet, consectetur'
            })
            },
            close(){
            this.$vs.notify({
            color:'danger',
            title:'Closed',
            text:'You close a dialog!'
            })
            },
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
  name: "dialog",
  data: () => ({
    title: "Dialog",
    defaultalert: false,
    colorAlert: "primary",
    titleAlert: "Alert",
    activeAlert: false,
    valueInput: "",
    activeConfirm: false,
    confirmalert: false,
    select1: 2,
    options1: [
      { text: "IT", value: 0 },
      { text: "Blade Runner", value: 2 },
      { text: "Thor Ragnarok", value: 3 }
    ],
    activePrompt: false,
    activePrompt2: false,
    val: "",
    valMultipe: {
      value1: "",
      value2: ""
    },
    promtalert: false
  }),
  computed: {
    validName() {
      return (
        this.valMultipe.value1.length > 0 && this.valMultipe.value2.length > 0
      );
    }
  },
  methods: {
    openAlert(color) {
      this.colorAlert = color || this.getColorRandom();
      this.$vs.dialog({
        color: this.colorAlert,
        title: `Dialog - ${this.colorAlert}`,
        text:
          "Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
        accept: this.acceptAlert
      });
    },
    acceptAlert() {
      this.$vs.notify({
        color: this.colorAlert,
        title: "Accept Selected",
        text: "Lorem ipsum dolor sit amet, consectetur"
      });
    },
    getColorRandom() {
      function getRandomInt(min, max) {
        return Math.floor(Math.random() * (max - min)) + min;
      }
      return `rgb(${getRandomInt(0, 255)},${getRandomInt(
        0,
        255
      )},${getRandomInt(0, 255)})`;
    },
    openConfirm() {
      this.$vs.dialog({
        type: "confirm",
        color: "primary",
        title: `Confirm`,
        text:
          "Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.",
        accept: this.acceptAlert2
      });
    },
    acceptAlert2() {
      this.$vs.notify({
        color: "primary",
        title: "Deleted image",
        text: "The selected image was successfully deleted"
      });
    },
    acceptAlert3() {
      this.$vs.notify({
        color: "success",
        title: "Accept Selected",
        text: "Lorem ipsum dolor sit amet, consectetur"
      });
    },
    close() {
      this.$vs.notify({
        color: "danger",
        title: "Closed",
        text: "You close a dialog!"
      });
    }
  }
};
</script>


