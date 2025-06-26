<script setup lang="ts">
import MyComponent from "./components/MyComponent.vue";
import MyComponentWithModel from "./components/MyComponentWithModel.vue";

type MyComponentPropType = InstanceType<typeof MyComponent>["$props"];
const _myComponentProps: MyComponentPropType = { status: "running" }; // Type error

type MyComponentWithModelPropType = InstanceType<
  typeof MyComponentWithModel
>["$props"];
const _myComponentWithModelProps: MyComponentWithModelPropType = {
  status: "running", // No type error
};
</script>
<template>
  <div>
    <MyComponent status="running" />
    <MyComponentWithModel status="running" />
  </div>
</template>
