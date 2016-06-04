<template>
  <div id="app">
    <input type='checkbox' id='sideToggle'>
    <aside>
    <left-menu><left-menu>
    </aside>
    <div id='wrap'>
      <label id='sideMenuControl' for='sideToggle'>=</label>
      <main-nav><main-nav>
      <p>纯css实现侧边栏伸缩 </p>
    </div>
  </div>
</template>

<script>
import LeftMenu from './components/LeftMenu'
import MainNav from './components/MainNav'

export default {
  components: {
    LeftMenu,
    MainNav
  }
}
</script>

<style>
#sideToggle {
    display: none;
}

#sideToggle:checked + aside {
    left: 0;
}

#sideToggle:checked ~ #wrap {
    padding-left: 200px;
}
aside {
    position: absolute;
    top: 0;
    bottom: 0;
    left: -200px;
    width: 200px;
    transition: 0.2s ease-out;
    -webkit-transition: 0.2s ease-out;
}
#wrap {
    transition: 0.25s ease-out;
    -webkit-transition: 0.25s ease-out;
}

#wrap > label {
    display: inline-block;
}

#wrap > label {
    background: #2196f3;
    border-radius: 50px;
    color: #FFF;
    cursor: pointer;
    display: block;
    font-family: Courier New;
    font-size: 25px;
    font-weight: bold;
    width: 30px;
    height: 30px;
    line-height: 35px;
    text-align: center;
    text-shadow: 0 -4px;
}

#wrap > label:hover {
    background: #000;
}
</style>
