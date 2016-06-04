<template>
  <div id="MainNav">
      <ui-toolbar type="colored" text-color="white" flat loading>
          <div slot="actions">
              <ui-icon-button
                  type="clear" color="white" icon="arrow_back"
              ></ui-icon-button>

              <ui-icon-button
                  type="clear" color="white" icon="star_border"
              ></ui-icon-button>

              <ui-icon-button
                  type="clear" color="white" icon="more_vert" has-dropdown-menu
                  :menu-options="menu" dropdown-position="bottom right"
              ></ui-icon-button>
          </div>
          导航菜单
      </ui-toolbar>
  </div>
</template>

<script>
//import UiTab from '../../src/UiTab.vue';
//import UiTabs from '../../src/UiTabs.vue';
import UiToolbar from 'keen-ui/lib/UiToolbar';
import UiIconButton from 'keen-ui/lib/UiIconButton';

export default {
    data() {
        return {
            menu: [{
                id: 'settings',
                text: '设置'
            }, {
                id: 'about',
                text: '关于'
            }, {
                id: 'help',
                text: '帮助'
            }]
        };
    },

    components: {
        //UiTab,
        //UiTabs,
        UiToolbar,
        UiIconButton
    }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
