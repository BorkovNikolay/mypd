<template>
    <el-scrollbar ref="scrollbarRef" height="100vh" always @scroll="scroll">
    <Header/>
    <div class="common-layout">
    <el-container>
      <el-container>
        <!--Боковая панель-->
        <el-aside width="200px">
            Aside
        </el-aside>
        <!--main------------->
        <el-main>
            Main
        </el-main>

      </el-container>
    </el-container>
  </div>
    <el-button type="primary" @click="Click()">Регистрация</el-button>
</el-scrollbar>
</template>
   
   
   
<script lang="ts" setup>
    import { useRouter } from 'vue-router';
    import Header from "@/components/Header.vue";
     
    import { ref } from 'vue'
  
    import { ElScrollbar } from 'element-plus'


    const value = ref(0)


    const scroll = ({ scrollTop }) => {
    value.value = scrollTop
    }
   
   
    const router = useRouter();
   
    function Click() {
    router.push({
       path: `/`  // Корректный путь
    });
   }
     
   
</script>
   
   
<style scoped>
   /*h1{
     font-size: 50px;
   }
   
   .el-row {
     margin-top: 20px;
     margin-bottom: 20px;
   }
   
   .img-col{
     margin-top: 10px;
     margin-bottom: 10px;
   }
   
   #stages{
     text-align: center;
   }
   
    
   .img{
     width: 100%;
   }
   
   .stages-bg{
     width: 100%;
     height: 100%;
     background: #3980FF;  
     border-radius: 20px;
   }
   
   .main-bg{
     width: 100%;
     height: 100%;
     background: #3980FF;
     background-image: url("../assets/img/bg.png") ; 
     background-repeat: no-repeat; 
     border-radius: 20px;
   }*/
</style>