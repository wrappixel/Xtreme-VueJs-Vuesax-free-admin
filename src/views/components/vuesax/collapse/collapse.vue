<template>
  <vs-row vs-justify="center">
    <vs-col type="flex" vs-justify="center" vs-align="center" vs-lg="12" vs-xs="12">
      <!--
        /////////////////
        Default Collapse
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Default Collapse
          <vs-button class="ml-auto p-0" @click="defaultcollapse=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          To implement the collapse we have the component
          <code>vs-collapse</code> and as sub-component for each item the component
          <code>vs-collapse-item</code>
        </p>
        <div>
          <vs-collapse>
            <vs-collapse-item>
              <div slot="header">Collapse item</div>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque rhoncus eros tortor, non fringilla lectus cursus et. Fusce vel nisi ante. Aliquam sit amet lectus pharetra, luctus mi sed, aliquet felis. Mauris a tortor viverra, ornare tellus in, consectetur leo.
              <br />
              <br />Etiam nec nunc nec nisl luctus tincidunt efficitur vitae elit. Vestibulum iaculis nibh commodo neque ultrices lobortis. Cras magna massa, pretium vitae mattis varius, pharetra nec massa. Aliquam ac ex enim. Quisque consequat dui libero, vel blandit lorem porttitor sit amet. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Nullam sed lobortis nisl, quis eleifend metus.
            </vs-collapse-item>
            <vs-collapse-item>
              <div slot="header">Collapse item 2</div>Nunc auctor et leo vitae suscipit. Nullam aliquet purus scelerisque enim hendrerit tristique. Maecenas tincidunt dui arcu, a aliquet nisl venenatis vitae. Praesent mauris ligula, porta at maximus ac, rutrum vitae sapien. Donec a sapien id erat dapibus dignissim sodales in est. Donec gravida dapibus sapien at sollicitudin. Maecenas iaculis quam ex,
              <br />
              <br />eu aliquam erat sagittis eget. Suspendisse mollis felis nec ipsum vehicula, at posuere libero viverra. Nam hendrerit dapibus eleifend. Aliquam elit nulla, tincidunt pellentesque enim mollis, consectetur placerat enim. Integer condimentum tristique ante et ullamcorper. Mauris placerat pretium ex. Nam aliquam sed tortor sit amet
              <br />
              <br />efficitur. Mauris quis faucibus nulla. Pellentesque egestas non ipsum vel maximus.
            </vs-collapse-item>
            <vs-collapse-item disabled>
              <div slot="header">Collapse item 3 - Disabled</div>Suspendisse aliquet condimentum diam, sed aliquam nisl dapibus et. Aliquam euismod ullamcorper dolor eu
            </vs-collapse-item>
            <vs-collapse-item>
              <div slot="header">Collapse item 4</div>Suspendisse aliquet condimentum diam, sed aliquam nisl dapibus et. Aliquam euismod ullamcorper dolor eu imperdiet. Nullam eget odio at magna gravida suscipit sed vestibulum odio. Maecenas porta elit vel lectus molestie, eget aliquam enim feugiat. Vivamus nec faucibus nisl. Nunc venenatis tempus finibus.
            </vs-collapse-item>
          </vs-collapse>
        </div>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="defaultcollapse">
          <vs-prism>
            &lt;div&gt;
            &lt;vs-collapse&gt;
            &lt;vs-collapse-item&gt;
            &lt;div slot=&quot;header&quot;&gt;
            Collapse item
            &lt;/div&gt;
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque rhoncus eros tortor, non fringilla lectus cursus et. Fusce vel nisi ante. Aliquam sit amet lectus pharetra, luctus mi sed, aliquet felis. Mauris a tortor viverra, ornare tellus in, consectetur leo.
            &lt;br&gt;&lt;br&gt;
            Etiam nec nunc nec nisl luctus tincidunt efficitur vitae elit. Vestibulum iaculis nibh commodo neque ultrices lobortis. Cras magna massa, pretium vitae mattis varius, pharetra nec massa. Aliquam ac ex enim. Quisque consequat dui libero, vel blandit lorem porttitor sit amet. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Nullam sed lobortis nisl, quis eleifend metus.
            &lt;/vs-collapse-item&gt;
            &lt;vs-collapse-item&gt;
            &lt;div slot=&quot;header&quot;&gt;
            Collapse item 2
            &lt;/div&gt;
            Nunc auctor et leo vitae suscipit. Nullam aliquet purus scelerisque enim hendrerit tristique. Maecenas tincidunt dui arcu, a aliquet nisl venenatis vitae. Praesent mauris ligula, porta at maximus ac, rutrum vitae sapien. Donec a sapien id erat dapibus dignissim sodales in est. Donec gravida dapibus sapien at sollicitudin. Maecenas iaculis quam ex,
            &lt;br&gt;&lt;br&gt;
            eu aliquam erat sagittis eget. Suspendisse mollis felis nec ipsum vehicula, at posuere libero viverra. Nam hendrerit dapibus eleifend. Aliquam elit nulla, tincidunt pellentesque enim mollis, consectetur placerat enim. Integer condimentum tristique ante et ullamcorper. Mauris placerat pretium ex. Nam aliquam sed tortor sit amet
            &lt;br&gt;&lt;br&gt;
            efficitur. Mauris quis faucibus nulla. Pellentesque egestas non ipsum vel maximus.
            &lt;/vs-collapse-item&gt;
            &lt;vs-collapse-item disabled &gt;
            &lt;div slot=&quot;header&quot;&gt;
            Collapse item 3 - Disabled
            &lt;/div&gt;
            Suspendisse aliquet condimentum diam, sed aliquam nisl dapibus et. Aliquam euismod ullamcorper dolor eu
            &lt;/vs-collapse-item&gt;
            &lt;vs-collapse-item&gt;
            &lt;div slot=&quot;header&quot;&gt;
            Collapse item 4
            &lt;/div&gt;
            Suspendisse aliquet condimentum diam, sed aliquam nisl dapibus et. Aliquam euismod ullamcorper dolor eu imperdiet. Nullam eget odio at magna gravida suscipit sed vestibulum odio. Maecenas porta elit vel lectus molestie, eget aliquam enim feugiat. Vivamus nec faucibus nisl. Nunc venenatis tempus finibus.
            &lt;/vs-collapse-item&gt;
            &lt;/vs-collapse&gt;
            &lt;/div&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Default Accordion
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          Default Accordion
          <vs-button class="ml-auto p-0" @click="defaultaccordian=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You may need to show only one element and the others contract for this is the property
          <code>accordion</code>
        </p>
        <div>
          <vs-collapse accordion>
            <vs-collapse-item>
              <div slot="header">Collapse item</div>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque rhoncus eros tortor, non fringilla lectus cursus et. Fusce vel nisi ante. Aliquam sit amet lectus pharetra, luctus mi sed, aliquet felis. Mauris a tortor viverra, ornare tellus in, consectetur leo.
              <br />
              <br />Etiam nec nunc nec nisl luctus tincidunt efficitur vitae elit. Vestibulum iaculis nibh commodo neque ultrices lobortis. Cras magna massa, pretium vitae mattis varius, pharetra nec massa. Aliquam ac ex enim. Quisque consequat dui libero, vel blandit lorem porttitor sit amet. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Nullam sed lobortis nisl, quis eleifend metus.
            </vs-collapse-item>
            <vs-collapse-item>
              <div slot="header">Collapse item 2</div>Nunc auctor et leo vitae suscipit. Nullam aliquet purus scelerisque enim hendrerit tristique. Maecenas tincidunt dui arcu, a aliquet nisl venenatis vitae. Praesent mauris ligula, porta at maximus ac, rutrum vitae sapien. Donec a sapien id erat dapibus dignissim sodales in est. Donec gravida dapibus sapien at sollicitudin. Maecenas iaculis quam ex,
              <br />
              <br />eu aliquam erat sagittis eget. Suspendisse mollis felis nec ipsum vehicula, at posuere libero viverra. Nam hendrerit dapibus eleifend. Aliquam elit nulla, tincidunt pellentesque enim mollis, consectetur placerat enim. Integer condimentum tristique ante et ullamcorper. Mauris placerat pretium ex. Nam aliquam sed tortor sit amet
              <br />
              <br />efficitur. Mauris quis faucibus nulla. Pellentesque egestas non ipsum vel maximus.
            </vs-collapse-item>
            <vs-collapse-item>
              <div slot="header">Collapse item 3</div>Suspendisse aliquet condimentum diam, sed aliquam nisl dapibus et. Aliquam euismod ullamcorper dolor eu
            </vs-collapse-item>
            <vs-collapse-item>
              <div slot="header">Collapse item 4</div>Suspendisse aliquet condimentum diam, sed aliquam nisl dapibus et. Aliquam euismod ullamcorper dolor eu imperdiet. Nullam eget odio at magna gravida suscipit sed vestibulum odio. Maecenas porta elit vel lectus molestie, eget aliquam enim feugiat. Vivamus nec faucibus nisl. Nunc venenatis tempus finibus.
            </vs-collapse-item>
          </vs-collapse>
        </div>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="defaultaccordian">
          <vs-prism>
            &lt;div&gt;
            &lt;vs-collapse accordion &gt;
            &lt;vs-collapse-item&gt;
            &lt;div slot=&quot;header&quot;&gt;
            Collapse item
            &lt;/div&gt;
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque rhoncus eros tortor, non fringilla lectus cursus et. Fusce vel nisi ante. Aliquam sit amet lectus pharetra, luctus mi sed, aliquet felis. Mauris a tortor viverra, ornare tellus in, consectetur leo.
            &lt;br&gt;&lt;br&gt;
            Etiam nec nunc nec nisl luctus tincidunt efficitur vitae elit. Vestibulum iaculis nibh commodo neque ultrices lobortis. Cras magna massa, pretium vitae mattis varius, pharetra nec massa. Aliquam ac ex enim. Quisque consequat dui libero, vel blandit lorem porttitor sit amet. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Nullam sed lobortis nisl, quis eleifend metus.
            &lt;/vs-collapse-item&gt;
            &lt;vs-collapse-item&gt;
            &lt;div slot=&quot;header&quot;&gt;
            Collapse item 2
            &lt;/div&gt;
            Nunc auctor et leo vitae suscipit. Nullam aliquet purus scelerisque enim hendrerit tristique. Maecenas tincidunt dui arcu, a aliquet nisl venenatis vitae. Praesent mauris ligula, porta at maximus ac, rutrum vitae sapien. Donec a sapien id erat dapibus dignissim sodales in est. Donec gravida dapibus sapien at sollicitudin. Maecenas iaculis quam ex,
            &lt;br&gt;&lt;br&gt;
            eu aliquam erat sagittis eget. Suspendisse mollis felis nec ipsum vehicula, at posuere libero viverra. Nam hendrerit dapibus eleifend. Aliquam elit nulla, tincidunt pellentesque enim mollis, consectetur placerat enim. Integer condimentum tristique ante et ullamcorper. Mauris placerat pretium ex. Nam aliquam sed tortor sit amet
            &lt;br&gt;&lt;br&gt;
            efficitur. Mauris quis faucibus nulla. Pellentesque egestas non ipsum vel maximus.
            &lt;/vs-collapse-item&gt;
            &lt;vs-collapse-item &gt;
            &lt;div slot=&quot;header&quot;&gt;
            Collapse item 3
            &lt;/div&gt;
            Suspendisse aliquet condimentum diam, sed aliquam nisl dapibus et. Aliquam euismod ullamcorper dolor eu
            &lt;/vs-collapse-item&gt;
            &lt;vs-collapse-item&gt;
            &lt;div slot=&quot;header&quot;&gt;
            Collapse item 4
            &lt;/div&gt;
            Suspendisse aliquet condimentum diam, sed aliquam nisl dapibus et. Aliquam euismod ullamcorper dolor eu imperdiet. Nullam eget odio at magna gravida suscipit sed vestibulum odio. Maecenas porta elit vel lectus molestie, eget aliquam enim feugiat. Vivamus nec faucibus nisl. Nunc venenatis tempus finibus.
            &lt;/vs-collapse-item&gt;
            &lt;/vs-collapse&gt;
            &lt;/div&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Types
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Types
          <vs-button class="ml-auto p-0" @click="typecollapse=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can easily change the style of the accordion with the
          <code>type</code> property, the supported styles are:
        </p>
        <ul class="list-group list-group-horizontal mb-3">
          <li class="list-group-item rounded-0 py-2">
            <span>shadow</span>
          </li>
          <li class="list-group-item rounded-0 py-2">
            <span>border</span>
          </li>
          <li class="list-group-item rounded-0 py-2">
            <span>margin</span>
          </li>
        </ul>

        <div>
          <ul class="list-group list-group-horizontal-lg mb-3">
            <li class="list-group-item rounded-0 py-2">
              <vs-radio v-model="type" vs-value="default">Default</vs-radio>
            </li>
            <li class="list-group-item rounded-0 py-2">
              <vs-radio v-model="type" vs-value="shadow">Shadow</vs-radio>
            </li>
            <li class="list-group-item rounded-0 py-2">
              <vs-radio v-model="type" vs-value="border">Border</vs-radio>
            </li>
            <li class="list-group-item rounded-0 py-2">
              <vs-radio v-model="type" vs-value="margin">Margin</vs-radio>
            </li>
          </ul>
          <vs-collapse :type="type">
            <vs-collapse-item>
              <div slot="header">Collapse item</div>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque rhoncus eros tortor, non fringilla lectus cursus et. Fusce vel nisi ante. Aliquam sit amet lectus pharetra, luctus mi sed, aliquet felis. Mauris a tortor viverra, ornare tellus in, consectetur leo.
              <br />
              <br />Etiam nec nunc nec nisl luctus tincidunt efficitur vitae elit. Vestibulum iaculis nibh commodo neque ultrices lobortis. Cras magna massa, pretium vitae mattis varius, pharetra nec massa. Aliquam ac ex enim. Quisque consequat dui libero, vel blandit lorem porttitor sit amet. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Nullam sed lobortis nisl, quis eleifend metus.
            </vs-collapse-item>
            <vs-collapse-item>
              <div slot="header">Collapse item 2</div>Nunc auctor et leo vitae suscipit. Nullam aliquet purus scelerisque enim hendrerit tristique. Maecenas tincidunt dui arcu, a aliquet nisl venenatis vitae. Praesent mauris ligula, porta at maximus ac, rutrum vitae sapien. Donec a sapien id erat dapibus dignissim sodales in est. Donec gravida dapibus sapien at sollicitudin. Maecenas iaculis quam ex,
              <br />
              <br />eu aliquam erat sagittis eget. Suspendisse mollis felis nec ipsum vehicula, at posuere libero viverra. Nam hendrerit dapibus eleifend. Aliquam elit nulla, tincidunt pellentesque enim mollis, consectetur placerat enim. Integer condimentum tristique ante et ullamcorper. Mauris placerat pretium ex. Nam aliquam sed tortor sit amet
              <br />
              <br />efficitur. Mauris quis faucibus nulla. Pellentesque egestas non ipsum vel maximus.
            </vs-collapse-item>
            <vs-collapse-item disabled>
              <div slot="header">Collapse item 3 - Disabled</div>Suspendisse aliquet condimentum diam, sed aliquam nisl dapibus et. Aliquam euismod ullamcorper dolor eu
            </vs-collapse-item>
            <vs-collapse-item>
              <div slot="header">Collapse item 4</div>Suspendisse aliquet condimentum diam, sed aliquam nisl dapibus et. Aliquam euismod ullamcorper dolor eu imperdiet. Nullam eget odio at magna gravida suscipit sed vestibulum odio. Maecenas porta elit vel lectus molestie, eget aliquam enim feugiat. Vivamus nec faucibus nisl. Nunc venenatis tempus finibus.
            </vs-collapse-item>
          </vs-collapse>
        </div>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="typecollapse">
          <vs-prism>
            &lt;div&gt;
            &lt;ul class=&quot;list-group list-group-horizontal mb-3&quot;&gt;
            &lt;li class=&quot;list-group-item rounded-0 py-2&quot;&gt;
            &lt;vs-radio v-model=&quot;type&quot; vs-value=&quot;default&quot;&gt;Default&lt;/vs-radio&gt;
            &lt;/li&gt;
            &lt;li class=&quot;list-group-item rounded-0 py-2&quot;&gt;
            &lt;vs-radio v-model=&quot;type&quot; vs-value=&quot;shadow&quot;&gt;Shadow&lt;/vs-radio&gt;
            &lt;/li&gt;
            &lt;li class=&quot;list-group-item rounded-0 py-2&quot;&gt;
            &lt;vs-radio v-model=&quot;type&quot; vs-value=&quot;border&quot;&gt;Border&lt;/vs-radio&gt;
            &lt;/li&gt;
            &lt;li class=&quot;list-group-item rounded-0 py-2&quot;&gt;
            &lt;vs-radio v-model=&quot;type&quot; vs-value=&quot;margin&quot;&gt;Margin&lt;/vs-radio&gt;
            &lt;/li&gt;
            &lt;/ul&gt;
            &lt;vs-collapse :type=&quot;type&quot;&gt;
            &lt;vs-collapse-item&gt;
            &lt;div slot=&quot;header&quot;&gt;
            Collapse item
            &lt;/div&gt;
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque rhoncus eros tortor, non fringilla lectus cursus et. Fusce vel nisi ante. Aliquam sit amet lectus pharetra, luctus mi sed, aliquet felis. Mauris a tortor viverra, ornare tellus in, consectetur leo.
            &lt;br&gt;&lt;br&gt;
            Etiam nec nunc nec nisl luctus tincidunt efficitur vitae elit. Vestibulum iaculis nibh commodo neque ultrices lobortis. Cras magna massa, pretium vitae mattis varius, pharetra nec massa. Aliquam ac ex enim. Quisque consequat dui libero, vel blandit lorem porttitor sit amet. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Nullam sed lobortis nisl, quis eleifend metus.
            &lt;/vs-collapse-item&gt;
            &lt;vs-collapse-item&gt;
            &lt;div slot=&quot;header&quot;&gt;
            Collapse item 2
            &lt;/div&gt;
            Nunc auctor et leo vitae suscipit. Nullam aliquet purus scelerisque enim hendrerit tristique. Maecenas tincidunt dui arcu, a aliquet nisl venenatis vitae. Praesent mauris ligula, porta at maximus ac, rutrum vitae sapien. Donec a sapien id erat dapibus dignissim sodales in est. Donec gravida dapibus sapien at sollicitudin. Maecenas iaculis quam ex,
            &lt;br&gt;&lt;br&gt;
            eu aliquam erat sagittis eget. Suspendisse mollis felis nec ipsum vehicula, at posuere libero viverra. Nam hendrerit dapibus eleifend. Aliquam elit nulla, tincidunt pellentesque enim mollis, consectetur placerat enim. Integer condimentum tristique ante et ullamcorper. Mauris placerat pretium ex. Nam aliquam sed tortor sit amet
            &lt;br&gt;&lt;br&gt;
            efficitur. Mauris quis faucibus nulla. Pellentesque egestas non ipsum vel maximus.
            &lt;/vs-collapse-item&gt;
            &lt;vs-collapse-item disabled &gt;
            &lt;div slot=&quot;header&quot;&gt;
            Collapse item 3 - Disabled
            &lt;/div&gt;
            Suspendisse aliquet condimentum diam, sed aliquam nisl dapibus et. Aliquam euismod ullamcorper dolor eu
            &lt;/vs-collapse-item&gt;
            &lt;vs-collapse-item&gt;
            &lt;div slot=&quot;header&quot;&gt;
            Collapse item 4
            &lt;/div&gt;
            Suspendisse aliquet condimentum diam, sed aliquam nisl dapibus et. Aliquam euismod ullamcorper dolor eu imperdiet. Nullam eget odio at magna gravida suscipit sed vestibulum odio. Maecenas porta elit vel lectus molestie, eget aliquam enim feugiat. Vivamus nec faucibus nisl. Nunc venenatis tempus finibus.
            &lt;/vs-collapse-item&gt;
            &lt;/vs-collapse&gt;
            &lt;/div&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Open on hover
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Open on Hover
          <vs-button class="ml-auto p-0" @click="hovercollapse=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          If you want the items to open when you hover in, add the
          <code>open-hover</code> property in the component
        </p>
        <div>
          <vs-collapse open-hover>
            <vs-collapse-item>
              <div slot="header">Collapse item</div>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque rhoncus eros tortor, non fringilla lectus cursus et. Fusce vel nisi ante. Aliquam sit amet lectus pharetra, luctus mi sed, aliquet felis. Mauris a tortor viverra, ornare tellus in, consectetur leo.
              <br />
              <br />Etiam nec nunc nec nisl luctus tincidunt efficitur vitae elit. Vestibulum iaculis nibh commodo neque ultrices lobortis. Cras magna massa, pretium vitae mattis varius, pharetra nec massa. Aliquam ac ex enim. Quisque consequat dui libero, vel blandit lorem porttitor sit amet. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Nullam sed lobortis nisl, quis eleifend metus.
            </vs-collapse-item>
            <vs-collapse-item>
              <div slot="header">Collapse item 2</div>Nunc auctor et leo vitae suscipit. Nullam aliquet purus scelerisque enim hendrerit tristique. Maecenas tincidunt dui arcu, a aliquet nisl venenatis vitae. Praesent mauris ligula, porta at maximus ac, rutrum vitae sapien. Donec a sapien id erat dapibus dignissim sodales in est. Donec gravida dapibus sapien at sollicitudin. Maecenas iaculis quam ex,
              <br />
              <br />eu aliquam erat sagittis eget. Suspendisse mollis felis nec ipsum vehicula, at posuere libero viverra. Nam hendrerit dapibus eleifend. Aliquam elit nulla, tincidunt pellentesque enim mollis, consectetur placerat enim. Integer condimentum tristique ante et ullamcorper. Mauris placerat pretium ex. Nam aliquam sed tortor sit amet
              <br />
              <br />efficitur. Mauris quis faucibus nulla. Pellentesque egestas non ipsum vel maximus.
            </vs-collapse-item>
            <vs-collapse-item>
              <div slot="header">Collapse item 3</div>Suspendisse aliquet condimentum diam, sed aliquam nisl dapibus et. Aliquam euismod ullamcorper dolor eu
            </vs-collapse-item>
            <vs-collapse-item>
              <div slot="header">Collapse item 4</div>Suspendisse aliquet condimentum diam, sed aliquam nisl dapibus et. Aliquam euismod ullamcorper dolor eu imperdiet. Nullam eget odio at magna gravida suscipit sed vestibulum odio. Maecenas porta elit vel lectus molestie, eget aliquam enim feugiat. Vivamus nec faucibus nisl. Nunc venenatis tempus finibus.
            </vs-collapse-item>
          </vs-collapse>
        </div>

        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="hovercollapse">
          <vs-prism>
            &lt;div&gt;
            &lt;vs-collapse open-hover &gt;
            &lt;vs-collapse-item&gt;
            &lt;div slot=&quot;header&quot;&gt;
            Collapse item
            &lt;/div&gt;
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque rhoncus eros tortor, non fringilla lectus cursus et. Fusce vel nisi ante. Aliquam sit amet lectus pharetra, luctus mi sed, aliquet felis. Mauris a tortor viverra, ornare tellus in, consectetur leo.
            &lt;br&gt;&lt;br&gt;
            Etiam nec nunc nec nisl luctus tincidunt efficitur vitae elit. Vestibulum iaculis nibh commodo neque ultrices lobortis. Cras magna massa, pretium vitae mattis varius, pharetra nec massa. Aliquam ac ex enim. Quisque consequat dui libero, vel blandit lorem porttitor sit amet. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Nullam sed lobortis nisl, quis eleifend metus.
            &lt;/vs-collapse-item&gt;
            &lt;vs-collapse-item&gt;
            &lt;div slot=&quot;header&quot;&gt;
            Collapse item 2
            &lt;/div&gt;
            Nunc auctor et leo vitae suscipit. Nullam aliquet purus scelerisque enim hendrerit tristique. Maecenas tincidunt dui arcu, a aliquet nisl venenatis vitae. Praesent mauris ligula, porta at maximus ac, rutrum vitae sapien. Donec a sapien id erat dapibus dignissim sodales in est. Donec gravida dapibus sapien at sollicitudin. Maecenas iaculis quam ex,
            &lt;br&gt;&lt;br&gt;
            eu aliquam erat sagittis eget. Suspendisse mollis felis nec ipsum vehicula, at posuere libero viverra. Nam hendrerit dapibus eleifend. Aliquam elit nulla, tincidunt pellentesque enim mollis, consectetur placerat enim. Integer condimentum tristique ante et ullamcorper. Mauris placerat pretium ex. Nam aliquam sed tortor sit amet
            &lt;br&gt;&lt;br&gt;
            efficitur. Mauris quis faucibus nulla. Pellentesque egestas non ipsum vel maximus.
            &lt;/vs-collapse-item&gt;
            &lt;vs-collapse-item &gt;
            &lt;div slot=&quot;header&quot;&gt;
            Collapse item 3
            &lt;/div&gt;
            Suspendisse aliquet condimentum diam, sed aliquam nisl dapibus et. Aliquam euismod ullamcorper dolor eu
            &lt;/vs-collapse-item&gt;
            &lt;vs-collapse-item&gt;
            &lt;div slot=&quot;header&quot;&gt;
            Collapse item 4
            &lt;/div&gt;
            Suspendisse aliquet condimentum diam, sed aliquam nisl dapibus et. Aliquam euismod ullamcorper dolor eu imperdiet. Nullam eget odio at magna gravida suscipit sed vestibulum odio. Maecenas porta elit vel lectus molestie, eget aliquam enim feugiat. Vivamus nec faucibus nisl. Nunc venenatis tempus finibus.
            &lt;/vs-collapse-item&gt;
            &lt;/vs-collapse&gt;
            &lt;/div&gt;
          </vs-prism>
        </vs-popup>
        <!-- Code -->
      </vs-card>

      <!--
        /////////////////
        Change Arrow Icon
        /////////////////
      -->
      <vs-card>
        <h3 class="card-title d-flex">
          With Change Arrow Icon
          <vs-button class="ml-auto p-0" @click="arrowcollapse=true" type="line">
            <vs-icon icon="code"></vs-icon>
          </vs-button>
        </h3>
        <p class="card-subtitle">
          You can customise the arrow on the component
          <code>vs-collapse</code> by passing the string name of an icon to the
          <code>icon-arrow</code> property.
        </p>

        <div>
          <vs-collapse>
            <vs-collapse-item icon-arrow="label">
              <div slot="header">Collapse item</div>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque rhoncus eros tortor, non fringilla lectus cursus et. Fusce vel nisi ante. Aliquam sit amet lectus pharetra, luctus mi sed, aliquet felis. Mauris a tortor viverra, ornare tellus in, consectetur leo.
              <br />
              <br />Etiam nec nunc nec nisl luctus tincidunt efficitur vitae elit. Vestibulum iaculis nibh commodo neque ultrices lobortis. Cras magna massa, pretium vitae mattis varius, pharetra nec massa. Aliquam ac ex enim. Quisque consequat dui libero, vel blandit lorem porttitor sit amet. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Nullam sed lobortis nisl, quis eleifend metus.
            </vs-collapse-item>
            <vs-collapse-item icon-arrow="grade">
              <div slot="header">Collapse item 2</div>Nunc auctor et leo vitae suscipit. Nullam aliquet purus scelerisque enim hendrerit tristique. Maecenas tincidunt dui arcu, a aliquet nisl venenatis vitae. Praesent mauris ligula, porta at maximus ac, rutrum vitae sapien. Donec a sapien id erat dapibus dignissim sodales in est. Donec gravida dapibus sapien at sollicitudin. Maecenas iaculis quam ex,
              <br />
              <br />eu aliquam erat sagittis eget. Suspendisse mollis felis nec ipsum vehicula, at posuere libero viverra. Nam hendrerit dapibus eleifend. Aliquam elit nulla, tincidunt pellentesque enim mollis, consectetur placerat enim. Integer condimentum tristique ante et ullamcorper. Mauris placerat pretium ex. Nam aliquam sed tortor sit amet
              <br />
              <br />efficitur. Mauris quis faucibus nulla. Pellentesque egestas non ipsum vel maximus.
            </vs-collapse-item>
            <vs-collapse-item disabled icon-arrow="arrow_downward">
              <div slot="header">Collapse item 3 - Disabled</div>Suspendisse aliquet condimentum diam, sed aliquam nisl dapibus et. Aliquam euismod ullamcorper dolor eu
            </vs-collapse-item>
            <vs-collapse-item icon-arrow="arrow_drop_down">
              <div slot="header">Collapse item 4</div>Suspendisse aliquet condimentum diam, sed aliquam nisl dapibus et. Aliquam euismod ullamcorper dolor eu imperdiet. Nullam eget odio at magna gravida suscipit sed vestibulum odio. Maecenas porta elit vel lectus molestie, eget aliquam enim feugiat. Vivamus nec faucibus nisl. Nunc venenatis tempus finibus.
            </vs-collapse-item>
          </vs-collapse>
        </div>
        <!-- Code -->
        <vs-popup class="holamundo" title="Code" :active.sync="arrowcollapse">
          <vs-prism>
            &lt;div&gt;
            &lt;vs-collapse&gt;
            &lt;vs-collapse-item icon-arrow=&quot;label&quot;&gt;
            &lt;div slot=&quot;header&quot;&gt;
            Collapse item
            &lt;/div&gt;
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque rhoncus eros tortor, non fringilla lectus cursus et. Fusce vel nisi ante. Aliquam sit amet lectus pharetra, luctus mi sed, aliquet felis. Mauris a tortor viverra, ornare tellus in, consectetur leo.
            &lt;br&gt;&lt;br&gt;
            Etiam nec nunc nec nisl luctus tincidunt efficitur vitae elit. Vestibulum iaculis nibh commodo neque ultrices lobortis. Cras magna massa, pretium vitae mattis varius, pharetra nec massa. Aliquam ac ex enim. Quisque consequat dui libero, vel blandit lorem porttitor sit amet. Vestibulum ante ipsum primis in faucibus orci luctus et ultrices posuere cubilia Curae; Nullam sed lobortis nisl, quis eleifend metus.
            &lt;/vs-collapse-item&gt;
            &lt;vs-collapse-item icon-arrow=&quot;grade&quot;&gt;
            &lt;div slot=&quot;header&quot;&gt;
            Collapse item 2
            &lt;/div&gt;
            Nunc auctor et leo vitae suscipit. Nullam aliquet purus scelerisque enim hendrerit tristique. Maecenas tincidunt dui arcu, a aliquet nisl venenatis vitae. Praesent mauris ligula, porta at maximus ac, rutrum vitae sapien. Donec a sapien id erat dapibus dignissim sodales in est. Donec gravida dapibus sapien at sollicitudin. Maecenas iaculis quam ex,
            &lt;br&gt;&lt;br&gt;
            eu aliquam erat sagittis eget. Suspendisse mollis felis nec ipsum vehicula, at posuere libero viverra. Nam hendrerit dapibus eleifend. Aliquam elit nulla, tincidunt pellentesque enim mollis, consectetur placerat enim. Integer condimentum tristique ante et ullamcorper. Mauris placerat pretium ex. Nam aliquam sed tortor sit amet
            &lt;br&gt;&lt;br&gt;
            efficitur. Mauris quis faucibus nulla. Pellentesque egestas non ipsum vel maximus.
            &lt;/vs-collapse-item&gt;
            &lt;vs-collapse-item disabled icon-arrow=&quot;arrow_downward&quot;&gt;
            &lt;div slot=&quot;header&quot;&gt;
            Collapse item 3 - Disabled
            &lt;/div&gt;
            Suspendisse aliquet condimentum diam, sed aliquam nisl dapibus et. Aliquam euismod ullamcorper dolor eu
            &lt;/vs-collapse-item&gt;
            &lt;vs-collapse-item icon-arrow=&quot;arrow_drop_down&quot;&gt;
            &lt;div slot=&quot;header&quot;&gt;
            Collapse item 4
            &lt;/div&gt;
            Suspendisse aliquet condimentum diam, sed aliquam nisl dapibus et. Aliquam euismod ullamcorper dolor eu imperdiet. Nullam eget odio at magna gravida suscipit sed vestibulum odio. Maecenas porta elit vel lectus molestie, eget aliquam enim feugiat. Vivamus nec faucibus nisl. Nunc venenatis tempus finibus.
            &lt;/vs-collapse-item&gt;
            &lt;/vs-collapse&gt;
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
  name: "collapse",
  data: () => ({
    title: "Collapse",
    defaultcollapse: false,
    defaultaccordian: false,
    type: "shadow",
    typecollapse: false,
    hovercollapse: false,
    arrowcollapse: false
  })
};
</script>

<style lang="css">
.con-vs-radio {
  margin: 5px;
}
</style>


