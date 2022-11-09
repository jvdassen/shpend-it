<script setup>
import TheWelcome from './components/TheWelcome.vue'
</script>

<template>
  <header>
  </header>

  <main>
    <TheWelcome />
  </main>
</template>

<style>
html {
  background: #f080804f;
}
.icon {
  height: 16em;
  width: 16em;
  background-size: contain;
  background-position: center;
  background-repeat: no-repeat;
  border-radius: 50%;
}
.iconwrap {
  height: 16em;
  display: flex;
  justify-content: center;
}

.name, .moneys {
  text-align: center;
}
.stuffs {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}
.stuff {
  flex: 0 0 28%;
/*
  border:  solid 1px #3d3d3d;
*/
  margin-bottom: 4em;
}
h4, h3 {
  text-align: center;
}
button {
  align-items: center;
  background-color: #fee6e3;
  border: 2px solid #111;
  border-radius: 8px;
  box-sizing: border-box;
  color: #111;
  cursor: pointer;
  display: flex;
  font-family: Inter,sans-serif;
  font-size: 16px;
  height: 48px;
  justify-content: center;
  line-height: 24px;
  max-width: 100%;
  padding: 0 25px;
  position: relative;
  text-align: center;
  text-decoration: none;
  user-select: none;
  -webkit-user-select: none;
  touch-action: manipulation;
}

button:after {
  background-color: #111;
  border-radius: 8px;
  content: "";
  display: block;
  height: 48px;
  left: 0;
  width: 100%;
  position: absolute;
  top: -2px;
  transform: translate(8px, 8px);
  transition: transform .2s ease-out;
  z-index: -1;
}

button:hover:after {
  transform: translate(0, 0);
}

button:active {
  background-color: #ffdeda;
  outline: 0;
}

button:hover {
  outline: 0;
}

.controls {
  display: flex;
  box-sizing: border-box;
  justify-content: space-around;
}

.controls > button {
  box-sizing: border-box;
}
.iconproductwrap {
 height: 8em;
}
.iconproduct {
  max-height: 120px;
  height: 120px;
  width: 100%;
  background-size: contain;
  background-position: center;
  background-repeat: no-repeat;
}
.moneys {
  background: #5C7457;
  color: white;
  border-radius: 5px;
  font-size: 36px;
  padding: 0.5em;
}
.rich {
  background: #F0544F0F;
  border-radius: 6px;
  padding: 1em 0;
}
.name {
  color: #843B62;
}
.quant {
  width: 5em;
  align-items: center;
  background-color: #fee6e3;
  border: 2px solid #111;
  border-radius: 8px;
  text-align: center;
}
</style>
