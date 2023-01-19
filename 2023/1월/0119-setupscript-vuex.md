# 0119
- vue setup script
- Vuex
- Vuex with Composition API

## 1. vue setup script
```jsx
<script setup>
import { defineProps, defineEmits } from "vue";

const props = defineProps({});
const emit = defineEmits([]);
</script>
```

## 2. Vuex
- 상태 관리 패턴 + 라이브러리

![image](https://user-images.githubusercontent.com/58069290/213448135-f0abca40-063a-46a2-8e05-5336abe761b3.png)

## 3. vuex with Composition APi
### Composition API에서 Vuex 사용

```
import { useStore } from 'vuex'

export default {
  setup () {
    const store = useStore()

    return {
			//state
			count: computed(() => store.state.count),

      //mutation
      increment: () => store.commit('increment'),

      //action
      asyncIncrement: () => store.dispatch('asyncIncrement')
    }
  }
}
```

## @Vue/runtime-core
defineComponent를 함수를 import 할 때 vue 모듈에서 가져올건지 runtime-core에서 가져올 건지 정할 수 있는데 뭐가 다른걸까 찾아봤다
- runtime-core은 커스텀 renderer를 만드는 모듈이었다
