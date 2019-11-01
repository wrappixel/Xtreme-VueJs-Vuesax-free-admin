<template>
  <vs-row vs-justify="center">
    <vs-col type="flex" vs-justify="center" vs-align="center" vs-lg="12" vs-xs="12">
      <!--
        /////////////////
        Default Divider
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Default Divider
          <vs-button class="ml-auto p-0" @click="defaultdivider=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can add a line to divide with the component
          <code>vs-divider</code>.
        </p>
        <div class="p-3 border">
          Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
          <vs-divider />Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
        </div>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="defaultdivider">
          <vs-prism>
            Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
            &lt;vs-divider/&gt;
            Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        With Text
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Text
          <vs-button class="ml-auto p-0" @click="textdivider=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p
          class="card-subtitle"
        >You can add a text between the line to delimit two elements and have a description for the user.</p>
        <div class="p-3 border">
          Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
          <vs-divider>My Text</vs-divider>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
        </div>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="textdivider">
          <vs-prism>
            Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
            &lt;vs-divider&gt;
            My Text
            &lt;/vs-divider&gt;
            Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        With Text Position
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Text Position
          <vs-button class="ml-auto p-0" @click="textposition=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can guide the text in 5 ways with property
          <code>position</code> :
        </p>
        <vs-row>
          <vs-col vs-lg="6" vs-xs="12">
            <ul class="list-group list-group-horizontal-lg mb-3">
              <li class="list-group-item rounded-0">left</li>
              <li class="list-group-item">left-center</li>
              <li class="list-group-item">center (default)</li>
              <li class="list-group-item">right-center</li>
              <li class="list-group-item rounded-0">right</li>
            </ul>
          </vs-col>
        </vs-row>
        <div class="p-3 border">
          <vs-divider position="left">My Text</vs-divider>
          <vs-divider position="left-center">My Text</vs-divider>
          <vs-divider position="center">My Text</vs-divider>
          <vs-divider position="right-center">My Text</vs-divider>
          <vs-divider position="right">My Text</vs-divider>
        </div>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="textposition">
          <vs-prism>
            &lt;vs-divider position=&quot;left&quot;&gt;
            My Text
            &lt;/vs-divider&gt;
            &lt;vs-divider position=&quot;left-center&quot;&gt;
            My Text
            &lt;/vs-divider&gt;
            &lt;vs-divider position=&quot;center&quot;&gt;
            My Text
            &lt;/vs-divider&gt;
            &lt;vs-divider position=&quot;right-center&quot;&gt;
            My Text
            &lt;/vs-divider&gt;
            &lt;vs-divider position=&quot;right&quot;&gt;
            My Text
            &lt;/vs-divider&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        With Text Color
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Text Color
          <vs-button class="ml-auto p-0" @click="dividercolor=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can change the color of the component with the property
          <code>color</code>, you can use the main colors or RGB and HEX.
        </p>
        <div class="p-3 border">
          <vs-divider>Default</vs-divider>
          <vs-divider color="primary">Primary</vs-divider>
          <vs-divider color="success">Success</vs-divider>
          <vs-divider color="danger">Danger</vs-divider>
          <vs-divider color="warning">Warning</vs-divider>
          <vs-divider color="dark">Dark</vs-divider>
          <vs-divider color="rgb(29, 222, 194)">RGB</vs-divider>
          <vs-divider color="#ad289f">HEX</vs-divider>
        </div>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="dividercolor">
          <vs-prism>
            &lt;vs-divider&gt;Default&lt;/vs-divider&gt;
            &lt;vs-divider color=&quot;primary&quot;&gt;Primary&lt;/vs-divider&gt;
            &lt;vs-divider color=&quot;success&quot;&gt;Success&lt;/vs-divider&gt;
            &lt;vs-divider color=&quot;danger&quot;&gt;Danger&lt;/vs-divider&gt;
            &lt;vs-divider color=&quot;warning&quot;&gt;Warning&lt;/vs-divider&gt;
            &lt;vs-divider color=&quot;dark&quot;&gt;Dark&lt;/vs-divider&gt;
            &lt;vs-divider color=&quot;rgb(29, 222, 194)&quot;&gt;RGB&lt;/vs-divider&gt;
            &lt;vs-divider color=&quot;#ad289f&quot;&gt;HEX&lt;/vs-divider&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        With Custom Icons Divider
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Custom Icons Divider
          <vs-button class="ml-auto p-0" @click="customdivider=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          To add an icon within the division we have the property
          <code>icon</code>.
        </p>
        <div class="p-3 border">
          <vs-divider icon="arrow_downward" position="left"></vs-divider>
          <vs-divider icon="star" position="left-center" color="primary"></vs-divider>
          <vs-divider icon="check" position="center" color="success"></vs-divider>
          <vs-divider icon="delete_forever" position="right-center" color="danger"></vs-divider>
          <vs-divider icon="report_problem" position="right" color="warning"></vs-divider>
          <vs-divider icon="watch_later" position="center" color="dark"></vs-divider>
        </div>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="customdivider">
          <vs-prism>
            &lt;vs-divider icon=&quot;arrow_downward&quot; position=&quot;left&quot;&gt;&lt;/vs-divider&gt;
            &lt;vs-divider icon=&quot;star&quot; position=&quot;left-center&quot; color=&quot;primary&quot;&gt;&lt;/vs-divider&gt;
            &lt;vs-divider icon=&quot;check&quot; position=&quot;center&quot; color=&quot;success&quot;&gt;&lt;/vs-divider&gt;
            &lt;vs-divider icon=&quot;delete_forever&quot; position=&quot;right-center&quot; color=&quot;danger&quot;&gt;&lt;/vs-divider&gt;
            &lt;vs-divider icon=&quot;report_problem&quot; position=&quot;right&quot; color=&quot;warning&quot;&gt;&lt;/vs-divider&gt;
            &lt;vs-divider icon=&quot;watch_later&quot; position=&quot;center&quot; color=&quot;dark&quot;&gt;&lt;/vs-divider&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        With Custom Style
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Custom Style
          <vs-button class="ml-auto p-0" @click="styledivider=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can change line's style with the property
          <code>border-style</code>. The allowed values are equivalent to the
          <code>border-style</code> property in CSS.
        </p>
        <vs-row>
          <vs-col vs-lg="6" vs-xs="12">
            <ul class="list-group mb-3">
              <li class="list-group-item rounded-0">
                <span class="font-weight-bold">dotted</span> - Defines a dotted border
              </li>
              <li class="list-group-item">
                <span class="font-weight-bold">dashed</span> - Defines a dashed border
              </li>
              <li class="list-group-item rounded-0">
                <span class="font-weight-bold">solid</span> - Defines a solid border (default)
              </li>
            </ul>
          </vs-col>
        </vs-row>

        <div class="p-3 border">
          <vs-divider border-style="dotted" color="dark">dotted</vs-divider>
          <vs-divider border-style="dashed" color="dark">dashed</vs-divider>
          <vs-divider border-style="solid" color="dark">solid</vs-divider>
        </div>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="styledivider">
          <vs-prism>
            &lt;vs-divider border-style=&quot;dotted&quot; color=&quot;dark&quot;&gt;dotted&lt;/vs-divider&gt;
            &lt;vs-divider border-style=&quot;dashed&quot; color=&quot;dark&quot;&gt;dashed&lt;/vs-divider&gt;
            &lt;vs-divider border-style=&quot;solid&quot; color=&quot;dark&quot;&gt;solid&lt;/vs-divider&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>
    </vs-col>
  </vs-row>
</template>

<script>
export default {
  name: "divider",
  data: () => ({
    title: "Divider",
    defaultdivider: false,
    textdivider: false,
    textposition: false,
    dividercolor: false,
    customdivider: false,
    styledivider: false
  })
};
</script>