< E01 >  
변경 요약 : <script>와 export default {}를 <script setup> 으로 대체.  
            data() { return { message: ... } }를 import { ref } from 'vue';와 const message = ref("Vue!"); 로 대체.  
실행 화면 : "Hello, Vue!" 문자열이 나타난다.
              
<img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/e9290590-2ced-4710-8b18-8af80046fcaa" />  

< E02 >  
변경 요약 : data() { return { ... }를 import { ref } 및 const name = ref(...)로 대체.  
mounted() { ... }를 import { onMounted } 및 onMounted(() => { ... })로 대체.  
computed: { fullName() { ... } }를	import { computed } 및 const fullName = computed(() => { ... })로 대체.  
실행 화면 : 2초 후의 화면입니다. 첫 화면은 Kyungsu Lee로 표기됩니다.

<img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/46e095bb-96f7-4ffa-98bd-b2e84f3210c9" />  

< E03 >  
변경 요약 : data() { return { message: ... } }를 import { ref } 및 const message = ref(...)로 대체.  
실행 화면 : 검은 박스 안에 값을 입력하면 아래에 같은 값을 띄워줍니다.  
<img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/5a7dd526-af84-4922-a7ca-7473fce3b757" />  

< E04 >  
변경 요약 :  isVisible: true를 const isVisible = ref(true); 대체.  
items: [...]를 const items = ref([...]);로 대체.  
count: 0를 const count = ref(0);로 대체.  
실행 화면 :  Toggle Visibility 버튼을 누르면 위의 3 문장이 사라집니다. 다시 누르면 보여집니다.  
Increment Count 버튼을 누르면 값이 1씩 증가합니다. if문에 따라 아래의 문장이 달라집니다.
<img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/f7778085-3547-404a-beba-555215449682" />  

< E05 >  
변경 요약 :  data() { return { ... } }를 import { ref } 및 const name = ref(...)로 대체.  
methods: { handleEvent() { ... } }를 const handleEvent = (payload) => { ... }로 대체.  
components: { ChildComponent }를 제거.(script setup 사용)  
props: ['message']를 const props = defineProps({ message: String })로 대체.  
@click="$emit('custom-event', ...)를  const emit = defineEmits(['custom-event']) 후 @click="emit('custom-event', ...)로 대체.  
실행 화면 :  Hello from parent를 누르면 "Hello from parent" 문자열을 부모에게 보내고, 콘솔에 문자열이 출력됩니다.
<img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/cd4c3d6e-a13b-4ca1-8f73-df888ab1df0e" />  

< E06 >  
변경 요약 :  inject: ['sharedMessage']를 import { inject } from 'vue'; 와 const sharedMessage = inject('sharedMessage');로 대체.  
provide() { return { sharedMessage: ... } }를 import { provide, ref } 및 provide('sharedMessage', ref(...))로 대체.  
components: { ChildComponent1 }를 제거.(script setup 사용)  
실행 화면 :  child1 아래에 빨간색의 Hello from providea 문자열이 나타나고, child2 아래에 검은색의 Hello from provide 문자열이 나타난다.
<img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/96a717ff-834c-4aaa-a6f5-a864aabad7d2" />  
  
< E07 >  
변경 요약 : name: '...'	제거.  
props: { ... }를 const props = defineProps({ ... })로 대체.  
data() { return { ... } }를 const var = ref(값)로 대체.  
computed: { fn() { ... } }를 const var = computed(() => { ... })로 대체.  
methods: { fn() { ... } }를 const fn = () => { ... }로 대체.  
watch: { ... }를 watch(변수, (new, old) => { ... })로 대체.  
created, mounted, updated.. 등을 on이 붙은 함수로 대체.  
실행 화면 :  이름과 성을 입력하고 Greet을 누르면 Greeting count가 올라가고, 3회부터는 아래의 문자열이 변경된다.
<img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/36d74c95-b347-4218-a342-8d8ac16f269f" />  

< E08 >  
변경 요약 : vue3 스타일이지만, E07과 E09 사이의 문법이다. E09에서 E08과의 차이점을 설명하겠다.  
실행 화면 : E07과 동일하다.  
<img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/4889f461-30c0-4a98-9924-b12f47a3a39b" />  

< E09 >  
변경 요약 : vue3 스타일이지만, E08과 다른 점이 있다.  
setup 옵션을 포함한 Options API 구조가 아닌 <script setup> 구조를 사용하였다.  
export default { name: '...', setup() { ... } }를 defineOptions({ name: '...' })로 대체한 상태이다.  
실행 화면 : E07, E08과 동일하다.  
<img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/4df74de6-9a19-4129-ba0f-a517f9a4f69d" />

< E10 >  
변경 요약 : export default { setup() { return { ... } } }를 <script setup>로 대체.    
name: 'E10Ref'를 defineOptions({ name: 'E10Ref' })로 대체.  
실행 화면 : Increment 버튼을 누르면 count가 1씩 증가한다.  
<img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/23a23d4e-273d-4aff-9524-b324e347ed49" />
