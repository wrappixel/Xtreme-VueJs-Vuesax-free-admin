<template>
  <vs-row vs-justify="center">
    <vs-col type="flex" vs-justify="center" vs-align="center" vs-lg="12" vs-xs="12">
      <!--
        /////////////////
        Default Breadcrumb
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Default Breadcrumb
          <vs-button class="ml-auto p-0" @click="defaultbreadcrumb=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          Use the
          <code>items</code> in order to programatically generate the breadcrumb links.
        </p>
        <vs-breadcrumb
          :items="
               [
                 {
                   title: 'Dashboard',
                   url: 'dashboard'
                 },
                 {
                   title: 'Link 1',
                   url: 'link-1'
                 },
                 {
                   title: 'Link 2',
                   disabled: true
                 },
                 {
                   title: 'Active',
                   active: true
                 }
               ]"
        ></vs-breadcrumb>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="defaultbreadcrumb">
          <vs-prism>
            &lt;vs-breadcrumb
            :items=&quot;
            [
            {
            title: 'Dashboard',
            url: 'dashboard'
            },
            {
            title: 'Link 1',
            url: 'link-1'
            },
            {
            title: 'Link 2',
            disabled: true
            },
            {
            title: 'Active',
            active: true
            }
            ]&quot;
            &gt;&lt;/vs-breadcrumb&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        With Color Breadcrumb
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Color Breadcrumb
          <vs-button class="ml-auto p-0" @click="colorbreadcrumb=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          Use the
          <code>color</code> directive like for any other component that supports it to customize the breadcrumbs links color.
        </p>
        <div class="centerx">
          <input v-model="colorx" type="color" name value />
          <vs-breadcrumb :color="colorx" :items="items"></vs-breadcrumb>
        </div>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="colorbreadcrumb">
          <vs-prism>
            &lt;div class=&quot;centerx&quot;&gt;
            &lt;input v-model=&quot;colorx&quot; type=&quot;color&quot; name=&quot;&quot; value=&quot;&quot;&gt;
            &lt;vs-breadcrumb
            :color=&quot;colorx&quot;
            :items=&quot;items&quot;
            &gt;&lt;/vs-breadcrumb&gt;
            &lt;/div&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
            /////////////////
            With Separator Breadcrumb
            /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Separator Breadcrumb
          <vs-button class="ml-auto p-0" @click="separatorbreadcrumb=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can change the separator dividing the links by either passing a string to the separator directive like so "•", "-", "|" etc..., or by passing in one of the material icons text
          <code>"chevron_right"</code>.
        </p>
        <vs-breadcrumb :items="items" separator="•"></vs-breadcrumb>
        <vs-breadcrumb :items="items" separator="-"></vs-breadcrumb>
        <vs-breadcrumb :items="items" separator="|"></vs-breadcrumb>
        <vs-breadcrumb :items="items" separator="chevron_right"></vs-breadcrumb>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="separatorbreadcrumb">
          <vs-prism>
            &lt;vs-breadcrumb :items=&quot;items&quot; separator=&quot;&bull;&quot;&gt;&lt;/vs-breadcrumb&gt;
            &lt;vs-breadcrumb :items=&quot;items&quot; separator=&quot;-&quot;&gt;&lt;/vs-breadcrumb&gt;
            &lt;vs-breadcrumb :items=&quot;items&quot; separator=&quot;|&quot;&gt;&lt;/vs-breadcrumb&gt;
            &lt;vs-breadcrumb :items=&quot;items&quot; separator=&quot;chevron_right&quot;&gt;&lt;/vs-breadcrumb&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
            /////////////////
            With Slot Breadcrumb
            /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Slot Breadcrumb
          <vs-button class="ml-auto p-0" @click="slotbreadcrumb=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p
          class="card-subtitle"
        >A default Vue slot that can be used instead of passing in an array of object. This allows for greater control of the breadcrumbs</p>
        <vs-breadcrumb>
          <li>
            <a href="#" title="Home">Home</a>
            <span class="vs-breadcrum--separator">/</span>
          </li>
          <li>
            <a href="#" title="Profil">Profil</a>
            <span class="vs-breadcrum--separator">/</span>
          </li>
          <li aria-current="page" class="active">Infos</li>
        </vs-breadcrumb>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="slotbreadcrumb">
          <vs-prism>
            &lt;vs-breadcrumb&gt;
            &lt;li&gt;&lt;a href=&quot;#&quot; title=&quot;Home&quot;&gt;Home&lt;/a&gt;&lt;span class=&quot;vs-breadcrum--separator&quot;&gt;/&lt;/span&gt;&lt;/li&gt;
            &lt;li&gt;&lt;a href=&quot;#&quot; title=&quot;Profil&quot;&gt;Profil&lt;/a&gt;&lt;span class=&quot;vs-breadcrum--separator&quot;&gt;/&lt;/span&gt;&lt;/li&gt;
            &lt;li aria-current=&quot;page&quot; class=&quot;active&quot;&gt;Infos&lt;/li&gt;
            &lt;/vs-breadcrumb&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
            /////////////////
            With Alignment Breadcrumb
            /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Alignment Breadcrumb
          <vs-button class="ml-auto p-0" @click="alignmentbreadcrumb=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          Use
          <code>align</code> to either align the breadcrumb to the left, center or right.
        </p>
        <vs-breadcrumb align="left">
          <li>
            <a href="#" title="Home">Home</a>
            <span class="vs-breadcrum--separator">/</span>
          </li>
          <li>
            <a href="#" title="Profil">Profil</a>
            <span class="vs-breadcrum--separator">/</span>
          </li>
          <li aria-current="page" class="active">Infos</li>
        </vs-breadcrumb>
        <vs-breadcrumb align="center">
          <li>
            <a href="#" title="Home">Home</a>
            <span class="vs-breadcrum--separator">/</span>
          </li>
          <li>
            <a href="#" title="Profil">Profil</a>
            <span class="vs-breadcrum--separator">/</span>
          </li>
          <li aria-current="page" class="active">Infos</li>
        </vs-breadcrumb>
        <vs-breadcrumb align="right">
          <li>
            <a href="#" title="Home">Home</a>
            <span class="vs-breadcrum--separator">/</span>
          </li>
          <li>
            <a href="#" title="Profil">Profil</a>
            <span class="vs-breadcrum--separator">/</span>
          </li>
          <li aria-current="page" class="active">Infos</li>
        </vs-breadcrumb>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="alignmentbreadcrumb">
          <vs-prism>
            &lt;vs-breadcrumb align=&quot;left&quot;&gt;
            &lt;li&gt;&lt;a href=&quot;#&quot; title=&quot;Home&quot;&gt;Home&lt;/a&gt;&lt;span class=&quot;vs-breadcrum--separator&quot;&gt;/&lt;/span&gt;&lt;/li&gt;
            &lt;li&gt;&lt;a href=&quot;#&quot; title=&quot;Profil&quot;&gt;Profil&lt;/a&gt;&lt;span class=&quot;vs-breadcrum--separator&quot;&gt;/&lt;/span&gt;&lt;/li&gt;
            &lt;li aria-current=&quot;page&quot; class=&quot;active&quot;&gt;Infos&lt;/li&gt;
            &lt;/vs-breadcrumb&gt;
            &lt;vs-breadcrumb align=&quot;center&quot;&gt;
            &lt;li&gt;&lt;a href=&quot;#&quot; title=&quot;Home&quot;&gt;Home&lt;/a&gt;&lt;span class=&quot;vs-breadcrum--separator&quot;&gt;/&lt;/span&gt;&lt;/li&gt;
            &lt;li&gt;&lt;a href=&quot;#&quot; title=&quot;Profil&quot;&gt;Profil&lt;/a&gt;&lt;span class=&quot;vs-breadcrum--separator&quot;&gt;/&lt;/span&gt;&lt;/li&gt;
            &lt;li aria-current=&quot;page&quot; class=&quot;active&quot;&gt;Infos&lt;/li&gt;
            &lt;/vs-breadcrumb&gt;
            &lt;vs-breadcrumb align=&quot;right&quot;&gt;
            &lt;li&gt;&lt;a href=&quot;#&quot; title=&quot;Home&quot;&gt;Home&lt;/a&gt;&lt;span class=&quot;vs-breadcrum--separator&quot;&gt;/&lt;/span&gt;&lt;/li&gt;
            &lt;li&gt;&lt;a href=&quot;#&quot; title=&quot;Profil&quot;&gt;Profil&lt;/a&gt;&lt;span class=&quot;vs-breadcrum--separator&quot;&gt;/&lt;/span&gt;&lt;/li&gt;
            &lt;li aria-current=&quot;page&quot; class=&quot;active&quot;&gt;Infos&lt;/li&gt;
            &lt;/vs-breadcrumb&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>
    </vs-col>
  </vs-row>
</template>

<script>
export default {
  name: "breadcrumb",
  data: () => ({
    title: "Breadcrumb",
    defaultbreadcrumb: false,
    colorx: "#3DC9B3",
    items: [
      {
        title: "Dashboard",
        url: "dashboard"
      },
      {
        title: "Link 1",
        url: "link-1"
      },
      {
        title: "Link 2",
        disabled: true
      },
      {
        title: "Active",
        active: true
      }
    ],
    colorbreadcrumb: false,
    separatorbreadcrumb: false,
    slotbreadcrumb: false,
    alignmentbreadcrumb: false
  })
};
</script>


