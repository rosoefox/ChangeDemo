< E01 >  
변경 요약 : <script>와 export default {}를 <script setup> 으로 대체.  
            data() { return { message: ... } }를 import { ref } from 'vue';와 const message = ref("Vue!"); 로 대체.  
실행 화면 :
              
<img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/e9290590-2ced-4710-8b18-8af80046fcaa" />  

< E02 >  
변경 요약 : data() { return { ... }를 import { ref } 및 const name = ref(...)로 대체.  
mounted() { ... }를 import { onMounted } 및 onMounted(() => { ... })로 대체.  
computed: { fullName() { ... } }를	import { computed } 및 const fullName = computed(() => { ... })로 대체.  
실행 화면 : 2초 후의 화면입니다. 첫 화면은 Kyungsu Lee로 표기됩니다.

<img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/46e095bb-96f7-4ffa-98bd-b2e84f3210c9" />  
<E03>  
변경 요약 : data() { return { message: ... } }를 import { ref } 및 const message = ref(...)로 대체.  
실행 화면 : 검은 박스 안에 값을 입력하면 아래에 같은 값을 띄워줍니다.  
<img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/5a7dd526-af84-4922-a7ca-7473fce3b757" />

