<template>
    <form @submit.prevent="handleSubmit">
      <input v-model="formData.name" type="text" placeholder="Name">
      <input v-model="formData.email" type="email" placeholder="Email">
      <button type="submit">Submit</button>
    </form>
  </template>
   
  <script lang="ts">
  import { defineComponent, reactive } from 'vue';
  import axios from 'axios'; // 确保已安装axios
   
  interface FormData {
    name: string;
    email: string;
  }
   
  export default defineComponent({
    setup() {
      const formData = reactive<FormData>({
        name: '',
        email: '',
      });
   
      const handleSubmit = async () => {
        try {
          // 调用接口
          const response = await axios.post('your-api-endpoint', formData);
          console.log(response.data);
        } catch (error) {
          console.error(error);
        }
      };
   
      return {
        formData,
        handleSubmit,
      };
    },
  });
  </script>