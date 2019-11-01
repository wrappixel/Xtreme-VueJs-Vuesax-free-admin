<template>
  <vs-row vs-justify="center">
    <vs-col type="flex" vs-justify="center" vs-align="center" vs-lg="12" vs-xs="12">
      <!--
		/////////////////
		Default Tabs
		/////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Default Tabs
          <vs-button class="ml-auto p-0" @click="defaulttabs=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          To implement a tabs, use the
          <code>vs-tabs</code> component. It must include
          <code>vs-tab</code> child components that represent each tab.
        </p>

        <vs-tabs>
          <vs-tab label="Home">
            <div class="con-tab-ejemplo">Home</div>
          </vs-tab>
          <vs-tab label="Service">
            <div class="con-tab-ejemplo">Service</div>
          </vs-tab>
          <vs-tab label="login">
            <div class="con-tab-ejemplo">login</div>
          </vs-tab>
          <vs-tab disabled label="Disabled">
            <div class="con-tab-ejemplo">Disabled</div>
          </vs-tab>
          <vs-tab label="Lorem ipsum dolor sit amet">
            <div class="con-tab-ejemplo">Lorem ipsum dolor sit amet</div>
          </vs-tab>
        </vs-tabs>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="defaulttabs">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;div class=&quot;&quot;&gt;
            &lt;vs-tabs&gt;
            &lt;vs-tab label=&quot;Home&quot;&gt;
            &lt;div class=&quot;con-tab-ejemplo&quot;&gt;
            Home
            &lt;/div&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab label=&quot;Service&quot;&gt;
            &lt;div class=&quot;con-tab-ejemplo&quot;&gt;
            Service
            &lt;/div&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab label=&quot;login&quot;&gt;
            &lt;div class=&quot;con-tab-ejemplo&quot;&gt;
            login
            &lt;/div&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab disabled label=&quot;Disabled&quot;&gt;
            &lt;div class=&quot;con-tab-ejemplo&quot;&gt;
            Disabled
            &lt;/div&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab label=&quot;Lorem ipsum dolor sit amet&quot;&gt;
            &lt;div class=&quot;con-tab-ejemplo&quot;&gt;
            Lorem ipsum dolor sit amet
            &lt;/div&gt;
            &lt;/vs-tab&gt;
            &lt;/vs-tabs&gt;
            &lt;/div&gt;
            &lt;/template&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Color Tabs
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Color Tabs
          <vs-button class="ml-auto p-0" @click="colortabs=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can change the color of the component with the property
          <code>color</code>, the parameter allows the main colors and HEX or RGB
        </p>

        <vs-tabs :color="colorx">
          <vs-tab @click="colorx = 'success'" label="Success">
            <div class="con-tab-ejemplo">Success</div>
          </vs-tab>
          <vs-tab @click="colorx = 'danger'" label="Danger">
            <div class="con-tab-ejemplo">Danger</div>
          </vs-tab>
          <vs-tab @click="colorx = 'warning'" label="Warning">
            <div class="con-tab-ejemplo">Warning</div>
          </vs-tab>
          <vs-tab @click="colorx = 'dark'" label="Dark">
            <div class="con-tab-ejemplo">Dark</div>
          </vs-tab>
          <vs-tab @click="colorx = 'rgb(16, 233, 179)'" label="RGB | HEX">
            <div class="con-tab-ejemplo">RGB | HEX</div>
          </vs-tab>
        </vs-tabs>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="colortabs">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;div&gt;
            &lt;vs-tabs :color=&quot;colorx&quot;&gt;
            &lt;vs-tab @click=&quot;colorx = 'success'&quot; label=&quot;Success&quot;&gt;
            &lt;div class=&quot;con-tab-ejemplo&quot;&gt;
            Success
            &lt;/div&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab @click=&quot;colorx = 'danger'&quot; label=&quot;Danger&quot;&gt;
            &lt;div class=&quot;con-tab-ejemplo&quot;&gt;
            Danger
            &lt;/div&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab @click=&quot;colorx = 'warning'&quot; label=&quot;Warning&quot;&gt;
            &lt;div class=&quot;con-tab-ejemplo&quot;&gt;
            Warning
            &lt;/div&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab @click=&quot;colorx = 'dark'&quot; label=&quot;Dark&quot;&gt;
            &lt;div class=&quot;con-tab-ejemplo&quot;&gt;
            Dark
            &lt;/div&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab @click=&quot;colorx = 'rgb(16, 233, 179)'&quot; label=&quot;RGB | HEX&quot;&gt;
            &lt;div class=&quot;con-tab-ejemplo&quot;&gt;
            RGB | HEX
            &lt;/div&gt;
            &lt;/vs-tab&gt;
            &lt;/vs-tabs&gt;
            &lt;/div&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            data:()=&gt;({
            colorx:'success'
            }),
            }
            &lt;/script&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Alignments Tabs
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Alignments Tabs
          <vs-button class="ml-auto p-0" @click="aligntabs=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          Change the alignment of the buttons with the property alignments. The allowed values are
        </p>
        <ul class="list-group list-group-horizontal mb-3">
          <li class="list-group-item rounded-0 py-2">
            <span>center</span>
          </li>
          <li class="list-group-item rounded-0 py-2">
            <span>right</span>
          </li>
          <li class="list-group-item rounded-0 py-2">
            <span>fixed</span>
          </li>
        </ul>

        <vs-card>
          <h3>Default</h3>
          <hr />
          <vs-tabs>
            <vs-tab label="Home">
              <div></div>
            </vs-tab>
            <vs-tab label="Documents">
              <div></div>
            </vs-tab>
            <vs-tab label="Contributors">
              <div></div>
            </vs-tab>
            <vs-tab label="Ecosistem">
              <div></div>
            </vs-tab>
          </vs-tabs>

          <h3>Center</h3>
          <hr />
          <vs-tabs alignment="center">
            <vs-tab label="Home">
              <div></div>
            </vs-tab>
            <vs-tab label="Documents">
              <div></div>
            </vs-tab>
            <vs-tab label="Contributors">
              <div></div>
            </vs-tab>
            <vs-tab label="Ecosistem">
              <div></div>
            </vs-tab>
          </vs-tabs>

          <h3>Right</h3>
          <hr />
          <vs-tabs alignment="right">
            <vs-tab label="Home">
              <div></div>
            </vs-tab>
            <vs-tab label="Documents">
              <div></div>
            </vs-tab>
            <vs-tab label="Contributors">
              <div></div>
            </vs-tab>
            <vs-tab label="Ecosistem">
              <div></div>
            </vs-tab>
          </vs-tabs>

          <h3>Fixed</h3>
          <hr />
          <vs-tabs alignment="fixed">
            <vs-tab label="Home">
              <div></div>
            </vs-tab>
            <vs-tab label="Documents">
              <div></div>
            </vs-tab>
            <vs-tab label="Contributors">
              <div></div>
            </vs-tab>
            <vs-tab label="Ecosistem">
              <div></div>
            </vs-tab>
          </vs-tabs>
        </vs-card>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="aligntabs">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;div class=&quot;&quot;&gt;
            &lt;h3&gt;
            Default
            &lt;/h3&gt;
            &lt;vs-tabs&gt;
            &lt;vs-tab label=&quot;Home&quot;&gt;
            &lt;div&gt;
            &lt;/div&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab label=&quot;Documents&quot;&gt;
            &lt;div&gt;
            &lt;/div&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab label=&quot;Contributors&quot;&gt;
            &lt;div&gt;
            &lt;/div&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab label=&quot;Ecosistem&quot;&gt;
            &lt;div&gt;
            &lt;/div&gt;
            &lt;/vs-tab&gt;
            &lt;/vs-tabs&gt;
            &lt;h3&gt;
            Center
            &lt;/h3&gt;
            &lt;vs-tabs alignment=&quot;center&quot;&gt;
            &lt;vs-tab label=&quot;Home&quot;&gt;
            &lt;div&gt;
            &lt;/div&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab label=&quot;Documents&quot;&gt;
            &lt;div&gt;
            &lt;/div&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab label=&quot;Contributors&quot;&gt;
            &lt;div&gt;
            &lt;/div&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab label=&quot;Ecosistem&quot;&gt;
            &lt;div&gt;
            &lt;/div&gt;
            &lt;/vs-tab&gt;
            &lt;/vs-tabs&gt;
            &lt;h3&gt;
            Right
            &lt;/h3&gt;
            &lt;vs-tabs alignment=&quot;right&quot;&gt;
            &lt;vs-tab label=&quot;Home&quot;&gt;
            &lt;div&gt;
            &lt;/div&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab label=&quot;Documents&quot;&gt;
            &lt;div&gt;
            &lt;/div&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab label=&quot;Contributors&quot;&gt;
            &lt;div&gt;
            &lt;/div&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab label=&quot;Ecosistem&quot;&gt;
            &lt;div&gt;
            &lt;/div&gt;
            &lt;/vs-tab&gt;
            &lt;/vs-tabs&gt;
            &lt;h3&gt;
            Fixed
            &lt;/h3&gt;
            &lt;vs-tabs alignment=&quot;fixed&quot;&gt;
            &lt;vs-tab label=&quot;Home&quot;&gt;
            &lt;div&gt;
            &lt;/div&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab label=&quot;Documents&quot;&gt;
            &lt;div&gt;
            &lt;/div&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab label=&quot;Contributors&quot;&gt;
            &lt;div&gt;
            &lt;/div&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab label=&quot;Ecosistem&quot;&gt;
            &lt;div&gt;
            &lt;/div&gt;
            &lt;/vs-tab&gt;
            &lt;/vs-tabs&gt;
            &lt;/div&gt;
            &lt;/template&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Position Tabs
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Position Tabs
          <vs-button class="ml-auto p-0" @click="postabs=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can change the position of the menu with the property
          <code>vs-position</code> that as a value you can have:
          <code>top, right,bottom, left</code>.
        </p>

        <vs-tabs color="rgb(32, 201, 192)">
          <vs-tab label="Top">
            <!-- top -->
            <vs-tabs>
              <vs-tab label="Home">
                <span>Jujubes gingerbread cake pastry biscuit jelly-o marshmallow. Chocolate cake jelly marshmallow topping. Danish caramels gummies tootsie roll marshmallow sweet croissant.</span>
              </vs-tab>
              <vs-tab label="Service">
                <span>Halvah dessert fruitcake toffee oat cake tart oat cake topping jelly beans. Pudding sweet pie pastry lemon drops jujubes danish pie gingerbread. Liquorice powder wafer.</span>
              </vs-tab>
              <vs-tab label="login">
                <span>Chocolate icing pie danish gummies. Dragée gummies toffee muffin chocolate bar marshmallow. Marshmallow chupa chups muffin cake icing pastry wafer.</span>
              </vs-tab>
              <vs-tab disabled label="Disabled">
                <span>Macaroon icing lemon drops jelly-o. Bonbon pie tart chocolate bar pastry. Sugar plum bonbon candy canes dragée toffee dragée toffee.</span>
              </vs-tab>
            </vs-tabs>
          </vs-tab>

          <vs-tab label="Right">
            <!-- right -->
            <vs-tabs position="right" color="rgb(29, 55, 194)">
              <vs-tab label="Home">
                <span>Jujubes gingerbread cake pastry biscuit jelly-o marshmallow. Chocolate cake jelly marshmallow topping. Danish caramels gummies tootsie roll marshmallow sweet croissant.</span>
              </vs-tab>
              <vs-tab label="Service">
                <span>Halvah dessert fruitcake toffee oat cake tart oat cake topping jelly beans. Pudding sweet pie pastry lemon drops jujubes danish pie gingerbread. Liquorice powder wafer.</span>
              </vs-tab>
              <vs-tab label="login">
                <span>Chocolate icing pie danish gummies. Dragée gummies toffee muffin chocolate bar marshmallow. Marshmallow chupa chups muffin cake icing pastry wafer.</span>
              </vs-tab>
              <vs-tab disabled label="Disabled">
                <span>Macaroon icing lemon drops jelly-o. Bonbon pie tart chocolate bar pastry. Sugar plum bonbon candy canes dragée toffee dragée toffee.</span>
              </vs-tab>
            </vs-tabs>
          </vs-tab>

          <vs-tab label="Bottom">
            <!-- bottom -->
            <vs-tabs position="bottom" color="rgb(29, 55, 194)">
              <vs-tab label="Home">
                <span>Jujubes gingerbread cake pastry biscuit jelly-o marshmallow. Chocolate cake jelly marshmallow topping. Danish caramels gummies tootsie roll marshmallow sweet croissant.</span>
              </vs-tab>
              <vs-tab label="Service">
                <span>Halvah dessert fruitcake toffee oat cake tart oat cake topping jelly beans. Pudding sweet pie pastry lemon drops jujubes danish pie gingerbread. Liquorice powder wafer.</span>
              </vs-tab>
              <vs-tab label="login">
                <span>Chocolate icing pie danish gummies. Dragée gummies toffee muffin chocolate bar marshmallow. Marshmallow chupa chups muffin cake icing pastry wafer.</span>
              </vs-tab>
              <vs-tab :disabled="true" label="Disabled">
                <span>Macaroon icing lemon drops jelly-o. Bonbon pie tart chocolate bar pastry. Sugar plum bonbon candy canes dragée toffee dragée toffee.</span>
              </vs-tab>
            </vs-tabs>
          </vs-tab>

          <vs-tab label="Left">
            <!-- left -->
            <vs-tabs position="left" color="danger">
              <vs-tab label="Home">
                <span>Jujubes gingerbread cake pastry biscuit jelly-o marshmallow. Chocolate cake jelly marshmallow topping. Danish caramels gummies tootsie roll marshmallow sweet croissant.</span>
              </vs-tab>
              <vs-tab label="Service">
                <span>Halvah dessert fruitcake toffee oat cake tart oat cake topping jelly beans. Pudding sweet pie pastry lemon drops jujubes danish pie gingerbread. Liquorice powder wafer.</span>
              </vs-tab>
              <vs-tab label="login">
                <span>Chocolate icing pie danish gummies. Dragée gummies toffee muffin chocolate bar marshmallow. Marshmallow chupa chups muffin cake icing pastry wafer.</span>
              </vs-tab>
              <vs-tab :disabled="true" label="Disabled">
                <span>Macaroon icing lemon drops jelly-o. Bonbon pie tart chocolate bar pastry. Sugar plum bonbon candy canes dragée toffee dragée toffee.</span>
              </vs-tab>
            </vs-tabs>
          </vs-tab>
        </vs-tabs>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="postabs">
          <vs-prism>
            &lt;vs-tabs color=&quot;rgb(32, 201, 192)&quot;&gt;
            &lt;vs-tab label=&quot;Top&quot;&gt;
            &lt;!-- top --&gt;
            &lt;vs-tabs color=&quot;rgb(201, 32, 178)&quot;&gt;
            &lt;vs-tab label=&quot;Home&quot;&gt;
            &lt;span&gt;Jujubes gingerbread cake pastry biscuit jelly-o marshmallow. Chocolate cake jelly marshmallow topping. Danish caramels gummies tootsie roll marshmallow sweet croissant.&lt;/span&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab label=&quot;Service&quot;&gt;
            &lt;span&gt;Halvah dessert fruitcake toffee oat cake tart oat cake topping jelly beans. Pudding sweet pie pastry lemon drops jujubes danish pie gingerbread. Liquorice powder wafer.&lt;/span&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab label=&quot;login&quot;&gt;
            &lt;span&gt;Chocolate icing pie danish gummies. Drag&eacute;e gummies toffee muffin chocolate bar marshmallow. Marshmallow chupa chups muffin cake icing pastry wafer.&lt;/span&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab disabled label=&quot;Disabled&quot;&gt;
            &lt;span&gt;Macaroon icing lemon drops jelly-o. Bonbon pie tart chocolate bar pastry. Sugar plum bonbon candy canes drag&eacute;e toffee drag&eacute;e toffee.&lt;/span&gt;
            &lt;/vs-tab&gt;
            &lt;/vs-tabs&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab label=&quot;Right&quot;&gt;
            &lt;!-- right --&gt;
            &lt;vs-tabs position=&quot;right&quot; color=&quot;rgb(29, 55, 194)&quot;&gt;
            &lt;vs-tab label=&quot;Home&quot;&gt;
            &lt;span&gt;Jujubes gingerbread cake pastry biscuit jelly-o marshmallow. Chocolate cake jelly marshmallow topping. Danish caramels gummies tootsie roll marshmallow sweet croissant.&lt;/span&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab label=&quot;Service&quot;&gt;
            &lt;span&gt;Halvah dessert fruitcake toffee oat cake tart oat cake topping jelly beans. Pudding sweet pie pastry lemon drops jujubes danish pie gingerbread. Liquorice powder wafer.&lt;/span&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab label=&quot;login&quot;&gt;
            &lt;span&gt;Chocolate icing pie danish gummies. Drag&eacute;e gummies toffee muffin chocolate bar marshmallow. Marshmallow chupa chups muffin cake icing pastry wafer.&lt;/span&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab disabled label=&quot;Disabled&quot;&gt;
            &lt;span&gt;Macaroon icing lemon drops jelly-o. Bonbon pie tart chocolate bar pastry. Sugar plum bonbon candy canes drag&eacute;e toffee drag&eacute;e toffee.&lt;/span&gt;
            &lt;/vs-tab&gt;
            &lt;/vs-tabs&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab label=&quot;Bottom&quot;&gt;
            &lt;!-- bottom --&gt;
            &lt;vs-tabs position=&quot;bottom&quot; color=&quot;rgb(29, 55, 194)&quot;&gt;
            &lt;vs-tab label=&quot;Home&quot;&gt;
            &lt;span&gt;Jujubes gingerbread cake pastry biscuit jelly-o marshmallow. Chocolate cake jelly marshmallow topping. Danish caramels gummies tootsie roll marshmallow sweet croissant.&lt;/span&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab label=&quot;Service&quot;&gt;
            &lt;span&gt;Halvah dessert fruitcake toffee oat cake tart oat cake topping jelly beans. Pudding sweet pie pastry lemon drops jujubes danish pie gingerbread. Liquorice powder wafer.&lt;/span&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab label=&quot;login&quot;&gt;
            &lt;span&gt;Chocolate icing pie danish gummies. Drag&eacute;e gummies toffee muffin chocolate bar marshmallow. Marshmallow chupa chups muffin cake icing pastry wafer.&lt;/span&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab :disabled=&quot;true&quot; label=&quot;Disabled&quot;&gt;
            &lt;span&gt;Macaroon icing lemon drops jelly-o. Bonbon pie tart chocolate bar pastry. Sugar plum bonbon candy canes drag&eacute;e toffee drag&eacute;e toffee.&lt;/span&gt;
            &lt;/vs-tab&gt;
            &lt;/vs-tabs&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab label=&quot;Left&quot;&gt;
            &lt;!-- left --&gt;
            &lt;vs-tabs position=&quot;left&quot; color=&quot;danger&quot;&gt;
            &lt;vs-tab label=&quot;Home&quot;&gt;
            &lt;span&gt;Jujubes gingerbread cake pastry biscuit jelly-o marshmallow. Chocolate cake jelly marshmallow topping. Danish caramels gummies tootsie roll marshmallow sweet croissant.&lt;/span&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab label=&quot;Service&quot;&gt;
            &lt;span&gt;Halvah dessert fruitcake toffee oat cake tart oat cake topping jelly beans. Pudding sweet pie pastry lemon drops jujubes danish pie gingerbread. Liquorice powder wafer.&lt;/span&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab label=&quot;login&quot;&gt;
            &lt;span&gt;Chocolate icing pie danish gummies. Drag&eacute;e gummies toffee muffin chocolate bar marshmallow. Marshmallow chupa chups muffin cake icing pastry wafer.&lt;/span&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab :disabled=&quot;true&quot; label=&quot;Disabled&quot;&gt;
            &lt;span&gt;Macaroon icing lemon drops jelly-o. Bonbon pie tart chocolate bar pastry. Sugar plum bonbon candy canes drag&eacute;e toffee drag&eacute;e toffee.&lt;/span&gt;
            &lt;/vs-tab&gt;
            &lt;/vs-tabs&gt;
            &lt;/vs-tab&gt;
            &lt;/vs-tabs&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Icons Tabs
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Icons Tabs
          <vs-button class="ml-auto p-0" @click="icontabs=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can add a left icon inside each tab with the property
          <code>icon</code> that has the same values as the
          <code>icon</code> component.
        </p>

        <vs-tabs :color="colorx2">
          <vs-tab label="Pets" icon="pets" @click="colorx2 = '#2962ff'"></vs-tab>
          <vs-tab label="Bank" icon="account_balance" @click="colorx2 = '#36bea6'"></vs-tab>
          <vs-tab label="Dashboard" icon="dashboard" @click="colorx2 = '#f62d51'"></vs-tab>
          <vs-tab label="Profile" icon="account_circle" @click="colorx2 = '#ffbc34'"></vs-tab>
        </vs-tabs>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="icontabs">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;div&gt;
            &lt;vs-tabs :color=&quot;colorx&quot;&gt;
            &lt;vs-tab label=&quot;Pets&quot; icon=&quot;pets&quot; @click=&quot;colorx = '#8B0000'&quot;&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab label=&quot;Bank&quot; icon=&quot;account_balance&quot; @click=&quot;colorx = '#FFA500'&quot;&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab label=&quot;Dashboard&quot; icon=&quot;dashboard&quot; @click=&quot;colorx = '#551A8B'&quot;&gt;
            &lt;/vs-tab&gt;
            &lt;vs-tab label=&quot;Profile&quot; icon=&quot;account_circle&quot; @click=&quot;colorx = '#0000FF'&quot;&gt;
            &lt;/vs-tab&gt;
            &lt;/vs-tabs&gt;
            &lt;/div&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            data:()=&gt;({
            colorx: '#8B0000'
            })
            }
            &lt;/script&gt;
            &lt;/template&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>
    </vs-col>
  </vs-row>
</template>

<script>
export default {
  name: "tabs",
  data: () => ({
    title: "Tabs",
    defaulttabs: false,
    colortabs: false,
    colorx: "success",
    aligntabs: false,
    postabs: false,
    icontabs: false,
    colorx2: "primary"
  })
};
</script>