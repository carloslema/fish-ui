<template>
  <main-layout menuActiveIndex="card">
    <h3>Card</h3>
    <fish-row gutter="1">
      <fish-col span="12">
        <code-card title="Basic" desc="A basic card containing a header, content and footer">
          <template slot="demo">
            <fish-card>
              <div slot="header">Title</div>
              Kristy is an art director living in New York.<br/>
              Veronika Ossi Is a living in New York WuMeiShi, her favorite cat, music and the party. <br/>
              Meng dogs have a variety of shapes and sizes. Some puppies look adorable stay because make love,
              pity others because of short of stature. There are even some people who can be stupid because of their huge body shapes.
              <br/>
              Many people also have their own barometers for what makes a cute dog.
              <div slot="footer">
                <fish-button>GO-Back</fish-button>
              </div>
            </fish-card>
          </template>
          <template slot="codeHtml">
            <pre v-highlightjs><code class="xml">&lt;fish-card&gt;
  &lt;div slot=&quot;header&quot;&gt;Title&lt;/div&gt;
  Kristy is an art director living in New York.&lt;br/&gt;
  Veronika OssiIs a living in New York WuMeiShi, her favorite cat, music and the party. <br/>
Meng dogs have a variety of shapes and sizes. Some puppies look adorable stay because make love, pity others because of short of stature.
              There are even some people who can be stupid because of their huge body shapes.
  &lt;br/&gt;
  Many people also have their own barometers for what makes a cute dog.
  &lt;div slot=&quot;footer&quot;&gt;
    &lt;fish-button&gt;GO-Back&lt;/fish-button&gt;
  &lt;/div&gt;
&lt;/fish-card&gt;</code></pre>
          </template>
        </code-card>
      </fish-col>
      <fish-col span="12">
        <code-card title="Content" desc="containing content">
          <template slot="demo">
            <fish-card>
              <h4>Elliot Fu</h4>
              <p>好友</p>
              Kristy is an art director living in New York.<br/>
              Veronika OssiIs a living in New York WuMeiShi, her favorite cat, music and the party. <br/>
              Meng dogs have a variety of shapes and sizes. Some puppies look adorable stay because make love,
              pity others because of short of stature. There are even some people who can be stupid because of their huge body shapes.
              <br/>
              Many people also have their own barometers for what makes a cute dog.
            </fish-card>
          </template>
          <template slot="codeHtml">
            <pre v-highlightjs><code class="xml">&lt;fish-card&gt;
  &lt;h4&gt;Elliot Fu&lt;/h4&gt;
  &lt;p&gt;好友&lt;/p&gt;
  Kristy is an art director living in New York.&lt;br/&gt;
  Veronika OssiIs a living in New York WuMeiShi, her favorite cat, music and the party. <br/>
Meng dogs have a variety of shapes and sizes. Some puppies look adorable stay because make love, pity others because of short of stature.
              There are even some people who can be stupid because of their huge body shapes.
  &lt;br/&gt;
  Many people also have their own barometers for what makes a cute dog.
&lt;/fish-card&gt;</code></pre>
          </template>
        </code-card>
      </fish-col>
    </fish-row>
    <fish-row gutter="1">
      <fish-col span="6">
        <code-card title="Header-Image" desc="containing a header and image">
          <template slot="demo">
            <fish-card>
              <strong slot="header">Elliot requested permission</strong>
              <img src="https://os.alipayobjects.com/rmsportal/QBnOOoLaAfKPirc.png" slot="image" width="100%"/>
            </fish-card>
          </template>
          <template slot="codeHtml">
            <pre v-highlightjs><code class="xml">&lt;fish-card&gt;
  &lt;strong slot=&quot;header&quot;&gt;Elliot requested permission&lt;/strong&gt;
  &lt;img src=&quot;https://os.alipayobjects.com/rmsportal/QBnOOoLaAfKPirc.png&quot; slot=&quot;image&quot; width=&quot;100%&quot;/&gt;
&lt;/fish-card&gt;</code></pre>
          </template>
        </code-card>
      </fish-col>
      <fish-col span="6">
        <code-card title="Header-Content" desc="containing a header and content">
          <template slot="demo">
            <fish-card>
              <img src="https://os.alipayobjects.com/rmsportal/QBnOOoLaAfKPirc.png" slot="image" width="100%"/>
              Elliot requested permission to view your contact details
            </fish-card>
          </template>
          <template slot="codeHtml">
            <pre v-highlightjs><code class="xml">&lt;fish-card&gt;
  &lt;img src=&quot;https://os.alipayobjects.com/rmsportal/QBnOOoLaAfKPirc.png&quot; slot=&quot;image&quot; width=&quot;100%&quot;/&gt;
  Elliot requested permission to view your contact details
&lt;/fish-card&gt;</code></pre>
          </template>
        </code-card>
      </fish-col>

    </fish-row>
    <h3>Card Slots</h3>
    <div class="fish table attributes">
      <table style="table-layout: auto;">
        <thead>
        <tr>
          <th v-for="column in columns">{{column}}</th>
        </tr>
        </thead>
        <tbody>
        <tr v-for="item in data">
          <td v-for="v in item" v-html="v"></td>
        </tr>
        </tbody>
      </table>
    </div>
  </main-layout>
</template>
<script>
  import MainLayout from './MainLayout.vue'
  import CodeCard from './CodeCard.vue'

  export default {
    components: {
      CodeCard,
      MainLayout
    },
    data () {
      return {
        columns: ['Attribute', 'Description', 'Type', 'Default'],
        data: [
          ['header', 'Card title(header)', 'String', '-'],
          ['image', 'Card image', 'String', '-'],
          ['footer', 'Card footer', 'String', '-']
        ]
      }
    }
  }
</script>
