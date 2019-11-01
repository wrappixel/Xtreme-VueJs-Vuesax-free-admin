<template>
  <vs-row vs-justify="center">
    <vs-col type="flex" vs-justify="center" vs-align="center" vs-lg="12" vs-xs="12">
      <!--
		/////////////////
		Default Progress
		/////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Default Progress
          <vs-button class="ml-auto p-0" @click="defaultprogress=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">Nice colors for your progress bar.</p>

        <div>
          <vs-progress :percent="100" color="primary">primary</vs-progress>
          <vs-progress :percent="90" color="warning">warning</vs-progress>
          <vs-progress :percent="75" color="danger">danger</vs-progress>
          <vs-progress :percent="60" color="success">success</vs-progress>
          <vs-progress :percent="45" color="dark">dark</vs-progress>
          <vs-progress :percent="30" color="rgb(164, 69, 15)">RGB</vs-progress>
          <vs-progress :percent="15" color="#24c1a0">HEX</vs-progress>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="defaultprogress">
          <vs-prism>
            &lt;vs-progress :percent=&quot;100&quot; color=&quot;primary&quot;&gt;primary&lt;/vs-progress&gt;
            &lt;vs-progress :percent=&quot;90&quot; color=&quot;warning&quot;&gt;warning&lt;/vs-progress&gt;
            &lt;vs-progress :percent=&quot;75&quot; color=&quot;danger&quot;&gt;danger&lt;/vs-progress&gt;
            &lt;vs-progress :percent=&quot;60&quot; color=&quot;success&quot;&gt;success&lt;/vs-progress&gt;
            &lt;vs-progress :percent=&quot;45&quot; color=&quot;dark&quot;&gt;dark&lt;/vs-progress&gt;
            &lt;vs-progress :percent=&quot;30&quot; color=&quot;rgb(164, 69, 15)&quot;&gt;RGB&lt;/vs-progress&gt;
            &lt;vs-progress :percent=&quot;15&quot; color=&quot;#24c1a0&quot;&gt;HEX&lt;/vs-progress&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
		/////////////////
		Indeterminate Progress
		/////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Indeterminate Progress
          <vs-button class="ml-auto p-0" @click="interprogress=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can have a progress bar with indeterminate value with the property
          <code>indeterminate</code>.
        </p>

        <div>
          <vs-progress indeterminate color="primary">primary</vs-progress>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="interprogress">
          <vs-prism>&lt;vs-progress indeterminate color=&quot;primary&quot;&gt;primary&lt;/vs-progress&gt;</vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
		/////////////////
		Height Progress
		/////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Height Progress
          <vs-button class="ml-auto p-0" @click="heightprogress=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can change the height of the loading bar with the property
          <code>height</code>.
        </p>

        <div>
          <vs-progress :height="2" :percent="100" color="primary">primary</vs-progress>
          <vs-progress :height="4" :percent="80" color="warning">warning</vs-progress>
          <vs-progress :height="8" :percent="60" color="danger">danger</vs-progress>
          <vs-progress :height="12" :percent="40" color="success">success</vs-progress>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="heightprogress">
          <vs-prism>
            &lt;vs-progress :height=&quot;2&quot; :percent=&quot;100&quot; color=&quot;primary&quot;&gt;primary&lt;/vs-progress&gt;
            &lt;vs-progress :height=&quot;4&quot; :percent=&quot;80&quot; color=&quot;warning&quot;&gt;warning&lt;/vs-progress&gt;
            &lt;vs-progress :height=&quot;8&quot; :percent=&quot;60&quot; color=&quot;danger&quot;&gt;danger&lt;/vs-progress&gt;
            &lt;vs-progress :height=&quot;12&quot; :percent=&quot;40&quot; color=&quot;success&quot;&gt;success&lt;/vs-progress&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>
    </vs-col>
  </vs-row>
</template>

<script>
export default {
  name: "progress",
  data: () => ({
    title: "Progress",
    defaultprogress: false,
    interprogress: false,
    heightprogress: false
  })
};
</script>

