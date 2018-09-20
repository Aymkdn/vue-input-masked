<template>
  <div id="app">
    <section class="page-header" id="header">
      <h1 class="project-name">vue-input-masked</h1>
      <h2 class="project-tagline">Simple masked input component for Vue.js 2.</h2>
      <a href="https://github.com/Aymkdn/vue-input-masked" class="btn project-url">View on GitHub</a>
    </section>
    <section class="main-content">
      <p>Same as <a href="https://github.com/niksmr/vue-masked-input">https://github.com/niksmr/vue-masked-input</a> but with the placeholder that stays visible while you're typing (see <a href="https://github.com/niksmr/vue-masked-input/issues/49">issue #49</a>).</p>
      <hr>
      <h3>Browser Compatibility:</h3>
      <p>IE11, and all modern browsers.</p>

      <h3>Patterns:</h3>
      <ul>
        <li>1 – number</li>
        <li>a – letter</li>
        <li>A – letter, forced to upper case when entered</li>
        <li>* – alphanumeric</li>
        <li># – alphanumeric, forced to upper case when entered</li>
        <li>+ – any character</li>
      </ul>

      <p>Use an <b>array</b> for <code>placeholder-char</code> to keep the placeholder up while typing.</p>
      <p>Use a <b>string</b> for <code>placeholder-char</code> to get the normal behavior.</p>

      <h3>Examples:</h3>
      <h4>Date: </h4>
      <p>
        <input-masked
         type="text"
         mask="1111-11-11"
         placeholder="YYYY-MM-DD"
         :placeholder-char="'YYYY-MM-DD'.split('')"
         v-model="date"></input-masked> <span class="value">{{ date }}</span>
       <h5>Code:</h5>
       <pre>
        <code>
&lt;input-masked
 type="text"
 mask="1111-11-11"
 placeholder="YYYY-MM-DD"
 :placeholder-char="'YYYY-MM-DD'.split('')"
 v-model="date"&gt;&lt;/input-masked&gt;
        </code>
       </pre>
      </p>

      <h4>Time: </h4>
      <p>
        <input-masked
         type="text"
         mask="11:11"
         placeholder="hh:ss"
         :placeholder-char="['h','h',':','s','s']"
         v-model="time"></input-masked> <span class="value">{{ time }}</span>
        <h5>Code:</h5>
        <pre>
         <code>
&lt;input-masked
 type="text"
 mask="11:11"
 placeholder="hh:ss"
 :placeholder-char="['h','h',':','s','s']"
 v-model="time"&gt;&lt;/input-masked&gt;
         </code>
        </pre>
      </p>

      <h4>Phone: </h4>
      <p>
        <input-masked
         type="text"
         mask="\+11 (111) 1111-11"
         placeholder="+11 (111) 1111-11"
         placeholder-char="_"
         v-model="phone"></input-masked> <span class="value">{{ phone }}</span>
        <h5>Code:</h5>
        <pre>
         <code>
&lt;input-masked
 type="text"
 mask="\+11 (111) 1111-11"
 placeholder="+11 (111) 1111-11"
 placeholder-char="_"
 v-model="phone"&gt;&lt;/input-masked&gt;
         </code>
        </pre>
      </p>
    </section>
  </div>
</template>

<script>
import InputMasked from './vue-input-masked.js'

export default {
  name: 'app',
  components: {
    InputMasked
  },
  data () {
    return {
      date:'',
      time:'',
      phone:''
    }
  }
}
</script>

<style src="./jekyll.css"></style>
