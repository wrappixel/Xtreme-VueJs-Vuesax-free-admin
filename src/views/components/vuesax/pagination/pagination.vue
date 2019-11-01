<template>
  <vs-row vs-justify="center">
    <vs-col type="flex" vs-justify="center" vs-align="center" vs-lg="12" vs-xs="12">
      <!--
		/////////////////
		Default Pagination
		/////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Default Pagination
          <vs-button class="ml-auto p-0" @click="defaultpage=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p
          class="card-subtitle"
        >The pagination component consists of several elements, all of which are optional. So with no extra class, your pagination links will look as follow :</p>

        <div>
          <vs-pagination :total="40" v-model="currentx"></vs-pagination>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="defaultpage">
          <vs-prism>
            &lt;template&gt;
            &lt;div&gt;
            &lt;vs-pagination :total=&quot;40&quot; v-model=&quot;currentx&quot;&gt;&lt;/vs-pagination&gt;
            &lt;/div&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            data: () =&gt; ({
            currentx: 14
            })
            }
            &lt;/script&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
		/////////////////
		Icon Pagination
		/////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Icon Pagination
          <vs-button class="ml-auto p-0" @click="iconpage=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          To customize the previous and next page icons change the value of the
          <code>prev-icon</code> and
          <code>prev-icon</code> directives. By default, their values are respectively arrow_back and arrow_forward.
        </p>

        <div>
          <vs-pagination
            :total="100"
            v-model="iconpageination"
            prev-icon="arrow_back"
            next-icon="arrow_forward"
          ></vs-pagination>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="iconpage">
          <vs-prism>
            &lt;template&gt;
            &lt;div&gt;
            &lt;vs-pagination :total=&quot;100&quot; v-model=&quot;currentx&quot; prev-icon=&quot;arrow_back&quot; next-icon=&quot;arrow_forward&quot;&gt;&lt;/vs-pagination&gt;
            &lt;/div&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            data: () =&gt; ({
            currentx: 64
            })
            }
            &lt;/script&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
		/////////////////
		Limit the amount of links shown
		/////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Limit the amount of links shown
          <vs-button class="ml-auto p-0" @click="limitpage=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          By default Vuesax will show a maximum of 9 links. This default behaviour can be changed by setting the
          <code>max</code> directive to a different integer value.
        </p>

        <div>
          <vs-pagination :total="30" v-model="limitx" :max="13"></vs-pagination>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="limitpage">
          <vs-prism>
            &lt;template&gt;
            &lt;div&gt;
            &lt;vs-pagination :total=&quot;30&quot; v-model=&quot;currentx&quot; :max=&quot;13&quot;&gt;&lt;/vs-pagination&gt;
            &lt;/div&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            data: () =&gt; ({
            currentx: 17
            })
            }
            &lt;/script&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
		/////////////////
		Goto Pagination
		/////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Goto Pagination
          <vs-button class="ml-auto p-0" @click="gotopage=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          The
          <code>goto</code> directive will allow users to directly jump to a desired page.
        </p>

        <div>
          <vs-pagination :total="20" v-model="gotox" goto></vs-pagination>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="gotopage">
          <vs-prism>
            &lt;template&gt;
            &lt;div&gt;
            &lt;vs-pagination :total=&quot;20&quot; v-model=&quot;currentx&quot; goto &gt;&lt;/vs-pagination&gt;
            &lt;/div&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            data: () =&gt; ({
            currentx: 8
            })
            }
            &lt;/script&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
		/////////////////
		Color Pagination
		/////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Color Pagination
          <vs-button class="ml-auto p-0" @click="colorpage=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can change the color of the component with the property
          <code>color</code>, you can use the Main colors or RGB and HEX colors
        </p>

        <div class="d-flex align-items-center">
          <input class="input-color mr-3" v-model="colorx" type="color" />
          <vs-pagination :color="colorx" :total="20" v-model="colorp"></vs-pagination>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="colorpage">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;div class=&quot;centerx&quot;&gt;
            &lt;input class=&quot;input-color&quot; v-model=&quot;colorx&quot; type=&quot;color&quot;&gt;
            &lt;vs-pagination :color=&quot;colorx&quot; :total=&quot;20&quot; v-model=&quot;currentx&quot;&gt;&lt;/vs-pagination&gt;
            &lt;/div&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            data: ()=&gt;({
            colorx: '#f91f43',
            currentx: 7
            })
            }
            &lt;/script&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
		/////////////////
		Programmatic Inc/Dec Pagination
		/////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Programmatic Inc/Dec Pagination
          <vs-button class="ml-auto p-0" @click="colorpage=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p
          class="card-subtitle"
        >You can also update page number from outside of pagination component.</p>

        <div class="btn-alignment">
          <p>Current: {{ currentx }}</p>
          <vs-button @click="currentx++">Increment</vs-button>
          <vs-button @click="currentx--">Decrement</vs-button>
          <br />
          <br />
          <vs-pagination :total="20" v-model="icdec"></vs-pagination>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="colorpage">
          <vs-prism>
            &lt;template&gt;
            &lt;div&gt;
            &lt;p&gt;Current: {{ currentx }}&lt;/p&gt;
            &lt;vs-button @click=&quot;currentx++&quot;&gt;Increment&lt;/vs-button&gt;
            &lt;vs-button @click=&quot;currentx--&quot;&gt;Decrement&lt;/vs-button&gt;
            &lt;br&gt;&lt;br&gt;
            &lt;vs-pagination :total=&quot;20&quot; v-model=&quot;currentx&quot;&gt;&lt;/vs-pagination&gt;
            &lt;/div&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            data: () =&gt; ({
            currentx: 5
            })
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
  name: "pagination",
  data: () => ({
    title: "Pagination",
    defaultpage: false,
    currentx: 14,
    iconpage: false,
    iconpageination: 64,
    limitpage: false,
    limitx: 17,
    gotopage: false,
    gotox: 12,
    colorpage: false,
    colorx: "#f91f43",
    colorp: 7,
    icdec: 5
  })
};
</script>

