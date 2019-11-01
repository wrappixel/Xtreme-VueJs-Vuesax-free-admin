<template>
  <vs-row vs-justify="center">
    <vs-col type="flex" vs-justify="center" vs-align="center" vs-lg="12" vs-xs="12">
      <!--
        /////////////////
        Default Notification
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Default Notification
          <vs-button class="ml-auto p-0" @click="defaultnotification=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          To add a notification we have the global function
          <code>$vs.notify</code>. The first parameter is a json with all the necessary attributes, or if we only want the standard notification we can only add a string with the text of the notification.
        </p>

        <div class="btn-alignment">
          <vs-button
            @click="$vs.notify({title:'Primary',text:'Lorem ipsum dolor sit amet, consectetur',color:'primary'})"
            color="primary"
            type="flat"
          >Notification Primary</vs-button>
          <vs-button
            @click="$vs.notify({title:'Success',text:'Lorem ipsum dolor sit amet, consectetur',color:'success'})"
            color="success"
            type="flat"
          >Notification Success</vs-button>
          <vs-button
            @click="$vs.notify({title:'Danger',text:'Lorem ipsum dolor sit amet, consectetur',color:'danger'})"
            color="danger"
            type="flat"
          >Notification Danger</vs-button>
          <vs-button
            @click="$vs.notify({title:'Warning',text:'Lorem ipsum dolor sit amet, consectetur',color:'warning'})"
            color="warning"
            type="flat"
          >Notification Warning</vs-button>
          <vs-button
            @click="$vs.notify({title:'dark',text:'Lorem ipsum dolor sit amet, consectetur',color:'dark'})"
            color="dark"
            type="flat"
          >Notification Dark</vs-button>
          <vs-button @click="random()" color="success" type="gradient">Notification Random Color</vs-button>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="defaultnotification">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;div class=&quot;con-notifications&quot;&gt;
            &lt;vs-button @click=&quot;$vs.notify({title:'Default',text:'Lorem ipsum dolor sit amet, consectetur'})&quot; color=&quot;primary&quot; type=&quot;border&quot;&gt;Notification white&lt;/vs-button&gt;
            &lt;vs-button @click=&quot;$vs.notify({title:'Primary',text:'Lorem ipsum dolor sit amet, consectetur',color:'primary'})&quot; color=&quot;primary&quot; type=&quot;flat&quot;&gt;Notification Primary&lt;/vs-button&gt;
            &lt;vs-button @click=&quot;$vs.notify({title:'Success',text:'Lorem ipsum dolor sit amet, consectetur',color:'success'})&quot; color=&quot;success&quot; type=&quot;flat&quot;&gt;Notification Success&lt;/vs-button&gt;
            &lt;vs-button @click=&quot;$vs.notify({title:'Danger',text:'Lorem ipsum dolor sit amet, consectetur',color:'danger'})&quot; color=&quot;danger&quot; type=&quot;flat&quot;&gt;Notification Danger&lt;/vs-button&gt;
            &lt;vs-button @click=&quot;$vs.notify({title:'Warning',text:'Lorem ipsum dolor sit amet, consectetur',color:'warning'})&quot; color=&quot;warning&quot; type=&quot;flat&quot;&gt;Notification Warning&lt;/vs-button&gt;
            &lt;vs-button @click=&quot;$vs.notify({title:'dark',text:'Lorem ipsum dolor sit amet, consectetur',color:'dark'})&quot; color=&quot;dark&quot; type=&quot;flat&quot;&gt;Notification Dark&lt;/vs-button&gt;
            &lt;vs-button @click=&quot;random()&quot; color=&quot;success&quot; type=&quot;gradient&quot;&gt;Notification Random Color&lt;/vs-button&gt;
            &lt;/div&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            methods:{
            random(){
            function getRandomInt(min, max) {
            return Math.floor(Math.random() * (max - min)) + min;
            }
            let color = `rgb(${getRandomInt(0,255)},${getRandomInt(0,255)},${getRandomInt(0,255)})`
            this.$vs.notify({
            title:'Color',
            text:'Lorem ipsum dolor sit amet, consectetur',
            color:color
            })
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
        Notification Position
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Notification Position
          <vs-button class="ml-auto p-0" @click="posnotification=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          We can change the place where the notification appears with the property
          <code>position</code>. A practical example would be:
          <code>position: 'top-right'</code>. The supported values are:
        </p>
        <ul class="list-group list-group-horizontal-lg mb-3">
          <li class="list-group-item rounded-0 py-2">
            <span>top-right</span>
          </li>
          <li class="list-group-item rounded-0 py-2">
            <span>top-left</span>
          </li>
          <li class="list-group-item rounded-0 py-2">
            <span>bottom-left</span>
          </li>
          <li class="list-group-item rounded-0 py-2">
            <span>bottom-center</span>
          </li>
          <li class="list-group-item rounded-0 py-2">
            <span>top-center</span>
          </li>
        </ul>
        <div class="btn-alignment">
          <vs-button
            @click="$vs.notify({title:'Position Default',text:'Lorem ipsum dolor sit amet, consectetur',color:'primary'})"
            color="primary"
            type="flat"
          >Position Default</vs-button>
          <vs-button
            @click="$vs.notify({title:'Position top-right',text:'Lorem ipsum dolor sit amet, consectetur',color:'success',position:'top-right'})"
            color="success"
            type="flat"
          >Position Top Right</vs-button>
          <vs-button
            @click="$vs.notify({title:'Position top-left',text:'Lorem ipsum dolor sit amet, consectetur',color:'danger',position:'top-left'})"
            color="danger"
            type="flat"
          >Position Top Left</vs-button>
          <vs-button
            @click="$vs.notify({title:'Position bottom-left',text:'Lorem ipsum dolor sit amet, consectetur',color:'warning',position:'bottom-left'})"
            color="warning"
            type="flat"
          >Position Bottom Left</vs-button>
          <vs-button
            @click="$vs.notify({title:'Position bottom-center',text:'Lorem ipsum dolor sit amet, consectetur',color:'dark',position:'bottom-center'})"
            color="dark"
            type="flat"
          >Position Bottom Center</vs-button>
          <vs-button
            @click="randomCenter()"
            color="success"
            type="gradient"
          >Position Top Center Random Color</vs-button>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="posnotification">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;div class=&quot;con-notifications-position&quot;&gt;
            &lt;vs-button @click=&quot;$vs.notify({title:'Position Default',text:'Lorem ipsum dolor sit amet, consectetur',color:'primary'})&quot; color=&quot;primary&quot; type=&quot;flat&quot;&gt;Position Default&lt;/vs-button&gt;
            &lt;vs-button @click=&quot;$vs.notify({title:'Position top-right',text:'Lorem ipsum dolor sit amet, consectetur',color:'success',position:'top-right'})&quot; color=&quot;success&quot; type=&quot;flat&quot;&gt;Position Top Right&lt;/vs-button&gt;
            &lt;vs-button @click=&quot;$vs.notify({title:'Position top-left',text:'Lorem ipsum dolor sit amet, consectetur',color:'danger',position:'top-left'})&quot; color=&quot;danger&quot; type=&quot;flat&quot;&gt;Position Top Left&lt;/vs-button&gt;
            &lt;vs-button @click=&quot;$vs.notify({title:'Position bottom-left',text:'Lorem ipsum dolor sit amet, consectetur',color:'warning',position:'bottom-left'})&quot; color=&quot;warning&quot; type=&quot;flat&quot;&gt;Position Bottom Left&lt;/vs-button&gt;
            &lt;vs-button @click=&quot;$vs.notify({title:'Position bottom-center',text:'Lorem ipsum dolor sit amet, consectetur',color:'dark',position:'bottom-center'})&quot; color=&quot;dark&quot; type=&quot;flat&quot;&gt; Position Bottom Center&lt;/vs-button&gt;
            &lt;vs-button @click=&quot;randomCenter()&quot; color=&quot;success&quot; type=&quot;gradient&quot;&gt;Position Top Center Random Color&lt;/vs-button&gt;
            &lt;/div&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            methods:{
            randomCenter(){
            function getRandomInt(min, max) {
            return Math.floor(Math.random() * (max - min)) + min;
            }
            let color = `rgb(${getRandomInt(0,255)},${getRandomInt(0,255)},${getRandomInt(0,255)})`
            this.$vs.notify({title:'Position top-center',text:'Lorem ipsum dolor sit amet, consectetur',color:color,position:'top-center'})
            }
            }
            }
            &lt;/script&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Notification Icon
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Notification Icon
          <vs-button class="ml-auto p-0" @click="iconnotification=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          Notifications can include icons to improve the user experience and to construct a more pleasant and intuitive notification. To make this, use the
          <code>icon</code> property. A practical example would be:
          <code>icon: 'chat'</code>.
        </p>

        <div class="btn-alignment">
          <vs-button
            @click="$vs.notify({title:'Icon mail',text:'Lorem ipsum dolor sit amet, consectetur',color:'primary',icon:'mail'})"
            color="primary"
            type="flat"
          >Icon Mail</vs-button>
          <vs-button
            @click="$vs.notify({title:'Icon mail',text:'Lorem ipsum dolor sit amet, consectetur',color:'success',icon:'check_box'})"
            color="success"
            type="flat"
          >Icon check_box</vs-button>
          <vs-button
            @click="$vs.notify({title:'Icon mail',text:'Lorem ipsum dolor sit amet, consectetur',color:'danger',icon:'favorite'})"
            color="danger"
            type="flat"
          >Icon favorite</vs-button>
          <vs-button
            @click="$vs.notify({title:'Icon mail',text:'Lorem ipsum dolor sit amet, consectetur',color:'warning',icon:'error'})"
            color="warning"
            type="flat"
          >Icon error</vs-button>
          <vs-button
            @click="$vs.notify({title:'Icon mail',text:'Lorem ipsum dolor sit amet, consectetur',color:'dark',icon:'chat'})"
            color="dark"
            type="flat"
          >Icon chat</vs-button>
          <vs-button @click="randomIcon()" color="success" type="gradient">Icon Random Color</vs-button>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="iconnotification">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;div class=&quot;centerx&quot;&gt;
            &lt;vs-button @click=&quot;$vs.notify({title:'Icon mail',text:'Lorem ipsum dolor sit amet, consectetur',color:'primary',icon:'mail'})&quot; color=&quot;primary&quot; type=&quot;flat&quot;&gt;Icon Mail&lt;/vs-button&gt;
            &lt;vs-button @click=&quot;$vs.notify({title:'Icon mail',text:'Lorem ipsum dolor sit amet, consectetur',color:'success',icon:'check_box'})&quot; color=&quot;success&quot; type=&quot;flat&quot;&gt;Icon check_box&lt;/vs-button&gt;
            &lt;vs-button @click=&quot;$vs.notify({title:'Icon mail',text:'Lorem ipsum dolor sit amet, consectetur',color:'danger',icon:'favorite'})&quot; color=&quot;danger&quot; type=&quot;flat&quot;&gt;Icon favorite&lt;/vs-button&gt;
            &lt;vs-button @click=&quot;$vs.notify({title:'Icon mail',text:'Lorem ipsum dolor sit amet, consectetur',color:'warning',icon:'error'})&quot; color=&quot;warning&quot; type=&quot;flat&quot;&gt;Icon error&lt;/vs-button&gt;
            &lt;vs-button @click=&quot;$vs.notify({title:'Icon mail',text:'Lorem ipsum dolor sit amet, consectetur',color:'dark',icon:'chat'})&quot; color=&quot;dark&quot; type=&quot;flat&quot;&gt;Icon chat&lt;/vs-button&gt;
            &lt;vs-button @click=&quot;randomIcon()&quot; color=&quot;success&quot; type=&quot;gradient&quot;&gt;Icon Random Color&lt;/vs-button&gt;
            &lt;/div&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            methods:{
            randomIcon(){
            function getRandomInt(min, max) {
            return Math.floor(Math.random() * (max - min)) + min;
            }
            let color = `rgb(${getRandomInt(0,255)},${getRandomInt(0,255)},${getRandomInt(0,255)})`
            this.$vs.notify({title:'Icon mail',text:'Lorem ipsum dolor sit amet, consectetur',color:color,icon:'verified_user'})
            }
            }
            }
            &lt;/script&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Fixed and Function click
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Fixed and Function click
          <vs-button class="ml-auto p-0" @click="funnotification=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          Sometimes we need to execute a function when the user clicks on the notification. For this, pass a function to the click property. Example:
          <code>click:()=>{ ... }</code>
        </p>

        <div class="btn-alignment">
          <vs-button @click="myFunction()" type="flat">Run Example</vs-button>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="funnotification">
          <vs-prism>
            &lt;template lang=&quot;html&quot;&gt;
            &lt;div class=&quot;centerx&quot;&gt;
            &lt;vs-button @click=&quot;myFunction()&quot; type=&quot;flat&quot;&gt;Run Example&lt;/vs-button&gt;
            &lt;/div&gt;
            &lt;/template&gt;
            &lt;script&gt;
            export default {
            methods:{
            myFunction(){
            this.$vs.notify({
            title:'Function click',
            text:'Click on me',
            color:'primary',
            fixed:true,
            click:()=&gt;{
            // Secondary function
            this.$vs.notify({
            title:'Secondary function',
            text:'Executed the function when clicking',
            color:'success',
            icon:'check_box'
            })
            },
            })
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
        Time Notification
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Time Notification
          <vs-button class="ml-auto p-0" @click="timenotification=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can change the total time that the notification stays on the screen with the time property. Example:
          <code>time: 4000</code>.
        </p>

        <div class="btn-alignment">
          <vs-button
            @click="$vs.notify({
                  title:'Time default',
                  text:'Lorem ipsum dolor sit amet consectetur',
                  color:'primary',
                  icon:'query_builder'
                })"
            color="primary"
            type="flat"
          >Time default</vs-button>

          <vs-button
            @click="$vs.notify({
                  time:4000,
                  title:'Time 4s (4000)',
                  text:'Lorem ipsum dolor sit amet consectetur',
                  color:'primary',
                  icon:'query_builder'
                })"
            color="primary"
            type="flat"
          >Time 4s (4000)</vs-button>

          <vs-button
            @click="$vs.notify({
                  time:8000,
                  title:'Time 8s (8000)',
                  text:'Lorem ipsum dolor sit amet consectetur',
                  color:'primary',
                  icon:'query_builder'
                })"
            color="primary"
            type="flat"
          >Time 8s (8000)</vs-button>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="timenotification">
          <vs-prism></vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>
    </vs-col>
  </vs-row>
