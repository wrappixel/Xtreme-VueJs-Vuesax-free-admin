<template>
  <vs-row vs-justify="center">
    <vs-col type="flex" vs-justify="center" vs-align="center" vs-lg="12" vs-xs="12">
      <!--
		/////////////////
		Default Textarea
		/////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Default Textarea
          <vs-button class="ml-auto p-0" @click="defaulttextarea=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          To add a Textarea we have the component
          <code>vs-textarea</code>
        </p>

        <div>
          <vs-textarea v-model="textarea" />
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="defaulttextarea">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;div&gt;
            &lt;vs-textarea v-model=&quot;textarea&quot; /&gt;
            &lt;/div&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            data:()=&gt;({
            textarea: '',
            })
            }
            &lt;/script&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Default Label
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Default Label
          <vs-button class="ml-auto p-0" @click="defaultlabeltext=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          If you need to add a label you can use the
          <code>label</code> property
        </p>

        <div>
          <vs-textarea label="Label in Textarea" v-model="textarea2" />
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="defaultlabeltext">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;div&gt;
            &lt;vs-textarea label=&quot;Label in Textarea&quot; v-model=&quot;textarea&quot; /&gt;
            &lt;/div&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            data:()=&gt;({
            textarea: '',
            })
            }
            &lt;/script&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Counter Textarea
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Counter Textarea
          <vs-button class="ml-auto p-0" @click="coutertext=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          There are times when we need the user to only enter a certain number of characters for it, we have the property
          <code>counter</code>, the value is a number and determines the maximum
        </p>

        <div>
          <vs-textarea
            counter="20"
            label="Counter: 20"
            :counter-danger.sync="counterDanger"
            v-model="textarea3"
          />
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="coutertext">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;div&gt;
            &lt;vs-textarea counter=&quot;20&quot; label=&quot;Counter: 20&quot; :counter-danger.sync=&quot;counterDanger&quot; v-model=&quot;textarea&quot; /&gt;
            &lt;/div&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            data:()=&gt;({
            textarea: '',
            counterDanger: false
            })
            }
            &lt;/script&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Width Textarea
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Width Textarea
          <vs-button class="ml-auto p-0" @click="widthtextarea=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can set the width of the textarea width the
          <code>width</code> property.
        </p>

        <div>
          <vs-textarea label="Width set to 300px" width="300px" />
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="widthtextarea">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;div&gt;
            &lt;vs-textarea label=&quot;Width set to 300px&quot; width=&quot;300px&quot; /&gt;
            &lt;/div&gt;
            &lt;/template&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Height Textarea
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Height Textarea
          <vs-button class="ml-auto p-0" @click="heighttextarea=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can set the height of the textarea with the
          <code>height</code> property.
        </p>

        <div>
          <vs-textarea label="Height set to 200px" height="200px" />
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="heighttextarea">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;div&gt;
            &lt;vs-textarea label=&quot;Height set to 200px&quot; height=&quot;200px&quot; /&gt;
            &lt;/div&gt;
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
  name: "textarea",
  data: () => ({
    title: "Textarea",
    defaulttextarea: false,
    textarea: "",
    textarea2: "",
    textarea3: "",
    defaultlabeltext: false,
    coutertext: false,
    counterDanger: false,
    widthtextarea: false,
    heighttextarea: false
  })
};
</script>