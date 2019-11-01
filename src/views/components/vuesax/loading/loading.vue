<template>
  <vs-row vs-justify="center">
    <vs-col type="flex" vs-justify="center" vs-align="center" vs-lg="12" vs-xs="12">
      <!--
        /////////////////
        Default loading
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Default loading
          <vs-button class="ml-auto p-0" @click="defaultloading=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          To add a loading in any part of your application we have the global function
          <code>$vs.loading ()</code>, and then when you want to remove it we have
          <code>$vs.loading.close()</code>.
        </p>

        <vs-button @click="openLoading" type="filled" color="primary">Loading Default</vs-button>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="defaultloading">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;div class=&quot;centerx&quot;&gt;
            &lt;vs-button @click=&quot;openLoading&quot; type=&quot;filled&quot; color=&quot;primary&quot;&gt;Loading Default&lt;/vs-button&gt;
            &lt;/div&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            methods:{
            openLoading(){
            this.$vs.loading()
            setTimeout( ()=&gt; {
            this.$vs.loading.close()
            }, 2000);
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
        Loading Type
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Loading Type
          <vs-button class="ml-auto p-0" @click="loadingtype=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can change the
          <code>type</code> of animation with the type property and the animations so far are:
        </p>
        <ul class="list-group list-group-horizontal-lg mb-3">
          <li class="list-group-item rounded-0 py-2">
            <span>point</span>
          </li>
          <li class="list-group-item py-2">
            <span>radius</span>
          </li>
          <li class="list-group-item py-2">
            <span>border</span>
          </li>
          <li class="list-group-item py-2">
            <span>corners</span>
          </li>
          <li class="list-group-item py-2">
            <span>sound</span>
          </li>
          <li class="list-group-item rounded-0 py-2">
            <span>material</span>
          </li>
        </ul>

        <div class="fill-row-loading d-flex align-items-center justify-content-center">
          <div
            :class="{'activeLoading':activeLoading}"
            @click="openLoading2(type)"
            v-for="type in types"
            :id="[`loading-${type}`]"
            :key="type"
            class="vs-con-loading__container loading-example"
          ></div>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="loadingtype">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;div class=&quot;demo-alignment&quot;&gt;
            &lt;div class=&quot;fill-row-loading&quot;&gt;
            &lt;div :class=&quot;{'activeLoading':activeLoading}&quot; @click=&quot;openLoading(type)&quot; v-for=&quot;type in types&quot; :id=&quot;[`loading-${type}`]&quot; class=&quot;vs-con-loading__container loading-example&quot;&gt;
            &lt;/div&gt;
            &lt;/div&gt;
            &lt;/div&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            data:()=&gt;({
            types:[
            'default',
            'point',
            'radius',
            'corners',
            'border',
            'sound',
            'material',
            ],
            activeLoading:false,
            }),
            mounted(){
            this.types.forEach((type)=&gt;{
            this.$vs.loading({
            container: `#loading-${type}`,
            type,
            text:type
            })
            })
            },
            methods:{
            openLoading(type){
            this.activeLoading = true
            this.$vs.loading({
            type:type,
            })
            setTimeout( ()=&gt; {
            this.activeLoading = false
            this.$vs.loading.close()
            }, 3000);
            },
            }
            }
            &lt;/script&gt;
            &lt;style lang=&quot;scss&quot;&gt;
            .fill-row-loading {
            display: flex;
            align-items: center;
            justify-content: center;
            flex-wrap: wrap;
            .loading-example {
            width: 120px;
            float: left;
            height: 120px;
            box-shadow: 0px 5px 20px 0px rgba(0, 0, 0, 0.05);
            border-radius: 10px;
            margin: 8px;
            transition: all 0.3s ease;
            cursor: pointer;
            &amp;:hover {
            box-shadow: 0px 0px 0px 0px rgba(0, 0, 0, 0.05);
            transform: translate(0, 4px);
            }
            h4 {
            z-index: 40000;
            position: relative;
            text-align: center;
            padding: 10px;
            }
            &amp;.activeLoading {
            opacity: 0 !important;
            transform: scale(0.5);
            }
            }
            }
            &lt;/style&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Loading Color
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Loading Color
          <vs-button class="ml-auto p-0" @click="loadingcolor=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can change the color of the loading with the property
          <code>color</code>.
        </p>

        <div class>
          <input type="color" v-model="colorLoading" name value />
          <vs-button @click="openLoadingColor" type="gradient" color="primary" class="ml-3">Primary</vs-button>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="loadingcolor">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;div class=&quot;centerx&quot;&gt;
            &lt;input type=&quot;color&quot; v-model=&quot;colorLoading&quot; name=&quot;&quot; value=&quot;&quot;&gt;
            &lt;vs-button @click=&quot;openLoadingColor&quot; type=&quot;gradient&quot; color=&quot;danger&quot;&gt;Danger&lt;/vs-button&gt;
            &lt;/div&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            data(){
            return {
            colorLoading:'#7d0c3f',
            }
            },
            methods:{
            openLoadingColor(){
            this.$vs.loading({color:this.colorLoading})
            setTimeout( ()=&gt; {
            this.$vs.loading.close()
            }, 2000);
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
        Loading Backgroundcolor
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Loading Backgroundcolor
          <vs-button class="ml-auto p-0" @click="loadingbgcolor=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          If you need to change the background of the loading, you can use the property
          <code>background</code>.
        </p>

        <div class>
          <input type="color" v-model="backgroundLoading" name value />
          <vs-button
            @click="openLoadingBackground"
            type="gradient"
            class="ml-3"
            color="primary"
          >Primary</vs-button>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="loadingbgcolor">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;div class=&quot;centerx&quot;&gt;
            &lt;input type=&quot;color&quot; v-model=&quot;backgroundLoading&quot; name=&quot;&quot; value=&quot;&quot;&gt;
            &lt;vs-button @click=&quot;openLoadingBackground&quot; type=&quot;gradient&quot; color=&quot;success&quot;&gt;Success&lt;/vs-button&gt;
            &lt;/div&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            data(){
            return {
            backgroundLoading:'#22c16b',
            }
            },
            methods:{
            openLoadingBackground(){
            this.$vs.loading({background:this.backgroundLoading,color:'rgb(255, 255, 255)'})
            setTimeout( ()=&gt; {
            this.$vs.loading.close()
            }, 3000);
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
        Loading Contained
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Loading Contained
          <vs-button class="ml-auto p-0" @click="containedloading=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          To add a loading within a container, call the
          <code>$ vs.loading ()</code> global function passing the
          <code>container</code> and the
          <code>scale</code> parameters. When you want to remove it we have
          <code>$ vs.loading.close ()</code>, passing the
          <code>same</code> container parameter.
        </p>

        <div class>
          <vs-button
            ref="loadableButton"
            id="button-with-loading"
            class="vs-con-loading__container"
            @click="openLoadingContained"
            type="relief"
            vslor="primary"
          >Button with Loading</vs-button>
          <vs-button
            @click="openLoadingInDiv"
            type="relief"
            class="ml-3"
            vslor="primary"
          >Div with Loading</vs-button>
          <div class="fill-row px-3 py-5 w-25 mt-3 shadow">
            <div id="div-with-loading" class="vs-con-loading__container">Load Me!</div>
          </div>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="containedloading">
          <vs-prism></vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>
    </vs-col>
  </vs-row>
</template>

<script>
export default {
  name: "list",
  data: () => ({
    title: "List",
    defaultloading: false,
    loadingtype: false,
    types: [
      "default",
      "point",
      "radius",
      "corners",
      "border",
      "sound",
      "material"
    ],
    activeLoading: false,
    loadingcolor: false,
    colorLoading: "#2962ff",
    loadingbgcolor: false,
    backgroundLoading: "#2962ff",
    containedloading: false
  }),
  methods: {
    openLoading() {
      this.$vs.loading();
      setTimeout(() => {
        this.$vs.loading.close();
      }, 2000);
    },
    openLoading2(type) {
      this.activeLoading = true;
      this.$vs.loading({
        type: type
      });
      setTimeout(() => {
        this.activeLoading = false;
        this.$vs.loading.close();
      }, 3000);
    },
    openLoadingColor() {
      this.$vs.loading({ color: this.colorLoading });
      setTimeout(() => {
        this.$vs.loading.close();
      }, 2000);
    },
    openLoadingBackground() {
      this.$vs.loading({
        background: this.backgroundLoading,
        color: "rgb(255, 255, 255)"
      });
      setTimeout(() => {
        this.$vs.loading.close();
      }, 3000);
    },
    openLoadingContained() {
      this.$vs.loading({
        background: this.backgroundLoading,
        color: this.colorLoading,
        container: this.refs.loadableButton,
        scale: 0.45
      });
      setTimeout(() => {
        this.$vs.loading.close(this.refs.loadableButton);
      }, 3000);
    },
    openLoadingInDiv() {
      this.$vs.loading({
        container: "#div-with-loading",
        scale: 0.6
      });
      setTimeout(() => {
        this.$vs.loading.close("#div-with-loading > .con-vs-loading");
      }, 3000);
    }
  },
  mounted() {
    this.types.forEach(type => {
      this.$vs.loading({
        container: `#loading-${type}`,
        type,
        text: type
      });
    });
  }
};
</script>


<style lang="scss">
.fill-row-loading {
  flex-wrap: wrap;
  .loading-example {
    width: 120px;
    z-index: 1;
    float: left;
    height: 120px;
    box-shadow: 0px 5px 20px 0px rgba(0, 0, 0, 0.05);
    border-radius: 10px;
    margin: 8px;
    transition: all 0.3s ease;
    cursor: pointer;
    &:hover {
      box-shadow: 0px 0px 0px 0px rgba(0, 0, 0, 0.05);
      transform: translate(0, 4px);
    }
    h4 {
      position: relative;
      text-align: center;
      padding: 10px;
    }
    &.activeLoading {
      opacity: 0 !important;
      transform: scale(0.5);
    }
  }
}
</style>

