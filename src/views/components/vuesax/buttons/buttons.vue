<template>
  <vs-row vs-justify="center">
    <vs-col type="flex" vs-justify="center" vs-align="center" vs-lg="12" vs-xs="12">
      <!--
        /////////////////
        Filled Buttons
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Filled Buttons
          <vs-button class="ml-auto p-0" @click="filledbuttons=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          To define the type of button the directive is used
          <code>type</code> with the value of some type of button like it can be:
          <code>filled</code>.
        </p>
        <div class="btn-alignment">
          <vs-button color="primary" type="filled">Primary</vs-button>
          <vs-button color="success" type="filled">Success</vs-button>
          <vs-button color="danger" type="filled">Danger</vs-button>
          <vs-button color="warning" type="filled">Warning</vs-button>
          <vs-button color="dark" type="filled">Dark</vs-button>
          <vs-button color="rgb(62, 201, 214)" type="filled">RGB</vs-button>
          <vs-button disabled type="filled">Disabled</vs-button>
          <vs-button color="primary" type="filled" to="/components/list.html">Router</vs-button>
        </div>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="filledbuttons">
          <vs-prism>
            &lt;div class=&quot;btn-alignment&quot;&gt;
            &lt;vs-button color=&quot;primary&quot; type=&quot;filled&quot;&gt;Primary&lt;/vs-button&gt;
            &lt;vs-button color=&quot;success&quot; type=&quot;filled&quot;&gt;Success&lt;/vs-button&gt;
            &lt;vs-button color=&quot;danger&quot; type=&quot;filled&quot;&gt;Danger&lt;/vs-button&gt;
            &lt;vs-button color=&quot;warning&quot; type=&quot;filled&quot;&gt;Warning&lt;/vs-button&gt;
            &lt;vs-button color=&quot;dark&quot; type=&quot;filled&quot;&gt;Dark&lt;/vs-button&gt;
            &lt;vs-button color=&quot;rgb(62, 201, 214)&quot; type=&quot;filled&quot;&gt;RGB&lt;/vs-button&gt;
            &lt;vs-button disabled type=&quot;filled&quot;&gt;Disabled&lt;/vs-button&gt;
            &lt;vs-button color=&quot;primary&quot; type=&quot;filled&quot; to=&quot;/components/list.html&quot;&gt;Router&lt;/vs-button&gt;
            &lt;/div&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
            /////////////////
            Border Buttons
            /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Border Buttons
          <vs-button class="ml-auto p-0" @click="borderbuttons=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          To add a type of button with edges we change the value of
          <code>border</code>.
        </p>
        <div class="btn-alignment">
          <vs-button color="primary" type="border">Primary</vs-button>
          <vs-button color="success" type="border">Success</vs-button>
          <vs-button color="danger" type="border">Danger</vs-button>
          <vs-button color="warning" type="border">Warning</vs-button>
          <vs-button color="dark" type="border">Dark</vs-button>
          <vs-button color="rgb(134, 4, 98)" type="border">RGB</vs-button>
          <vs-button disabled type="border">Disabled</vs-button>
          <vs-button color="primary" type="border" to="/components/list.html">Router</vs-button>
        </div>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="borderbuttons">
          <vs-prism>
            &lt;div class=&quot;btn-alignment&quot;&gt;
            &lt;vs-button color=&quot;primary&quot; type=&quot;border&quot;&gt;Primary&lt;/vs-button&gt;
            &lt;vs-button color=&quot;success&quot; type=&quot;border&quot;&gt;Success&lt;/vs-button&gt;
            &lt;vs-button color=&quot;danger&quot; type=&quot;border&quot;&gt;Danger&lt;/vs-button&gt;
            &lt;vs-button color=&quot;warning&quot; type=&quot;border&quot;&gt;Warning&lt;/vs-button&gt;
            &lt;vs-button color=&quot;dark&quot; type=&quot;border&quot;&gt;Dark&lt;/vs-button&gt;
            &lt;vs-button color=&quot;rgb(134, 4, 98)&quot; type=&quot;border&quot;&gt;RGB&lt;/vs-button&gt;
            &lt;vs-button disabled type=&quot;border&quot;&gt;Disabled&lt;/vs-button&gt;
            &lt;vs-button color=&quot;primary&quot; type=&quot;border&quot; to=&quot;/components/list.html&quot;&gt;Router&lt;/vs-button&gt;
            &lt;/div&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
            /////////////////
            Flat Buttons
            /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Flat Buttons
          <vs-button class="ml-auto p-0" @click="flatbuttons=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          To add a type of button with edges we change the value of
          <code>flat</code>.
        </p>
        <div class="btn-alignment">
          <vs-button color="primary" type="flat">Primary</vs-button>
          <vs-button color="success" type="flat">Success</vs-button>
          <vs-button color="danger" type="flat">Danger</vs-button>
          <vs-button color="warning" type="flat">Warning</vs-button>
          <vs-button color="dark" type="flat">Dark</vs-button>
          <vs-button color="rgb(11, 189, 135)" type="flat">RGB</vs-button>
          <vs-button disabled type="flat">Disabled</vs-button>
        </div>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="flatbuttons">
          <vs-prism>
            &lt;div class=&quot;btn-alignment&quot;&gt;
            &lt;vs-button color=&quot;primary&quot; type=&quot;flat&quot;&gt;Primary&lt;/vs-button&gt;
            &lt;vs-button color=&quot;success&quot; type=&quot;flat&quot;&gt;Success&lt;/vs-button&gt;
            &lt;vs-button color=&quot;danger&quot; type=&quot;flat&quot;&gt;Danger&lt;/vs-button&gt;
            &lt;vs-button color=&quot;warning&quot; type=&quot;flat&quot;&gt;Warning&lt;/vs-button&gt;
            &lt;vs-button color=&quot;dark&quot; type=&quot;flat&quot;&gt;Dark&lt;/vs-button&gt;
            &lt;vs-button color=&quot;rgb(11, 189, 135)&quot; type=&quot;flat&quot;&gt;RGB&lt;/vs-button&gt;
            &lt;vs-button disabled type=&quot;flat&quot;&gt;Disabled&lt;/vs-button&gt;
            &lt;/div&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
            /////////////////
            Line Down Buttons
            /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Line Down Buttons
          <vs-button class="ml-auto p-0" @click="linebuttons=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          To add a type of button with edges we change the value of
          <code>line</code>.
        </p>
        <div class="btn-alignment">
          <vs-button type="line">Primary</vs-button>
          <vs-button line-origin="left" color="success" type="line">Success</vs-button>
          <vs-button color="danger" type="line">Danger</vs-button>
          <vs-button line-position="top" line-origin="left" color="warning" type="line">Warning</vs-button>
          <vs-button line-position="top" line-origin="right" color="dark" type="line">Dark</vs-button>
          <vs-button disabled type="line">Disabled</vs-button>
        </div>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="linebuttons">
          <vs-prism>
            &lt;div class=&quot;btn-alignment&quot;&gt;
            &lt;vs-button type=&quot;line&quot;&gt;Primary&lt;/vs-button&gt;
            &lt;vs-button line-origin=&quot;left&quot; color=&quot;success&quot; type=&quot;line&quot;&gt;Success&lt;/vs-button&gt;
            &lt;vs-button color=&quot;danger&quot; type=&quot;line&quot;&gt;Danger&lt;/vs-button&gt;
            &lt;vs-button line-position=&quot;top&quot; line-origin=&quot;left&quot; color=&quot;warning&quot; type=&quot;line&quot;&gt;Warning&lt;/vs-button&gt;
            &lt;vs-button line-position=&quot;top&quot; line-origin=&quot;right&quot; color=&quot;dark&quot; type=&quot;line&quot;&gt;Dark&lt;/vs-button&gt;
            &lt;vs-button disabled type=&quot;line&quot;&gt;Disabled&lt;/vs-button&gt;
            &lt;/div&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
            /////////////////
            Gredient Buttons
            /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Gredient Buttons
          <vs-button class="ml-auto p-0" @click="gredientbuttons=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          To add a type of button with edges we change the value of
          <code>gradient</code>.
        </p>
        <div class="btn-alignment">
          <vs-button type="gradient">primary</vs-button>
          <vs-button color="success" type="gradient">success</vs-button>
          <vs-button color="danger" type="gradient">danger</vs-button>
          <vs-button color="warning" type="gradient">warning</vs-button>
          <vs-button color="dark" type="gradient">dark</vs-button>
          <vs-button
            color="#3dd495"
            gradient-color-secondary="rgb(130, 207, 23)"
            type="gradient"
          >dark</vs-button>
          <vs-button disabled type="gradient">Disabled</vs-button>
        </div>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="gredientbuttons">
          <vs-prism>
            &lt;vs-button type=&quot;gradient&quot;&gt;primary&lt;/vs-button&gt;
            &lt;vs-button color=&quot;success&quot; type=&quot;gradient&quot;&gt;success&lt;/vs-button&gt;
            &lt;vs-button color=&quot;danger&quot; type=&quot;gradient&quot;&gt;danger&lt;/vs-button&gt;
            &lt;vs-button color=&quot;warning&quot; type=&quot;gradient&quot;&gt;warning&lt;/vs-button&gt;
            &lt;vs-button color=&quot;dark&quot; type=&quot;gradient&quot;&gt;dark&lt;/vs-button&gt;
            &lt;vs-button color=&quot;#3dd495&quot; gradient-color-secondary=&quot;rgb(130, 207, 23)&quot; type=&quot;gradient&quot;&gt;dark&lt;/vs-button&gt;
            &lt;vs-button disabled type=&quot;gradient&quot;&gt;Disabled&lt;/vs-button&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
            /////////////////
            Relief Buttons
            /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Relief Buttons
          <vs-button class="ml-auto p-0" @click="reliefbuttons=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          To add a type of button with edges we change the value of
          <code>relief</code>.
        </p>
        <div class="btn-alignment">
          <vs-button type="relief">Primary</vs-button>
          <vs-button color="success" type="relief">Success</vs-button>
          <vs-button color="danger" type="relief">Danger</vs-button>
          <vs-button color="warning" type="relief">warning</vs-button>
          <vs-button color="dark" type="relief">dark</vs-button>
          <vs-button color="rgb(187, 138, 200)" type="relief">Color</vs-button>
          <vs-button disabled type="relief">Disabled</vs-button>
        </div>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="reliefbuttons">
          <vs-prism>
            &lt;div class=&quot;btn-alignment&quot;&gt;
            &lt;vs-button type=&quot;relief&quot;&gt;Primary&lt;/vs-button&gt;
            &lt;vs-button color=&quot;success&quot; type=&quot;relief&quot;&gt;Success&lt;/vs-button&gt;
            &lt;vs-button color=&quot;danger&quot; type=&quot;relief&quot;&gt;Danger&lt;/vs-button&gt;
            &lt;vs-button color=&quot;warning&quot; type=&quot;relief&quot;&gt;warning&lt;/vs-button&gt;
            &lt;vs-button color=&quot;dark&quot; type=&quot;relief&quot;&gt;dark&lt;/vs-button&gt;
            &lt;vs-button color=&quot;rgb(187, 138, 200)&quot; type=&quot;relief&quot;&gt;Color&lt;/vs-button&gt;
            &lt;vs-button disabled type=&quot;relief&quot;&gt;Disabled&lt;/vs-button&gt;
            &lt;/div&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
            /////////////////
            Color Buttons
            /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Color Buttons
          <vs-button class="ml-auto p-0" @click="colorbuttons=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          There are cases in which we need something more personalized like a specific color, you can change the color of the button with the property
          <code>color</code> giving it as a value the color.
        </p>
        <div class="btn-alignment">
          <input type="color" v-model="colorx" name value />
          <input type="color" v-model="colorx2" name value />
          <vs-button :color="colorx" type="filled">Color</vs-button>
          <vs-button :color="colorx" type="border">Color</vs-button>
          <vs-button :color="colorx" type="flat">Color</vs-button>
          <vs-button :color="colorx" type="line">Color</vs-button>
          <vs-button :color="colorx" :gradient-color-secondary="colorx2" type="gradient">Color</vs-button>
          <vs-button :color="colorx" type="relief">Color</vs-button>
        </div>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="colorbuttons">
          <vs-prism>
            &lt;div class=&quot;btn-alignment&quot;&gt;
            &lt;input type=&quot;color&quot; v-model=&quot;colorx&quot; name=&quot;&quot; value=&quot;&quot;&gt;
            &lt;input type=&quot;color&quot; v-model=&quot;colorx2&quot; name=&quot;&quot; value=&quot;&quot;&gt;
            &lt;vs-button :color=&quot;colorx&quot; type=&quot;filled&quot;&gt;Color&lt;/vs-button&gt;
            &lt;vs-button :color=&quot;colorx&quot; type=&quot;border&quot;&gt;Color&lt;/vs-button&gt;
            &lt;vs-button :color=&quot;colorx&quot; type=&quot;flat&quot;&gt;Color&lt;/vs-button&gt;
            &lt;vs-button :color=&quot;colorx&quot; type=&quot;line&quot;&gt;Color&lt;/vs-button&gt;
            &lt;vs-button :color=&quot;colorx&quot; :gradient-color-secondary=&quot;colorx2&quot; type=&quot;gradient&quot;&gt;Color&lt;/vs-button&gt;
            &lt;vs-button :color=&quot;colorx&quot; type=&quot;relief&quot;&gt;Color&lt;/vs-button&gt;
            &lt;/div&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
            /////////////////
            Text Color Buttons
            /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Text Color Buttons
          <vs-button class="ml-auto p-0" @click="textcolorbuttons=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can change the font color of buttons, need only set the prop
          <code>text-color</code> with your color.
        </p>
        <div class="btn-alignment">
          <vs-button>Primary</vs-button>
          <vs-button color="success" text-color="rgb(255, 255, 255)">Success</vs-button>
          <vs-button color="danger" text-color="#ffffff">Danger</vs-button>
          <vs-button color="warning" text-color="primary">warning</vs-button>
          <vs-button color="dark">dark</vs-button>
          <vs-button color="rgb(187, 138, 200)" text-color="warning)">Color</vs-button>
          <vs-button disabled text-color="rgb(0, 0, 0)">Disabled</vs-button>
        </div>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="textcolorbuttons">
          <vs-prism>
            &lt;div class=&quot;btn-alignment&quot;&gt;
            &lt;vs-button&gt;Primary&lt;/vs-button&gt;
            &lt;vs-button color=&quot;success&quot; text-color=&quot;rgb(255, 255, 255)&quot;&gt;Success&lt;/vs-button&gt;
            &lt;vs-button color=&quot;danger&quot; text-color=&quot;#ffffff&quot;&gt;Danger&lt;/vs-button&gt;
            &lt;vs-button color=&quot;warning&quot; text-color=&quot;primary&quot;&gt;warning&lt;/vs-button&gt;
            &lt;vs-button color=&quot;dark&quot;&gt;dark&lt;/vs-button&gt;
            &lt;vs-button color=&quot;rgb(187, 138, 200)&quot; text-color=&quot;warning)&quot;&gt;Color&lt;/vs-button&gt;
            &lt;vs-button disabled text-color=&quot;rgb(0, 0, 0)&quot;&gt;Disabled&lt;/vs-button&gt;
            &lt;/div&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
            /////////////////
            Icons Buttons
            /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Icon Buttons
          <vs-button class="ml-auto p-0" @click="iconbuttons=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can add an icon to the button with the property
          <code>icon</code>.
        </p>
        <div class="btn-alignment">
          <vs-button color="primary" type="border" icon="home">Home</vs-button>
          <vs-button color="warning" type="filled" icon="star">Star</vs-button>
          <vs-button color="success" type="flat" icon="done">Done</vs-button>
          <vs-button color="dark" type="line" icon="menu">menu</vs-button>
          <vs-button color="danger" type="gradient" icon="favorite">favorite</vs-button>
          <vs-button disabled color="primary" type="border" icon="home">Disabled</vs-button>
        </div>
        <div class="clearfix"></div>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="iconbuttons">
          <vs-prism>
            &lt;div class=&quot;btn-alignment&quot;&gt;
            &lt;vs-button color=&quot;primary&quot; type=&quot;border&quot; icon=&quot;home&quot;&gt;Home&lt;/vs-button&gt;
            &lt;vs-button color=&quot;warning&quot; type=&quot;filled&quot; icon=&quot;star&quot;&gt;Star&lt;/vs-button&gt;
            &lt;vs-button color=&quot;success&quot; type=&quot;flat&quot; icon=&quot;done&quot;&gt;Done&lt;/vs-button&gt;
            &lt;vs-button color=&quot;dark&quot; type=&quot;line&quot; icon=&quot;menu&quot;&gt;menu&lt;/vs-button&gt;
            &lt;vs-button color=&quot;danger&quot; type=&quot;gradient&quot; icon=&quot;favorite&quot;&gt;favorite&lt;/vs-button&gt;
            &lt;vs-button disabled color=&quot;primary&quot; type=&quot;border&quot; icon=&quot;home&quot;&gt;Disabled&lt;/vs-button&gt;
            &lt;/div&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
            /////////////////
            Icon only Buttons
            /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Icon only
          <vs-button class="ml-auto p-0" @click="icononlybuttons=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can have a button with only the icon you want with the property
          <code>icon</code> and not add any internal value to the button
        </p>
        <div class="btn-alignment">
          <vs-button color="primary" type="border" icon="search"></vs-button>
          <vs-button color="warning" type="filled" icon="public"></vs-button>
          <vs-button color="success" type="flat" icon="photo_camera"></vs-button>
          <vs-button color="dark" type="line" icon="event_note"></vs-button>
          <vs-button color="danger" type="gradient" icon="person_add"></vs-button>
          <vs-button disabled color="primary" type="border" icon="search"></vs-button>
        </div>
        <div class="clearfix"></div>
        <div class="btn-alignment mt-3">
          <vs-button radius color="primary" type="border" icon="search"></vs-button>
          <vs-button radius color="warning" type="filled" icon="public"></vs-button>
          <vs-button radius color="success" type="flat" icon="photo_camera"></vs-button>
          <vs-button radius color="dark" type="line" icon="event_note"></vs-button>
          <vs-button radius color="danger" type="gradient" icon="person_add"></vs-button>
          <vs-button disabled radius color="primary" type="border" icon="search"></vs-button>
        </div>
        <div class="clearfix"></div>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="icononlybuttons">
          <vs-prism>
            &lt;div class=&quot;btn-alignment&quot;&gt;
            &lt;vs-button color=&quot;primary&quot; type=&quot;border&quot; icon=&quot;search&quot;&gt;&lt;/vs-button&gt;
            &lt;vs-button color=&quot;warning&quot; type=&quot;filled&quot; icon=&quot;public&quot;&gt;&lt;/vs-button&gt;
            &lt;vs-button color=&quot;success&quot; type=&quot;flat&quot; icon=&quot;photo_camera&quot;&gt;&lt;/vs-button&gt;
            &lt;vs-button color=&quot;dark&quot; type=&quot;line&quot; icon=&quot;event_note&quot;&gt;&lt;/vs-button&gt;
            &lt;vs-button color=&quot;danger&quot; type=&quot;gradient&quot; icon=&quot;person_add&quot;&gt;&lt;/vs-button&gt;
            &lt;vs-button disabled color=&quot;primary&quot; type=&quot;border&quot; icon=&quot;search&quot;&gt;&lt;/vs-button&gt;
            &lt;/div&gt;
            &lt;div class=&quot;clearfix&quot;&gt;&lt;/div&gt;
            &lt;div class=&quot;btn-alignment&quot;&gt;
            &lt;vs-button radius color=&quot;primary&quot; type=&quot;border&quot; icon=&quot;search&quot;&gt;&lt;/vs-button&gt;
            &lt;vs-button radius color=&quot;warning&quot; type=&quot;filled&quot; icon=&quot;public&quot;&gt;&lt;/vs-button&gt;
            &lt;vs-button radius color=&quot;success&quot; type=&quot;flat&quot; icon=&quot;photo_camera&quot;&gt;&lt;/vs-button&gt;
            &lt;vs-button radius color=&quot;dark&quot; type=&quot;line&quot; icon=&quot;event_note&quot;&gt;&lt;/vs-button&gt;
            &lt;vs-button radius color=&quot;danger&quot; type=&quot;gradient&quot; icon=&quot;person_add&quot;&gt;&lt;/vs-button&gt;
            &lt;vs-button disabled radius color=&quot;primary&quot; type=&quot;border&quot; icon=&quot;search&quot;&gt;&lt;/vs-button&gt;
            &lt;/div&gt;
            &lt;div class=&quot;clearfix&quot;&gt;&lt;/div&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
            /////////////////
            Size Buttons
            /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Size Buttons
          <vs-button class="ml-auto p-0" @click="sizebuttons=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          To define the size of button the directive is used
          <code>size</code>. there are three type of size:
          <code>large, default, small</code>. It is not important to specify the size when the button is of type
          <code>default</code>
        </p>
        <div class="btn-alignment">
          <vs-button size="large">Large</vs-button>
          <vs-button>Default</vs-button>
          <vs-button size="small">Small</vs-button>
        </div>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="sizebuttons">
          <vs-prism>
            &lt;div class=&quot;btn-alignment&quot;&gt;
            &lt;vs-button size=&quot;large&quot;&gt;Large&lt;/vs-button&gt;
            &lt;vs-button&gt;Default&lt;/vs-button&gt;
            &lt;vs-button size=&quot;small&quot;&gt;Small&lt;/vs-button&gt;
            &lt;/div&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
            /////////////////
            Router Buttons
            /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Router Buttons
          <vs-button class="ml-auto p-0" @click="routerbuttons=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can send a string or object to directive
          <code>to</code>. This directive wrap a
          <code>$router.push()</code> vue method, you can use all programmatic navigation on vue router.
        </p>
        <div class="btn-alignment">
          <vs-button color="primary" type="filled" to="/buttons">String literal</vs-button>
          <vs-button color="warning" type="filled" :to="{ path: '/buttons' }">Object Path</vs-button>
          <vs-button
            color="success"
            type="filled"
            :to="{ name: 'user', params: { userId: 123 } }"
          >Named Router</vs-button>
          <vs-button
            color="dark"
            type="filled"
            :to="{ path: 'register', query: { plan: 'private' } }"
          >With Query</vs-button>
        </div>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="routerbuttons">
          <vs-prism>
            &lt;div class=&quot;btn-alignment&quot;&gt;
            &lt;vs-button color=&quot;primary&quot; type=&quot;filled&quot; to=&quot;/buttons&quot;&gt;String literal&lt;/vs-button&gt;
            &lt;vs-button color=&quot;warning&quot; type=&quot;filled&quot; :to=&quot;{ path: '/buttons' }&quot;&gt;Object Path&lt;/vs-button&gt;
            &lt;vs-button color=&quot;success&quot; type=&quot;filled&quot; :to=&quot;{ name: 'user', params: { userId: 123 } }&quot;&gt;Named Router&lt;/vs-button&gt;
            &lt;vs-button color=&quot;dark&quot; type=&quot;filled&quot; :to=&quot;{ path: 'register', query: { plan: 'private' } }&quot;&gt;With Query&lt;/vs-button&gt;
            &lt;/div&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
            /////////////////
            Link Buttons
            /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Link Buttons
          <vs-button class="ml-auto p-0" @click="linkbuttons=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can specify for
          <code>window.location.href</code>.
        </p>
        <div class="btn-alignment">
          <vs-button
            color="primary"
            type="filled"
            href="https://lusaxweb.github.io/vuesax/"
          >String literal</vs-button>
          <vs-button
            color="primary"
            type="filled"
            :href="{url: 'https://lusaxweb.github.io/vuesax/'}"
          >Object Path</vs-button>
          <vs-button
            color="primary"
            type="filled"
            target
            :href="{url: 'https://lusaxweb.github.io/vuesax/'}"
          >Open Current Tab</vs-button>
        </div>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="linkbuttons">
          <vs-prism>
            &lt;div class=&quot;btn-alignment&quot;&gt;
            &lt;vs-button color=&quot;primary&quot; type=&quot;filled&quot; href=&quot;https://lusaxweb.github.io/vuesax/&quot;&gt;String literal&lt;/vs-button&gt;
            &lt;vs-button color=&quot;primary&quot; type=&quot;filled&quot; :href=&quot;{url: 'https://lusaxweb.github.io/vuesax/'}&quot;&gt;Object Path&lt;/vs-button&gt;
            &lt;vs-button color=&quot;primary&quot; type=&quot;filled&quot; target :href=&quot;{url: 'https://lusaxweb.github.io/vuesax/'}&quot;&gt;Open Current Tab&lt;/vs-button&gt;
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
  name: "buttons",
  data: () => ({
    title: "Buttons",
    filledbuttons: false,
    borderbuttons: false,
    flatbuttons: false,
    linebuttons: false,
    gredientbuttons: false,
    reliefbuttons: false,
    colorbuttons: false,
    colorx: "#c72a75",
    colorx2: "#5252e8",
    textcolorbuttons: false,
    iconbuttons: false,
    icononlybuttons: false,
    sizebuttons: false,
    routerbuttons: false,
    linkbuttons: false
  })
};
</script>


