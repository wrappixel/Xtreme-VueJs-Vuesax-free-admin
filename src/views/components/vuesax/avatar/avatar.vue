<template>
  <vs-row vs-justify="center">
    <vs-col type="flex" vs-justify="center" vs-align="center" vs-lg="12" vs-xs="12">
      <!--
        /////////////////
        Default Avatar
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Default Avatar
          <vs-button class="ml-auto p-0" @click="defaultavatar=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          Often you need to add an user's avatar to your app. In order to make this we have the component
          <code>vs-avatar</code>. To add an internal text value such as
          <code>Luis</code> use the
          <code>text</code> property.
        </p>
        <vs-avatar />
        <vs-avatar text="Luis Daniel" />
        <vs-avatar text="Luisd" />
        <vs-avatar src="https://avatars2.githubusercontent.com/u/31676496?s=460&v=4" />
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="defaultavatar">
          <vs-prism>
            &lt;vs-avatar /&gt;
            &lt;vs-avatar text=&quot;Luis Daniel&quot;/&gt;
            &lt;vs-avatar text=&quot;Luisd&quot;/&gt;
            &lt;vs-avatar src=&quot;https://avatars2.githubusercontent.com/u/31676496?s=460&v=4&quot;/&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>
      <!--
        /////////////////
        Avatar Size
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Avatar Size
          <vs-button class="ml-auto p-0" @click="sizeavatar=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can change the size of the Avatar with the property
          <code>size</code> the allowed values are:
        </p>
        <ul class="list-group list-group-horizontal mb-3">
          <li class="list-group-item rounded-0 py-2">
            <span>Large</span>
          </li>
          <li class="list-group-item rounded-0 py-2">
            <span>Small</span>
          </li>
          <li class="list-group-item rounded-0 py-2">
            <span>Custom Measure</span>
          </li>
        </ul>
        <vs-avatar size="small" />
        <vs-avatar text="Luis Daniel" />
        <vs-avatar size="large" src="https://avatars2.githubusercontent.com/u/31676496?s=460&v=4" />
        <vs-avatar size="70px" src="https://avatars2.githubusercontent.com/u/31676496?s=460&v=4" />
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="sizeavatar">
          <vs-prism>
            &lt;vs-avatar size=&quot;small&quot; /&gt;
            &lt;vs-avatar text=&quot;Luis Daniel&quot;/&gt;
            &lt;vs-avatar size=&quot;large&quot; src=&quot;https://avatars2.githubusercontent.com/u/31676496?s=460&amp;v=4&quot;/&gt;
            &lt;vs-avatar size=&quot;70px&quot; src=&quot;https://avatars2.githubusercontent.com/u/31676496?s=460&amp;v=4&quot;/&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Avatar Color
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Avatar Color
          <vs-button class="ml-auto p-0" @click="coloravatar=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can change the Avatar's color by using the property
          <code>color</code>. If needed you could also change the text's color with the property
          <code>text-color</code>.
        </p>
        <vs-avatar color="primary" text="primary" />
        <vs-avatar color="success" text="success" />
        <vs-avatar color="danger" text="danger" />
        <vs-avatar color="warning" text="warning" />
        <vs-avatar color="dark" text="dark" />
        <vs-avatar color="rgb(200, 21, 129)" text="RGB" />
        <vs-avatar color="#18cd5b" text="HEX" />
        <vs-avatar color="#26302a" text-color="rgb(246, 190, 16)" text="HEX RGB" />
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="coloravatar">
          <vs-prism>
            &lt;vs-avatar color=&quot;primary&quot; text=&quot;primary&quot;/&gt;
            &lt;vs-avatar color=&quot;success&quot; text=&quot;success&quot;/&gt;
            &lt;vs-avatar color=&quot;danger&quot; text=&quot;danger&quot;/&gt;
            &lt;vs-avatar color=&quot;warning&quot; text=&quot;warning&quot;/&gt;
            &lt;vs-avatar color=&quot;dark&quot; text=&quot;dark&quot;/&gt;
            &lt;vs-avatar color=&quot;rgb(200, 21, 129)&quot; text=&quot;RGB&quot;/&gt;
            &lt;vs-avatar color=&quot;#18cd5b&quot; text=&quot;HEX&quot;/&gt;
            &lt;vs-avatar color=&quot;#26302a&quot; text-color=&quot;rgb(246, 190, 16)&quot; text=&quot;HEX RGB&quot;/&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
            /////////////////
            Avatar Badge
            /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Avatar Badge
          <vs-button class="ml-auto p-0" @click="badgeavatar=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can add a notification label to the avatar, either a reference point or a number with the property
          <code>badge</code>.
        </p>
        <div class="con-avatarsx">
          <div class="con-avatar-solo">
            <vs-avatar badge />
            <vs-avatar :badge="badge1" text="Luisdaniel" />
            <vs-avatar badge-color="rgb(140, 23, 164)" :badge="badge2" text="Luisd" />
          </div>
          <vs-button color="primary" type="filled" @click="increment">Increment Badge counter</vs-button>
        </div>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="badgeavatar">
          <vs-prism>
            &lt;div class=&quot;con-avatarsx&quot;&gt;
            &lt;div class=&quot;con-avatar-solo&quot;&gt;
            &lt;vs-avatar badge /&gt;
            &lt;vs-avatar :badge=&quot;badge1&quot; text=&quot;Luisdaniel&quot;/&gt;
            &lt;vs-avatar badge-color=&quot;rgb(140, 23, 164)&quot; :badge=&quot;badge2&quot; text=&quot;Luisd&quot;/&gt;
            &lt;/div&gt;
            &lt;vs-button color=&quot;primary&quot; type=&quot;filled&quot; @click=&quot;increment&quot;&gt;
            Increment Badge counter
            &lt;/vs-button&gt;
            &lt;/div&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
            /////////////////
            Avatar Icon
            /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Avatar Icon
          <vs-button class="ml-auto p-0" @click="iconavatar=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can change the main icon of the Avatar with the property
          <code>icon</code>
        </p>
        <vs-avatar />
        <vs-avatar color="primary" icon="date_range" />
        <vs-avatar color="success" icon="whatshot" />
        <vs-avatar color="danger" icon="photo_camera" />
        <vs-avatar color="warning" icon="filter_vintage" />
        <vs-avatar color="dark" icon="watch" />
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="iconavatar">
          <vs-prism>
            &lt;vs-avatar /&gt;
            &lt;vs-avatar color=&quot;primary&quot; icon=&quot;date_range&quot; /&gt;
            &lt;vs-avatar color=&quot;success&quot; icon=&quot;whatshot&quot; /&gt;
            &lt;vs-avatar color=&quot;danger&quot; icon=&quot;photo_camera&quot; /&gt;
            &lt;vs-avatar color=&quot;warning&quot; icon=&quot;filter_vintage&quot; /&gt;
            &lt;vs-avatar color=&quot;dark&quot; icon=&quot;watch&quot; /&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>
    </vs-col>
  </vs-row>
</template>

<script>
export default {
  name: "avatar",
  data: () => ({
    title: "Avatar",
    defaultavatar: false,
    sizeavatar: false,
    coloravatar: false,
    badge1: 2,
    badge2: 10,
    badgeavatar: false,
    iconavatar: false
  }),
  methods: {
    increment() {
      this.badge1++;
      this.badge2++;
    }
  }
};
</script>


