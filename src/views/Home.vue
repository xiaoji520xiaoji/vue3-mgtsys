<template>
  <div class="home">
    <p>{{ num }}</p>
    <p>{{ info.id }}</p>
    <p>{{ info.name }}</p>
    <p>{{ info.age }}</p>
    <button @click="addFun">加1</button>
    <button @click="addAgeFun">年龄</button>
  </div>
</template>

<script>

import { 
  // onBeforeMount, onMounted, onBeforeUpdate, onUpdated, onBeforeUnmount, onUnmounted, onErrorCaptured, 
onRenderTracked, onRenderTriggered, ref, reactive } from 'vue'

export default {
  name: 'Home',
  setup() {
    let num = ref(1)
    let info = reactive({
      id: 1,
      name: 'Lester',
      age: 26,
    })
    // onBeforeMount(()=> {
    //   console.log('onBeforeMount');
    // })
    // onMounted(()=> {
    //   console.log('onMounted');
    // }) 
    // onBeforeUpdate(()=> {
    //   console.log('onBeforeUpdate');
    // })
    // onUpdated(()=> {
    //   console.log('onUpdated');
    // })
    // onBeforeUnmount(()=> {
    //   console.log('onBeforeUnmount');
    // })
    // onUnmounted(()=> {
    //   console.log('onUnmounted');
    // })
    // onErrorCaptured(err=> {
    //   console.log(err);
    // })
    onRenderTracked(obj=> {
      console.log(obj);
    })
    onRenderTriggered(obj=> {
      console.log(obj);
    })

    let addFun = ()=> {
      num.value++
      console.log(num);
    }

    let addAgeFun = ()=> {
      info.age++
    }

    console.log('setUp执行');

    return{
      num,
      addFun,
      info,
      addAgeFun,
    }
  }
}
</script>
