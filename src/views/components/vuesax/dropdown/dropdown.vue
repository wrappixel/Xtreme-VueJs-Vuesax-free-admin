<template>
  <vs-row vs-justify="center">
    <vs-col type="flex" vs-justify="center" vs-align="center" vs-lg="12" vs-xs="12">
      <!--
        /////////////////
        Default Dropdown
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Default Dropdown
          <vs-button class="ml-auto p-0" @click="defaultdropdown=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          To add the Dropdown we have three types of components the main
          <code>vs-dropdown</code> that contains the element that makes the
          <code>vs-dropdown-menu</code> appear and to add each item within it we have the component
          <code>vs-dropdown-item</code>
        </p>

        <vs-dropdown class="mr-4">
          <a class="a-icon" href="#">
            Dropdown hover
            <vs-icon class icon="expand_more"></vs-icon>
          </a>

          <vs-dropdown-menu>
            <vs-dropdown-item>Option 1</vs-dropdown-item>
            <vs-dropdown-item>Option 2</vs-dropdown-item>
            <vs-dropdown-item divider>Option 3</vs-dropdown-item>
          </vs-dropdown-menu>
        </vs-dropdown>

        <vs-dropdown>
          <a class="a-icon" href.prevent>
            Dropdown Option Disabled
            <vs-icon class icon="expand_more"></vs-icon>
          </a>

          <vs-dropdown-menu>
            <vs-dropdown-item>Option 1</vs-dropdown-item>
            <vs-dropdown-item disabled>Option 2</vs-dropdown-item>
            <vs-dropdown-item disabled divider>Option 3</vs-dropdown-item>
          </vs-dropdown-menu>
        </vs-dropdown>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="defaultdropdown">
          <vs-prism>
            &lt;vs-dropdown class=&quot;mr-4&quot;&gt;
            &lt;a class=&quot;a-icon&quot; href=&quot;#&quot;&gt;
            Dropdown hover
            &lt;vs-icon class=&quot;&quot; icon=&quot;expand_more&quot;&gt;&lt;/vs-icon&gt;
            &lt;/a&gt;
            &lt;vs-dropdown-menu&gt;
            &lt;vs-dropdown-item&gt;
            Option 1
            &lt;/vs-dropdown-item&gt;
            &lt;vs-dropdown-item&gt;
            Option 2
            &lt;/vs-dropdown-item&gt;
            &lt;vs-dropdown-item divider&gt;
            Option 3
            &lt;/vs-dropdown-item&gt;
            &lt;/vs-dropdown-menu&gt;
            &lt;/vs-dropdown&gt;
            &lt;vs-dropdown &gt;
            &lt;a class=&quot;a-icon&quot; href.prevent&gt;
            Dropdown Option Disabled
            &lt;vs-icon class=&quot;&quot; icon=&quot;expand_more&quot;&gt;&lt;/vs-icon&gt;
            &lt;/a&gt;
            &lt;vs-dropdown-menu&gt;
            &lt;vs-dropdown-item&gt;
            Option 1
            &lt;/vs-dropdown-item&gt;
            &lt;vs-dropdown-item disabled&gt;
            Option 2
            &lt;/vs-dropdown-item &gt;
            &lt;vs-dropdown-item disabled divider&gt;
            Option 3
            &lt;/vs-dropdown-item&gt;
            &lt;/vs-dropdown-menu&gt;
            &lt;/vs-dropdown&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Default Color Dropdown
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Default Color Dropdown
          <vs-button class="ml-auto p-0" @click="colordropdown=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can change the color of the component with the property
          <code>color</code>
        </p>

        <div class>
          <input type="color" class="mr-4" v-model="colorx" />
          <vs-dropdown :color="colorx">
            <a class="a-icon" href="#">
              Dropdown hover
              <vs-icon class icon="expand_more"></vs-icon>
            </a>

            <vs-dropdown-menu>
              <vs-dropdown-item>option 1</vs-dropdown-item>
              <vs-dropdown-item>option 2</vs-dropdown-item>
              <vs-dropdown-item divider>option 3</vs-dropdown-item>
            </vs-dropdown-menu>
          </vs-dropdown>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="colordropdown">
          <vs-prism>
            &lt;div class=&quot;&quot;&gt;
            &lt;input type=&quot;color&quot; class=&quot;mr-4&quot; v-model=&quot;colorx&quot;&gt;
            &lt;vs-dropdown :color=&quot;colorx&quot;&gt;
            &lt;a class=&quot;a-icon&quot; href=&quot;#&quot;&gt;
            Dropdown hover
            &lt;vs-icon class=&quot;&quot; icon=&quot;expand_more&quot;&gt;&lt;/vs-icon&gt;
            &lt;/a&gt;
            &lt;vs-dropdown-menu&gt;
            &lt;vs-dropdown-item&gt;
            option 1
            &lt;/vs-dropdown-item&gt;
            &lt;vs-dropdown-item&gt;
            option 2
            &lt;/vs-dropdown-item&gt;
            &lt;vs-dropdown-item divider&gt;
            option 3
            &lt;/vs-dropdown-item&gt;
            &lt;/vs-dropdown-menu&gt;
            &lt;/vs-dropdown&gt;
            &lt;/div&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Dropdown Option Group
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Dropdown Option Group
          <vs-button class="ml-auto p-0" @click="opgrpdropdown=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          If you need to group the options you can use the subcomponent
          <code>vs-dropdown-group</code> which as a required parameter is
          <code>vs-label</code> to define the group title
        </p>

        <div class>
          <vs-dropdown>
            <a class="a-icon" href.prevent>
              Dropdown Option Group
              <vs-icon class icon="expand_more"></vs-icon>
            </a>

            <vs-dropdown-menu>
              <vs-dropdown-item>Option 1</vs-dropdown-item>
              <vs-dropdown-item>Option 2</vs-dropdown-item>
              <vs-dropdown-group>
                <vs-dropdown-item>Option 1</vs-dropdown-item>
                <vs-dropdown-item>Option 2</vs-dropdown-item>

                <vs-dropdown-group>
                  <vs-dropdown-item>sub Options 1</vs-dropdown-item>
                  <vs-dropdown-item>sub Options 2</vs-dropdown-item>
                </vs-dropdown-group>
              </vs-dropdown-group>
              <vs-dropdown-item divider>Option 3</vs-dropdown-item>
            </vs-dropdown-menu>
          </vs-dropdown>

          <vs-dropdown>
            <a class="a-icon" href.prevent>
              Dropdown Group Collapse
              <vs-icon class icon="expand_more"></vs-icon>
            </a>

            <vs-dropdown-menu>
              <vs-dropdown-item to="/components/">Option 1</vs-dropdown-item>
              <vs-dropdown-item>Option 2</vs-dropdown-item>

              <vs-dropdown-group vs-collapse vs-label="Group Collapse" vs-icon="add">
                <vs-dropdown-item>Option Collapse 1</vs-dropdown-item>
                <vs-dropdown-item>Option Collapse 2</vs-dropdown-item>
                <vs-dropdown-group>
                  <vs-dropdown-item>Sub Options 1</vs-dropdown-item>
                  <vs-dropdown-item>Sub Options 2</vs-dropdown-item>

                  <vs-dropdown-group vs-collapse>
                    <vs-dropdown-item vs-label="Sub Collapse">Sub Collapse 1</vs-dropdown-item>
                    <vs-dropdown-item>Sub Collapse 2</vs-dropdown-item>
                  </vs-dropdown-group>
                </vs-dropdown-group>
              </vs-dropdown-group>

              <vs-dropdown-item divider>Option 3</vs-dropdown-item>
            </vs-dropdown-menu>
          </vs-dropdown>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="opgrpdropdown">
          <vs-prism>
            &lt;div class=&quot;examplex&quot;&gt;
            &lt;vs-dropdown&gt;
            &lt;a class=&quot;a-icon&quot; href.prevent&gt;
            Dropdown Option Group
            &lt;vs-icon class=&quot;&quot; icon=&quot;expand_more&quot;&gt;&lt;/vs-icon&gt;
            &lt;/a&gt;
            &lt;vs-dropdown-menu&gt;
            &lt;vs-dropdown-item&gt;
            Option 1
            &lt;/vs-dropdown-item&gt;
            &lt;vs-dropdown-item&gt;
            Option 2
            &lt;/vs-dropdown-item&gt;
            &lt;vs-dropdown-group&gt;
            &lt;vs-dropdown-item&gt;
            Option 1
            &lt;/vs-dropdown-item&gt;
            &lt;vs-dropdown-item&gt;
            Option 2
            &lt;/vs-dropdown-item&gt;
            &lt;vs-dropdown-group&gt;
            &lt;vs-dropdown-item&gt;
            sub Options 1
            &lt;/vs-dropdown-item&gt;
            &lt;vs-dropdown-item&gt;
            sub Options 2
            &lt;/vs-dropdown-item&gt;
            &lt;/vs-dropdown-group&gt;
            &lt;/vs-dropdown-group&gt;
            &lt;vs-dropdown-item divider&gt;
            Option 3
            &lt;/vs-dropdown-item&gt;
            &lt;/vs-dropdown-menu&gt;
            &lt;/vs-dropdown&gt;
            &lt;vs-dropdown &gt;
            &lt;a class=&quot;a-icon&quot; href.prevent&gt;
            Dropdown Group Collapse
            &lt;vs-icon class=&quot;&quot; icon=&quot;expand_more&quot;&gt;&lt;/vs-icon&gt;
            &lt;/a&gt;
            &lt;vs-dropdown-menu&gt;
            &lt;vs-dropdown-item to=&quot;/components/&quot;&gt;
            Option 1
            &lt;/vs-dropdown-item&gt;
            &lt;vs-dropdown-item&gt;
            Option 2
            &lt;/vs-dropdown-item&gt;
            &lt;vs-dropdown-group vs-collapse vs-label=&quot;Group Collapse&quot; vs-icon=&quot;add&quot;&gt;
            &lt;vs-dropdown-item&gt;
            Option Collapse 1
            &lt;/vs-dropdown-item&gt;
            &lt;vs-dropdown-item &gt;
            Option Collapse 2
            &lt;/vs-dropdown-item&gt;
            &lt;vs-dropdown-group&gt;
            &lt;vs-dropdown-item&gt;
            Sub Options 1
            &lt;/vs-dropdown-item&gt;
            &lt;vs-dropdown-item&gt;
            Sub Options 2
            &lt;/vs-dropdown-item&gt;
            &lt;vs-dropdown-group vs-collapse&gt;
            &lt;vs-dropdown-item vs-label=&quot;Sub Collapse&quot;&gt;
            Sub Collapse 1
            &lt;/vs-dropdown-item&gt;
            &lt;vs-dropdown-item&gt;
            Sub Collapse 2
            &lt;/vs-dropdown-item&gt;
            &lt;/vs-dropdown-group&gt;
            &lt;/vs-dropdown-group&gt;
            &lt;/vs-dropdown-group&gt;
            &lt;vs-dropdown-item divider&gt;
            Option 3
            &lt;/vs-dropdown-item&gt;
            &lt;/vs-dropdown-menu&gt;
            &lt;/vs-dropdown&gt;
            &lt;/div&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Dropdown Custom Content
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Dropdown Custom Content
          <vs-button class="ml-auto p-0" @click="logindropdown=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          Sometimes when we need something more personalized and not necessarily a menu for it you can add any content and have the dropdown functionality with the property
          <code>vs-custom-content</code>
        </p>

        <div class>
          <vs-dropdown vs-custom-content vs-trigger-click>
            <a class="a-icon" href.prevent>
              Click me open login
              <vs-icon class icon="expand_more"></vs-icon>
            </a>

            <vs-dropdown-menu class="loginx">
              <div class="p-3">
                <div class="text-center">
                  <h3>Login</h3>
                  <p class="text-muted">Welcome to vuesax, add your data to enter</p>
                </div>

                <vs-input
                  :valid.sync="valid.email"
                  success-text="Correo Valido"
                  class="w-100 mb-2"
                  danger-text="The email does not meet the requirements"
                  type="email"
                  label-placeholder="Email"
                  v-model="value1"
                />

                <vs-input
                  :valid.sync="valid.password"
                  success-text="Password Valida"
                  danger-text="The password must have at least 8 characters, 1 number, 1 special character"
                  type="password"
                  class="mb-3"
                  label-placeholder="Password"
                  v-model="value2"
                />

                <vs-button width="100%" color="primary" type="gradient" class="w-100">Login</vs-button>
              </div>
            </vs-dropdown-menu>
          </vs-dropdown>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="logindropdown">
          <vs-prism>
            &lt;div class=&quot;&quot;&gt;
            &lt;vs-dropdown vs-custom-content vs-trigger-click &gt;
            &lt;a class=&quot;a-icon&quot; href.prevent&gt;
            Click me open login
            &lt;vs-icon class=&quot;&quot; icon=&quot;expand_more&quot;&gt;&lt;/vs-icon&gt;
            &lt;/a&gt;
            &lt;vs-dropdown-menu class=&quot;loginx&quot;&gt;
            &lt;h3&gt;Login&lt;/h3&gt;
            &lt;p&gt;Welcome to vuesax, add your data to enter&lt;/p&gt;
            &lt;vs-input
            :valid.sync=&quot;valid.email&quot;
            success-text=&quot;Correo Valido&quot;
            danger-text=&quot;The email does not meet the requirements&quot;
            type=&quot;email&quot; label-placeholder=&quot;Email&quot; v-model=&quot;value1&quot;/&gt;
            &lt;vs-input
            :valid.sync=&quot;valid.password&quot;
            success-text=&quot;Password Valida&quot;
            danger-text=&quot;The password must have at least 8 characters, 1 number, 1 special character&quot;
            type=&quot;password&quot;
            label-placeholder=&quot;Password&quot; v-model=&quot;value2&quot;/&gt;
            &lt;vs-button width=&quot;100%&quot; color=&quot;success&quot; type=&quot;gradient&quot;&gt;Login&lt;/vs-button&gt;
            &lt;/vs-dropdown-menu&gt;
            &lt;/vs-dropdown&gt;
            &lt;/div&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Dropdown Button
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Dropdown Button
          <vs-button class="ml-auto p-0" @click="dropdownbtn=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p
          class="card-subtitle"
        >You can customize the component or element that initialize the dropdown in this case, it is a Button that is the most common</p>

        <div class="d-flex align-items-center">
          <div class="d-flex align-items-center dropdownbtn-alignment">
            <vs-button class="btnx" type="filled">Dropdown</vs-button>
            <vs-dropdown>
              <vs-button class="btn-drop" type="filled" icon="expand_more"></vs-button>
              <!-- <a href="#">Hola mundo</a> -->

              <vs-dropdown-menu>
                <vs-dropdown-item>option 1</vs-dropdown-item>
                <vs-dropdown-item>option 2</vs-dropdown-item>
                <vs-dropdown-group>
                  <vs-dropdown-item>option 1</vs-dropdown-item>
                  <vs-dropdown-item>option 2</vs-dropdown-item>
                </vs-dropdown-group>
                <vs-dropdown-item divider>option 3</vs-dropdown-item>
              </vs-dropdown-menu>
            </vs-dropdown>
          </div>

          <div class="d-flex align-items-center ml-4 dropdownbtn-alignment">
            <vs-button class="btnx" color="success" type="gradient">Dropdown</vs-button>
            <vs-dropdown>
              <vs-button class="btn-drop" color="success" type="gradient" icon="more_horiz"></vs-button>
              <!-- <a href="#">Hola mundo</a> -->

              <vs-dropdown-menu>
                <vs-dropdown-item>Home</vs-dropdown-item>
                <vs-dropdown-item>Contributors</vs-dropdown-item>
                <vs-dropdown-item divider>Logout</vs-dropdown-item>
              </vs-dropdown-menu>
            </vs-dropdown>
          </div>

          <div class="d-flex align-items-center ml-4 dropdownbtn-alignment">
            <vs-button class="btnx" type="line" color="danger">Icons</vs-button>
            <vs-dropdown>
              <vs-button class="btn-drop" type="line" color="danger" icon="mood"></vs-button>
              <!-- <a href="#">Hola mundo</a> -->

              <vs-dropdown-menu>
                <vs-dropdown-item>
                  <vs-icon class icon="mood"></vs-icon>
                </vs-dropdown-item>
                <vs-dropdown-item>
                  <vs-icon class icon="mood_bad"></vs-icon>
                </vs-dropdown-item>
                <vs-dropdown-item>
                  <vs-icon class icon="sentiment_dissatisfied"></vs-icon>
                </vs-dropdown-item>
                <vs-dropdown-item>
                  <vs-icon class icon="sentiment_satisfied"></vs-icon>
                </vs-dropdown-item>
                <vs-dropdown-item>
                  <vs-icon class icon="sentiment_very_dissatisfied"></vs-icon>
                </vs-dropdown-item>
                <vs-dropdown-item>
                  <vs-icon class icon="sentiment_very_satisfied"></vs-icon>
                </vs-dropdown-item>
              </vs-dropdown-menu>
            </vs-dropdown>
          </div>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="dropdownbtn">
          <vs-prism>
            &lt;div class=&quot;d-flex align-items-center&quot;&gt;
            &lt;div class=&quot;d-flex align-items-center dropdownbtn-alignment&quot;&gt;
            &lt;vs-button class=&quot;btnx&quot; type=&quot;filled&quot;&gt;Dropdown&lt;/vs-button&gt;
            &lt;vs-dropdown&gt;
            &lt;vs-button class=&quot;btn-drop&quot; type=&quot;filled&quot; icon=&quot;expand_more&quot;&gt;&lt;/vs-button&gt;
            &lt;!-- &lt;a href=&quot;#&quot;&gt;Hola mundo&lt;/a&gt; --&gt;
            &lt;vs-dropdown-menu&gt;
            &lt;vs-dropdown-item&gt;
            option 1
            &lt;/vs-dropdown-item&gt;
            &lt;vs-dropdown-item&gt;
            option 2
            &lt;/vs-dropdown-item&gt;
            &lt;vs-dropdown-group &gt;
            &lt;vs-dropdown-item&gt;
            option 1
            &lt;/vs-dropdown-item&gt;
            &lt;vs-dropdown-item&gt;
            option 2
            &lt;/vs-dropdown-item&gt;
            &lt;/vs-dropdown-group&gt;
            &lt;vs-dropdown-item divider&gt;
            option 3
            &lt;/vs-dropdown-item&gt;
            &lt;/vs-dropdown-menu&gt;
            &lt;/vs-dropdown&gt;
            &lt;/div&gt;
            &lt;div class=&quot;d-flex align-items-center ml-4 dropdownbtn-alignment&quot;&gt;
            &lt;vs-button class=&quot;btnx&quot; color=&quot;success&quot; type=&quot;gradient&quot;&gt;Dropdown&lt;/vs-button&gt;
            &lt;vs-dropdown&gt;
            &lt;vs-button class=&quot;btn-drop&quot; color=&quot;success&quot; type=&quot;gradient&quot; icon=&quot;more_horiz&quot;&gt;&lt;/vs-button&gt;
            &lt;!-- &lt;a href=&quot;#&quot;&gt;Hola mundo&lt;/a&gt; --&gt;
            &lt;vs-dropdown-menu&gt;
            &lt;vs-dropdown-item&gt;
            Home
            &lt;/vs-dropdown-item&gt;
            &lt;vs-dropdown-item&gt;
            Contributors
            &lt;/vs-dropdown-item&gt;
            &lt;vs-dropdown-item divider&gt;
            Logout
            &lt;/vs-dropdown-item&gt;
            &lt;/vs-dropdown-menu&gt;
            &lt;/vs-dropdown&gt;
            &lt;/div&gt;
            &lt;div class=&quot;d-flex align-items-center ml-4 dropdownbtn-alignment&quot;&gt;
            &lt;vs-button class=&quot;btnx&quot; type=&quot;line&quot; color=&quot;danger&quot;&gt;Icons&lt;/vs-button&gt;
            &lt;vs-dropdown&gt;
            &lt;vs-button class=&quot;btn-drop&quot; type=&quot;line&quot; color=&quot;danger&quot; icon=&quot;mood&quot;&gt;&lt;/vs-button&gt;
            &lt;!-- &lt;a href=&quot;#&quot;&gt;Hola mundo&lt;/a&gt; --&gt;
            &lt;vs-dropdown-menu&gt;
            &lt;vs-dropdown-item&gt;
            &lt;vs-icon class=&quot;&quot; icon=&quot;mood&quot;&gt;&lt;/vs-icon&gt;
            &lt;/vs-dropdown-item&gt;
            &lt;vs-dropdown-item&gt;
            &lt;vs-icon class=&quot;&quot; icon=&quot;mood_bad&quot;&gt;&lt;/vs-icon&gt;
            &lt;/vs-dropdown-item&gt;
            &lt;vs-dropdown-item&gt;
            &lt;vs-icon class=&quot;&quot; icon=&quot;sentiment_dissatisfied&quot;&gt;&lt;/vs-icon&gt;
            &lt;/vs-dropdown-item&gt;
            &lt;vs-dropdown-item&gt;
            &lt;vs-icon class=&quot;&quot; icon=&quot;sentiment_satisfied&quot;&gt;&lt;/vs-icon&gt;
            &lt;/vs-dropdown-item&gt;
            &lt;vs-dropdown-item&gt;
            &lt;vs-icon class=&quot;&quot; icon=&quot;sentiment_very_dissatisfied&quot;&gt;&lt;/vs-icon&gt;
            &lt;/vs-dropdown-item&gt;
            &lt;vs-dropdown-item&gt;
            &lt;vs-icon class=&quot;&quot; icon=&quot;sentiment_very_satisfied&quot;&gt;&lt;/vs-icon&gt;
            &lt;/vs-dropdown-item&gt;
            &lt;/vs-dropdown-menu&gt;
            &lt;/vs-dropdown&gt;
            &lt;/div&gt;
            &lt;/div&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>
    </vs-col>
  </vs-row>
</template>

<script>
export default {
  name: "dropdown",
  data: () => ({
    title: "Dropdown",
    defaultdropdown: false,
    colordropdown: false,
    colorx: "#c80948",
    opgrpdropdown: false,
    logindropdown: false,
    value1: "",
    value2: "",
    valid: {
      email: false,
      password: false
    },
    dropdownbtn: false
  }),
  methods: {
    
  }
};
</script>