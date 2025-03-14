# v-backtop

返回顶部指令，当页面滚动到一定高度时显示返回顶部按钮。

## 基础用法

请继续向下滚动页面，当滚动超过 400px 时会在右下角显示返回顶部按钮。点击按钮可以平滑滚动回顶部。

- `visibilityHeight`：滚动高度达到此参数值才出现
- `duration`：回到顶部所需时间(ms)

<BacktopDemo />

::: details 点击查看代码
<<< @/.vitepress/components/vBacktop/BacktopDemo.vue
:::

## API

<ApiTable :data="props" />

## 注意事项

::: warning 注意

- 使用该指令的元素会自动添加点击事件，点击后页面会平滑滚动到顶部
- 当滚动高度小于 visibilityHeight 时，元素会被隐藏
- 指令会自动处理事件的绑定和解绑，无需手动管理

:::

<script setup>
import BacktopDemo from '../.vitepress/components/vBacktop/BacktopDemo.vue'
import ApiTable from '../.vitepress/components/ApiTable.vue'

const props = [
  {
    name: 'visibilityHeight',
    description: '滚动高度达到此参数值才出现，单位 px',
    type: 'number',
    default: '400',
    required: false,
  },
  {
    name: 'duration',
    description: '回到顶部所需时间，单位 ms',
    type: 'number',
    default: '500',
    required: false,
  },
]
</script>
