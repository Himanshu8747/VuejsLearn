<template>
  <HelloWorld msg="Passing props from App to Hello world component"/>
  <h1>Hello World</h1>
  <p>Binding ID</p>
  <h1 :id="Id">Heading Second</h1>
  <p>Binding text</p>
  <h1 v-text="greet"></h1>
  <p>option 2</p>
  <h1>Moustache Syntax :{{greet}}</h1>
  <p>Binding Html</p>
  <strong>Only render the content that you trust using v-html</strong>
  <h1 v-html="Name"></h1>
  <p>Binding Attributes</p>
  <button v-bind:disabled="isDisabled">Submit</button>
  <button v-bind:disabled="!isDisabled">Submit</button>
  <p>Bonding classes</p>
  <div v-bind:class="status">Status</div>
  <button v-bind:class="isPrompted && 'prompted'">Prompted</button>
  <button v-bind:class="isSoldOut && 'soldOut'">SoldOut</button>
  <p>Binding Styles</p>
  <h1 v-bind:style=[headerStyles,morestyles]>Style Binding</h1>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';

export default {
    name: "App",
    data() {
        return {
            greet: "Hello People",
            Id: "heading_second",
            Name: "<b> Himanshus Vue js CodeBase </b>",
            isDisabled: true,
            status: "Success",
            isSoldOut: true,
            isPrompted: false,
            headerStyles: {
                "font-size": 60 + "px",
                "color": "red",
                "border": 2 + "px solid black"
            },
            morestyles: {
                "background-color": "black",
                "font-weight": 400,
            }
        };
    },
    components: { HelloWorld }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