</template>

<script>
export default {
  name: "notification",
  data: () => ({
    title: "Notification",
    defaultnotification: false,
    posnotification: false,
    iconnotification: false,
    funnotification: false,
    timenotification: false
  }),
  methods: {
    random() {
      function getRandomInt(min, max) {
        return Math.floor(Math.random() * (max - min)) + min;
      }
      let color = `rgb(${getRandomInt(0, 255)},${getRandomInt(
        0,
        255
      )},${getRandomInt(0, 255)})`;

      this.$vs.notify({
        title: "Color",
        text: "Lorem ipsum dolor sit amet, consectetur",
        color: color
      });
    },
    randomCenter() {
      function getRandomInt(min, max) {
        return Math.floor(Math.random() * (max - min)) + min;
      }
      let color = `rgb(${getRandomInt(0, 255)},${getRandomInt(
        0,
        255
      )},${getRandomInt(0, 255)})`;
      this.$vs.notify({
        title: "Position top-center",
        text: "Lorem ipsum dolor sit amet, consectetur",
        color: color,
        position: "top-center"
      });
    },
    randomIcon() {
      function getRandomInt(min, max) {
        return Math.floor(Math.random() * (max - min)) + min;
      }
      let color = `rgb(${getRandomInt(0, 255)},${getRandomInt(
        0,
        255
      )},${getRandomInt(0, 255)})`;

      this.$vs.notify({
        title: "Icon mail",
        text: "Lorem ipsum dolor sit amet, consectetur",
        color: color,
        icon: "verified_user"
      });
    },
    myFunction() {
      this.$vs.notify({
        title: "Function click",
        text: "Click on me",
        color: "primary",
        fixed: true,
        click: () => {
          // Secondary function
          this.$vs.notify({
            title: "Secondary function",
            text: "Executed the function when clicking",
            color: "success",
            icon: "check_box"
          });
        }
      });
    }
  }
};
</script>

