<template>
  <div>
    <!-- <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld />
    <AttributeDemoVue />
    <IfAndForDemoVue />
    <ModelDemo />
    <TodoItem v-for="item in groceryList" :todo="item" :key="item.id"></TodoItem> -->
    <!-- <MarkdownDemo /> -->

    <!-- <GetDataDemo/> -->

    <!-- <form id="search">
      Search <input name="query" v-model="searchQuery">
    </form>
    <DataGridDemo :data="gridDatas" :columns="gridColumns" :filter-key="searchQuery">

    </DataGridDemo> -->

    <!-- TreeItem -->
    <!-- <ul>
      <TreeItem class=" item" :model="treeData"></TreeItem>
    </ul> -->


    <!-- <SVGImageVue/> -->
    <!-- <ModalDemoVue/> -->


    <!-- <TransitionGroupDemoVue /> -->
    <!-- <TodeMVCDemoVue></TodeMVCDemoVue> -->
    <!-- <FlightBookDemoVue/> -->

    <TimerDemoVue/>


  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import AttributeDemoVue from "./components/AttributeDemo.vue";
import IfAndForDemoVue from "./components/IfAndForDemo.vue";
import ModelDemoVue from "./components/ModelDemo.vue";
import ModelDemo from "./components/ModelDemo.vue";
import TodoItemVue from "./components/TodoItem.vue";
import TodoItem from "./components/TodoItem.vue";
import MarkdownDemo from "./components/MarkdownDemo.vue";
import GetDataDemoVue from "./components/GetDataDemo.vue";
import GetDataDemo from "./components/GetDataDemo.vue";
import DataGridDemoVue from "./components/DataGridDemo.vue";
import DataGridDemo from "./components/DataGridDemo.vue";
import TreeItemVue from "./components/TreeItem.vue";
import TreeItem from "./components/TreeItem.vue";
import SVGImageVue from "./components/SVGImage/SVGImage.vue";
import ModalDemoVue from "./components/ModalDemo/ModalDemo.vue";
import TransitionGroupDemoVue from "./components/TransitionGroupDemo.vue";
import TodeMVCDemoVue from "./components/TodeMVCDemo.vue";
import FlightBookDemoVue from "./components/FlightBookDemo.vue";
import TimerDemoVue from "./components/TimerDemo.vue";

const treeData = {
  name: 'My Tree',
  children: [
    { name: 'hello' },
    { name: 'wat' },
    {
      name: 'child folder',
      children: [
        {
          name: 'child folder',
          children: [{ name: 'hello' }, { name: 'wat' }]
        },
        { name: 'hello' },
        { name: 'wat' },
        {
          name: 'child folder',
          children: [{ name: 'hello' }, { name: 'wat' }]
        }
      ]
    }
  ]
}
export default {
  name: "App",
  components: {
    HelloWorld,
    AttributeDemoVue,
    IfAndForDemoVue,
    ModelDemoVue,
    ModelDemo,
    TodoItemVue,
    TodoItem,
    MarkdownDemo,
    GetDataDemoVue,
    GetDataDemo,
    DataGridDemoVue,
    DataGridDemo,
    TreeItemVue,
    TreeItem,
    SVGImageVue,
    ModalDemoVue,
    TransitionGroupDemoVue,
    TodeMVCDemoVue,
    FlightBookDemoVue,
    TimerDemoVue
  },
  data() {
    return {
      groceryList: [
        { id: 0, text: 'Vegetables' },
        { id: 1, text: 'Cheese' },
        { id: 2, text: 'Whatever else humans are supposed to' }
      ],
      searchQuery: '',
      gridColumns: ['name', 'power'],
      gridDatas: [
        { name: 'Chuck Norris', power: Infinity },
        { name: 'Bruce Lee', power: 9000 },
        { name: 'Jackie Chan', power: 7000 },
        { name: 'Jet Li', power: 8000 }
      ],
      treeData
    }
  }

};
</script>

<style>
.item {
  cursor: pointer;
  line-height: 1.5;
}

.bold1 {
  font-weight: bold;
}
</style>
