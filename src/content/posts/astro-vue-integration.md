---
title: "Astro 与 Vue 3 的完美结合"
pubDate: "2024-01-20"
description: "探索如何在 Astro 中使用 Vue 3 构建高性能的动态组件。"
---

# Astro 与 Vue 3 的完美结合

Astro 是一个专注于内容驱动的静态站点生成器，而 Vue 3 是最流行的渐进式 JavaScript 框架之一。将它们结合在一起，可以获得两全其美的体验。

## 为什么选择 Astro + Vue？

### 1. 性能优先

Astro 使用"岛屿架构"（Islands Architecture），默认只发送最小的 JavaScript。只有当需要交互时，才加载对应的组件。

```javascript
// 这是一个静态组件，不需要 JS
<StaticComponent />

// 这是一个交互组件，会加载 JS
<InteractiveComponent client:visible />
```

### 2. Vue 3 的响应式优势

Vue 3 的 Composition API 让代码组织更加清晰：

```javascript
import { ref, computed, onMounted } from 'vue'

export default {
  setup() {
    const count = ref(0)
    const doubled = computed(() => count.value * 2)
    
    onMounted(() => {
      console.log('Component mounted!')
    })
    
    return { count, doubled }
  }
}
```

### 3. UnoCSS 的原子化样式

配合 UnoCSS，开发体验既高效又灵活：

```html
<button class="px-4 py-2 bg-primary-500 text-white rounded-lg hover:bg-primary-600 transition-colors">
  按钮
</button>
```

## 总结

Astro + Vue 3 + UnoCSS 是一个非常强大的组合，既能保证性能，又能提供出色的开发体验。
