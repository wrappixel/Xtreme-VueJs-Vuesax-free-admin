<template>
  <vs-row vs-justify="center">
    <vs-col type="flex" vs-justify="center" vs-align="center" vs-lg="12" vs-xs="12">
      <!--
        /////////////////
        Default List
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Default List
          <vs-button class="ml-auto p-0" @click="defaultlist=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          A basic list of items with
          <code>title</code> and
          <code>subtitle</code>.
        </p>

        <vs-list>
          <vs-list-item title="One text"></vs-list-item>
          <vs-list-item title="Another text" subtitle="A little text"></vs-list-item>
          <vs-list-item title="Some more text"></vs-list-item>
          <vs-list-item title="Even more text" subtitle="Another little text"></vs-list-item>
        </vs-list>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="defaultlist">
          <vs-prism>
            &lt;vs-list&gt;
            &lt;vs-list-item title=&quot;One text&quot;&gt;&lt;/vs-list-item&gt;
            &lt;vs-list-item title=&quot;Another text&quot; subtitle=&quot;A little text&quot;&gt;&lt;/vs-list-item&gt;
            &lt;vs-list-item title=&quot;Some more text&quot;&gt;&lt;/vs-list-item&gt;
            &lt;vs-list-item title=&quot;Even more text&quot; subtitle=&quot;Another little text&quot;&gt;&lt;/vs-list-item&gt;
            &lt;/vs-list&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Header List
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Header List
          <vs-button class="ml-auto p-0" @click="headerlist=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          A
          <code>vs-list-header</code> separator with custom
          <code>color</code>.
        </p>

        <vs-list>
          <vs-list-header title="Group 1"></vs-list-header>
          <vs-list-item title="Snickerdoodle" subtitle="An excellent companion"></vs-list-item>
          <vs-list-item
            title="Sapporo Haru"
            subtitle="An excellent polish restaurant, quick delivery and hearty, filling meals"
          ></vs-list-item>
          <vs-list-header title="Group 2" color="success"></vs-list-header>
          <vs-list-item
            title="Enid's"
            subtitle="At night a bar, during the day a delicious brunch spot."
          ></vs-list-item>
          <vs-list-item title="Veronika Ossi" subtitle="Has not watched anything recently"></vs-list-item>
        </vs-list>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="headerlist">
          <vs-prism>
            &lt;vs-list&gt;
            &lt;vs-list-header title=&quot;Group 1&quot;&gt;&lt;/vs-list-header&gt;
            &lt;vs-list-item title=&quot;Snickerdoodle&quot; subtitle=&quot;An excellent companion&quot;&gt;&lt;/vs-list-item&gt;
            &lt;vs-list-item title=&quot;Sapporo Haru&quot; subtitle=&quot;An excellent polish restaurant, quick delivery and hearty, filling meals&quot;&gt;&lt;/vs-list-item&gt;
            &lt;vs-list-header title=&quot;Group 2&quot; color=&quot;success&quot;&gt;&lt;/vs-list-header&gt;
            &lt;vs-list-item title=&quot;Enid's&quot; subtitle=&quot;At night a bar, during the day a delicious brunch spot.&quot;&gt;&lt;/vs-list-item&gt;
            &lt;vs-list-item title=&quot;Veronika Ossi&quot; subtitle=&quot;Has not watched anything recently&quot;&gt;&lt;/vs-list-item&gt;
            &lt;/vs-list&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Icon List
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Icon List
          <vs-button class="ml-auto p-0" @click="iconlist=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          The list items and the headers can have a
          <code>icon</code> as well.
        </p>

        <vs-list>
          <vs-list-header icon="supervisor_account" title="Group 1"></vs-list-header>
          <vs-list-item icon="check" title="Snickerdoodle" subtitle="An excellent companion"></vs-list-item>
          <vs-list-item
            icon="check"
            title="Sapporo Haru"
            subtitle="An excellent polish restaurant, quick delivery and hearty, filling meals"
          ></vs-list-item>
          <vs-list-header icon="how_to_reg" title="Group 2" color="success"></vs-list-header>
          <vs-list-item
            icon="verified_user"
            title="Enid's"
            subtitle="At night a bar, during the day a delicious brunch spot."
          ></vs-list-item>
          <vs-list-item
            icon="verified_user"
            title="Veronika Ossi"
            subtitle="Has not watched anything recently"
          ></vs-list-item>
        </vs-list>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="iconlist">
          <vs-prism>
            &lt;vs-list&gt;
            &lt;vs-list-header icon=&quot;supervisor_account&quot; title=&quot;Group 1&quot;&gt;&lt;/vs-list-header&gt;
            &lt;vs-list-item icon=&quot;check&quot; title=&quot;Snickerdoodle&quot; subtitle=&quot;An excellent companion&quot;&gt;&lt;/vs-list-item&gt;
            &lt;vs-list-item icon=&quot;check&quot; title=&quot;Sapporo Haru&quot; subtitle=&quot;An excellent polish restaurant, quick delivery and hearty, filling meals&quot;&gt;&lt;/vs-list-item&gt;
            &lt;vs-list-header icon=&quot;how_to_reg&quot; title=&quot;Group 2&quot; color=&quot;success&quot;&gt;&lt;/vs-list-header&gt;
            &lt;vs-list-item icon=&quot;verified_user&quot; title=&quot;Enid's&quot; subtitle=&quot;At night a bar, during the day a delicious brunch spot.&quot;&gt;&lt;/vs-list-item&gt;
            &lt;vs-list-item icon=&quot;verified_user&quot; title=&quot;Veronika Ossi&quot; subtitle=&quot;Has not watched anything recently&quot;&gt;&lt;/vs-list-item&gt;
            &lt;/vs-list&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Content List
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Content List
          <vs-button class="ml-auto p-0" @click="contentlist=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p
          class="card-subtitle"
        >You can add custom content to the item. It will be pushed to the right side.</p>

        <vs-list>
          <vs-list-header title="Group 1"></vs-list-header>
          <vs-list-item title="Snickerdoodle" subtitle="An excellent companion">
            <vs-button color="danger">One action</vs-button>
          </vs-list-item>
          <vs-list-item
            title="Sapporo Haru"
            subtitle="An excellent polish restaurant, quick delivery and hearty, filling meals"
          >
            <vs-checkbox color="danger" />
          </vs-list-item>
          <vs-list-header title="Group 2" color="success"></vs-list-header>
          <vs-list-item
            title="Enid's"
            subtitle="At night a bar, during the day a delicious brunch spot."
          >
            <vs-chip color="warning">Another component</vs-chip>
          </vs-list-item>
          <vs-list-item title="Veronika Ossi" subtitle="Has not watched anything recently">
            <vs-switch color="warning" v-model="val" />
          </vs-list-item>
        </vs-list>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="contentlist">
          <vs-prism>
            &lt;vs-list&gt;
            &lt;vs-list-header title=&quot;Group 1&quot;&gt;&lt;/vs-list-header&gt;
            &lt;vs-list-item title=&quot;Snickerdoodle&quot; subtitle=&quot;An excellent companion&quot;&gt;
            &lt;vs-button color=&quot;danger&quot;&gt;One action&lt;/vs-button&gt;
            &lt;/vs-list-item&gt;
            &lt;vs-list-item title=&quot;Sapporo Haru&quot; subtitle=&quot;An excellent polish restaurant, quick delivery and hearty, filling meals&quot;&gt;
            &lt;vs-checkbox color=&quot;danger&quot;/&gt;
            &lt;/vs-list-item&gt;
            &lt;vs-list-header title=&quot;Group 2&quot; color=&quot;success&quot;&gt;&lt;/vs-list-header&gt;
            &lt;vs-list-item title=&quot;Enid's&quot; subtitle=&quot;At night a bar, during the day a delicious brunch spot.&quot;&gt;
            &lt;vs-chip color=&quot;warning&quot;&gt;Another component&lt;/vs-chip&gt;
            &lt;/vs-list-item&gt;
            &lt;vs-list-item title=&quot;Veronika Ossi&quot; subtitle=&quot;Has not watched anything recently&quot;&gt;
            &lt;vs-switch color=&quot;warning&quot;/&gt;
            &lt;/vs-list-item&gt;
            &lt;/vs-list&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Avatar List
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Avatar List
          <vs-button class="ml-auto p-0" @click="avatarlist=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can implement an avatar in the list with the
          <code>slot="avatar"</code> by putting a [vs-avatar] component (/components/avatar.html)
        </p>

        <vs-list>
          <vs-list-header title="Users" color="danger"></vs-list-header>
          <vs-list-item title="Steve Jobes" subtitle="Top Contributor">
            <template slot="avatar">
              <vs-avatar color="danger" />
            </template>
          </vs-list-item>
          <vs-list-item title="Matt" subtitle="11 Points">
            <template slot="avatar">
              <vs-avatar color="warning" vs-text="Vuesax" />
            </template>
          </vs-list-item>
          <vs-list-header title="Profile photo" color="warning"></vs-list-header>
          <vs-list-item
            title="Xian Famous Foods"
            subtitle="A taste of Shaanxi's delicious culinary traditions, with delights like spicy cold noodles and lamb burgers."
          >
            <template slot="avatar">
              <vs-avatar color="primary" vs-text="Vue" />
            </template>
          </vs-list-item>
        </vs-list>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="avatarlist">
          <vs-prism>
            &lt;vs-list&gt;
            &lt;vs-list-header title=&quot;Users&quot; color=&quot;danger&quot;&gt;&lt;/vs-list-header&gt;
            &lt;vs-list-item title=&quot;Steve Jobes&quot; subtitle=&quot;Top Contributor&quot;&gt;
            &lt;template slot=&quot;avatar&quot;&gt;
            &lt;vs-avatar /&gt;
            &lt;/template&gt;
            &lt;/vs-list-item&gt;
            &lt;vs-list-item title=&quot;Matt&quot; subtitle=&quot;11 Points&quot;&gt;
            &lt;template slot=&quot;avatar&quot;&gt;
            &lt;vs-avatar vs-text=&quot;Vuesax&quot;/&gt;
            &lt;/template&gt;
            &lt;/vs-list-item&gt;
            &lt;vs-list-header title=&quot;Profile photo&quot; color=&quot;warning&quot;&gt;&lt;/vs-list-header&gt;
            &lt;vs-list-item title=&quot;Xian Famous Foods&quot; subtitle=&quot;A taste of Shaanxi's delicious culinary traditions, with delights like spicy cold noodles and lamb burgers.&quot;&gt;
            &lt;template slot=&quot;avatar&quot;&gt;
            &lt;vs-avatar vs-text=&quot;Vue&quot;/&gt;
            &lt;/template&gt;
            &lt;/vs-list-item&gt;
            &lt;/vs-list&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>
    </vs-col>
  </vs-row>
</template>

<script>
export default {
  name: "list",
  data: () => ({
    title: "List",
    defaultlist: false,
    headerlist: false,
    iconlist: false,
    contentlist: false,
    avatarlist: false
  })
};
</script>

