<template>
  <vs-row vs-justify="center">
    <vs-col type="flex" vs-justify="center" vs-align="center" vs-lg="12" vs-xs="12">
      <!--
        /////////////////
        Default Navbar
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Default Navbar
          <vs-button class="ml-auto p-0" @click="defaultnavbar=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          To add a navbar we have the component
          <code>vs-navbar</code>, there is a series of sub components to determine internal elements
          <code>vs-navbar-title</code>,
          <code>vs-spacer</code>.
        </p>

        <div>
          <vs-navbar v-model="activeItem" class="nabarx">
            <div slot="title">
              <vs-navbar-title>Navbar</vs-navbar-title>
            </div>

            <vs-navbar-item index="0">
              <a href="#">Home</a>
            </vs-navbar-item>
            <vs-navbar-item index="1">
              <a href="#">News</a>
            </vs-navbar-item>
            <vs-navbar-item index="2">
              <a href="#">Update</a>
            </vs-navbar-item>
          </vs-navbar>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="defaultnavbar">
          <vs-prism>
            &lt;div&gt;
            &lt;vs-navbar v-model=&quot;activeItem&quot; class=&quot;nabarx&quot;&gt;
            &lt;div slot=&quot;title&quot;&gt;
            &lt;vs-navbar-title&gt;
            Navbar
            &lt;/vs-navbar-title&gt;
            &lt;/div&gt;
            &lt;vs-navbar-item index=&quot;0&quot;&gt;
            &lt;a href=&quot;#&quot;&gt;Home&lt;/a&gt;
            &lt;/vs-navbar-item&gt;
            &lt;vs-navbar-item index=&quot;1&quot;&gt;
            &lt;a href=&quot;#&quot;&gt;News&lt;/a&gt;
            &lt;/vs-navbar-item&gt;
            &lt;vs-navbar-item index=&quot;2&quot;&gt;
            &lt;a href=&quot;#&quot;&gt;Update&lt;/a&gt;
            &lt;/vs-navbar-item&gt;
            &lt;/vs-navbar&gt;
            &lt;/div&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Navbar With Input
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Navbar With Input
          <vs-button class="ml-auto p-0" @click="inputnavbar=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You may need an entry in the menu to simply use the
          <code>vs-input</code> component, for example if you need a search engine.
        </p>

        <div>
          <vs-navbar v-model="activeItem" class="nabarx">
            <div slot="title">
              <vs-navbar-title>Navbar</vs-navbar-title>
            </div>
            <vs-navbar-item index="0">
              <a href="#">Home</a>
            </vs-navbar-item>
            <vs-navbar-item index="1">
              <a href="#">News</a>
            </vs-navbar-item>
            <vs-navbar-item index="2">
              <a href="#">Update</a>
            </vs-navbar-item>
            <vs-input icon="search" placeholder="Search" v-model="search" />
          </vs-navbar>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="inputnavbar">
          <vs-prism>
            &lt;div&gt;
            &lt;vs-navbar v-model=&quot;activeItem&quot; class=&quot;nabarx&quot;&gt;
            &lt;div slot=&quot;title&quot;&gt;
            &lt;vs-navbar-title&gt;
            Navbar
            &lt;/vs-navbar-title&gt;
            &lt;/div&gt;
            &lt;vs-navbar-item index=&quot;0&quot;&gt;
            &lt;a href=&quot;#&quot;&gt;Home&lt;/a&gt;
            &lt;/vs-navbar-item&gt;
            &lt;vs-navbar-item index=&quot;1&quot;&gt;
            &lt;a href=&quot;#&quot;&gt;News&lt;/a&gt;
            &lt;/vs-navbar-item&gt;
            &lt;vs-navbar-item index=&quot;2&quot;&gt;
            &lt;a href=&quot;#&quot;&gt;Update&lt;/a&gt;
            &lt;/vs-navbar-item&gt;
            &lt;vs-input icon=&quot;search&quot; placeholder=&quot;Search&quot; v-model=&quot;search&quot;/&gt;
            &lt;/vs-navbar&gt;
            &lt;/div&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Navbar With Types
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Navbar With Types
          <vs-button class="ml-auto p-0" @click="navbartypes=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          If you want you can change the style of the buttons and the navbar by changing the property
          <code>type</code>
        </p>

        <div>
          <vs-select class="mb-3" label="Figuras" v-model="type">
            <vs-select-item
              :key="index"
              :value="item.value"
              :text="item.text"
              v-for="(item,index) in types"
            />
          </vs-select>

          <vs-navbar :type="type" v-model="activeItem" class="nabarx">
            <div slot="title">
              <vs-navbar-title>Type {{type}}</vs-navbar-title>
            </div>

            <vs-navbar-item index="0">
              <a href="#">Home</a>
            </vs-navbar-item>
            <vs-navbar-item index="1">
              <a href="#">News</a>
            </vs-navbar-item>
            <vs-navbar-item index="2">
              <a href="#">Update</a>
            </vs-navbar-item>
          </vs-navbar>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="navbartypes">
          <vs-prism>
            &lt;template&gt;
            &lt;div class=&quot;con-type-example&quot;&gt;
            &lt;vs-select
            class=&quot;selectExample&quot;
            label=&quot;Figuras&quot;
            v-model=&quot;type&quot;
            &gt;
            &lt;vs-select-item :key=&quot;index&quot; :value=&quot;item.value&quot; :text=&quot;item.text&quot; v-for=&quot;(item,index) in types&quot; /&gt;
            &lt;/vs-select&gt;
            &lt;vs-navbar :type=&quot;type&quot; v-model=&quot;activeItem&quot; class=&quot;nabarx&quot;&gt;
            &lt;div slot=&quot;title&quot;&gt;
            &lt;vs-navbar-title&gt;
            Type {{type}}
            &lt;/vs-navbar-title&gt;
            &lt;/div&gt;
            &lt;vs-navbar-item index=&quot;0&quot;&gt;
            &lt;a href=&quot;#&quot;&gt;Home&lt;/a&gt;
            &lt;/vs-navbar-item&gt;
            &lt;vs-navbar-item index=&quot;1&quot;&gt;
            &lt;a href=&quot;#&quot;&gt;News&lt;/a&gt;
            &lt;/vs-navbar-item&gt;
            &lt;vs-navbar-item index=&quot;2&quot;&gt;
            &lt;a href=&quot;#&quot;&gt;Update&lt;/a&gt;
            &lt;/vs-navbar-item&gt;
            &lt;/vs-navbar&gt;
            &lt;/div&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            data:()=&gt;({
            activeItem: 0,
            type: 'flat',
            types: [
            {
            value: null, text: 'Default'
            },
            {
            value: 'flat', text: 'Flat'
            },
            {
            value: 'fund', text: 'Fund'
            },
            {
            value: 'border', text: 'border'
            },
            {
            value: 'gradient', text: 'Gradient'
            },
            {
            value: 'shadow', text: 'Shadow'
            }
            ]
            })
            }
            &lt;/script&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Navbar With colors
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Navbar With colors
          <vs-button class="ml-auto p-0" @click="navbarcolors=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can change the color of the Topbar with the property
          <code>color</code>. You are able to use the Main Colors or RGB and HEX colors.
        </p>

        <div>
          <input class="input-color mb-3" v-model="colorx" type="color" name value />
          <vs-navbar
            v-model="indexActive"
            :color="colorx"
            text-color="rgba(255,255,255,.6)"
            active-text-color="rgba(255,255,255,1)"
            class="myNavbar"
          >
            <div slot="title">
              <vs-navbar-title>Navbar Color</vs-navbar-title>
            </div>

            <vs-navbar-item index="0">
              <a href="#">Home</a>
            </vs-navbar-item>
            <vs-navbar-item index="1">
              <a href="#">News</a>
            </vs-navbar-item>
            <vs-navbar-item index="2">
              <a href="#">Update</a>
            </vs-navbar-item>

            <vs-spacer></vs-spacer>

            <vs-button
              color-text="rgb(255, 255, 255)"
              color="rgba(255, 255, 255, 0.3)"
              type="flat"
              icon="more_horiz"
            ></vs-button>
          </vs-navbar>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="navbarcolors">
          <vs-prism>
            &lt;template&gt;
            &lt;div class=&quot;centerx&quot;&gt;
            &lt;input class=&quot;input-color&quot; v-model=&quot;colorx&quot; type=&quot;color&quot; name=&quot;&quot; value=&quot;&quot;&gt;
            &lt;vs-navbar
            v-model=&quot;indexActive&quot;
            :color=&quot;colorx&quot;
            text-color=&quot;rgba(255,255,255,.6)&quot;
            active-text-color=&quot;rgba(255,255,255,1)&quot;
            class=&quot;myNavbar&quot;&gt;
            &lt;div slot=&quot;title&quot;&gt;
            &lt;vs-navbar-title&gt;
            Navbar Color
            &lt;/vs-navbar-title&gt;
            &lt;/div&gt;
            &lt;vs-navbar-item index=&quot;0&quot; &gt;
            &lt;a href=&quot;#&quot;&gt;Home&lt;/a&gt;
            &lt;/vs-navbar-item&gt;
            &lt;vs-navbar-item index=&quot;1&quot;&gt;
            &lt;a href=&quot;#&quot;&gt;News&lt;/a&gt;
            &lt;/vs-navbar-item&gt;
            &lt;vs-navbar-item index=&quot;2&quot;&gt;
            &lt;a href=&quot;#&quot;&gt;Update&lt;/a&gt;
            &lt;/vs-navbar-item&gt;
            &lt;vs-spacer&gt;&lt;/vs-spacer&gt;
            &lt;vs-button color-text=&quot;rgb(255, 255, 255)&quot; color=&quot;rgba(255, 255, 255, 0.3)&quot; type=&quot;flat&quot; icon=&quot;more_horiz&quot;&gt;&lt;/vs-button&gt;
            &lt;/vs-navbar&gt;
            &lt;/div&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            data: ()=&gt;({
            colorx:'#1db952',
            indexActive: 0
            })
            }
            &lt;/script&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Navbar With collapse
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Navbar With collapse
          <vs-button class="ml-auto p-0" @click="navbarcolors=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p
          class="card-subtitle"
        >This property determines if the component starts hidden and with the option of clicking on the menu to open or saw the options</p>

        <div>
          <vs-navbar collapse v-model="activeItem" class="nabarx">
            <div slot="title">
              <vs-navbar-title>Navbar</vs-navbar-title>
            </div>

            <vs-navbar-item index="0">
              <a href="#">Home</a>
            </vs-navbar-item>
            <vs-navbar-item index="1">
              <a href="#">News</a>
            </vs-navbar-item>
            <vs-navbar-item index="2">
              <a href="#">Update</a>
            </vs-navbar-item>
          </vs-navbar>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="navbarcolors">
          <vs-prism></vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>
    </vs-col>
  </vs-row>
</template>

<script>
export default {
  name: "navbar",
  data: () => ({
    title: "Navbar",
    defaultnavbar: false,
    activeItem: 0,
    inputnavbar: false,
    search: "",
    navbartypes: false,
    type: "gradient",
    types: [
      {
        value: null,
        text: "Default"
      },
      {
        value: "flat",
        text: "Flat"
      },
      {
        value: "fund",
        text: "Fund"
      },
      {
        value: "border",
        text: "border"
      },
      {
        value: "gradient",
        text: "Gradient"
      },
      {
        value: "shadow",
        text: "Shadow"
      }
    ],
    navbarcolors: false,
    colorx: "#1db952",
    indexActive: 0,
    radios2: "primary"
  })
};
</script>

