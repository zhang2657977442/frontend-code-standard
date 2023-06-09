# Vue3组合式API

```vue
<script setup lang="ts">
// 引入第三方类库
import { ref, reactive, watch, watchEffect, onMounted, onBeforeUnmount } from 'vue'
import { useRoute, useRouter } from 'vue-router'

// 引入项目文件
import sleep from '../utils/sleep.ts'
    
// 引入TS类型
import type ObjType from 'xxxxxx'
  
// 定义TS类型
interface Props {
  data: ChatGroupType.ChatGroup;
  node: Node;
  editBoxId: string;
}
    
// 定义Props
const props = defineProps<Props>();

// 定义emit
const emit = defineEmits(['xxxxxx','xxxxxx'])

// 初始化实例
const route = useRoute()

// 定义基本类型常量
const a: number = 0

// 定义复杂类型常量
const obj: ObjType = {
  pageNum: 1,
  pageSize: 10,
}

// 定义基本类型响应式数据
const a: number = ref(0)
const b: string = ref('')

// 定义复杂类型响应式数据
const obj: ObjType = reactive({
  pageNum: 1,
  pageSize: 10,
})

// 定义计算属性
const count = computed(() => '返回值')

// 定义函数一
const fun1 = () =>{
    
}

// 定义函数二
const fun2 = () =>{
    
}

// 定义watch
watch(
  () => a,
  () => {
    console.log('数据变化了')
  },
  { deep: true,
    immediate: true,
  }
)

// 定义watchEffect
watchEffect(() => {})

// setup生命周期 函数执行
fun1()
fun2()
    
// 生命周期按顺序（包括路由钩子）
onMounted(()=>{})
    
......    

onBeforeUnmount(()=>{})
    
// 向外暴露函数
 defineExpose({fun1, fun2})
</script>

<template>
......
</template>

<style>
 ......
</style>
```

