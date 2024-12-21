<template>
  
<el-scrollbar ref="scrollbarRef" height="100vh" always @scroll="scroll">
 
  <Header/>
 
 
 <!--main-------------------------------------------------------------------------------------------------------------------->
 <el-main>
        
        <!--декаративный-блок-с-информацией-------------------------------------------------------------------------------------------------------------------->
        <el-row type="flex" justify="center" class="main-bg">
          <el-col  :span="10" class="img-col">
            <h1>Хакатон</h1>
            <div>
              <el-icon><Position /></el-icon>
              <span> инфо ================================ ================================</span>
            </div>
            <div>
              <el-icon><Finished /></el-icon>
              <span> инфо ================================ ================================</span>
            </div>
            <el-button type="primary" plain >Support</el-button>
          </el-col>
          <el-col  :span="10" class="img-col">
              <img src="../assets/img/hack1.png" alt="" class="img">
          </el-col>
        </el-row>
        <!--конец-------------------------------------------------------------------------------------------------------------------->  
        
        <!--текстовая-информация------------------------------------------------------------------------------------------------------------------->
        <el-row type="flex" justify="center" >
          <el-col  :span="22" >
            <h1>инфо</h1>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec auctor mauris vitae consequat tincidunt. Donec congue turpis pharetra, rutrum sapien id, porttitor quam. Praesent eu dui convallis libero pharetra interdum. Sed fringilla risus non metus fringilla, sit amet cursus orci molestie. Maecenas tristique molestie eros. Morbi nibh mauris, malesuada sit amet efficitur nec, lobortis at lectus. Vivamus vitae maximus urna, quis mollis lacus. Integer tellus felis, semper ac congue ut, volutpat non ligula. Aliquam nisl odio, placerat sed ex sed, tincidunt eleifend quam. Vestibulum consectetur interdum blandit. Duis et ornare elit, in venenatis purus.

            Suspendisse fermentum nisl efficitur sem gravida ultrices. Donec sit amet tempus lectus. Phasellus lacinia nibh gravida dictum dignissim. Nullam auctor urna ligula, a sodales risus bibendum eu. Donec commodo a libero nec ullamcorper. Sed eleifend, nunc quis gravida tempor, odio magna tincidunt est, euismod luctus elit neque dictum nisi. Vestibulum pellentesque nisl quis nulla sodales, et condimentum dui ornare. Donec in odio mi. Donec ut augue auctor, fringilla ipsum et, eleifend ipsum. Ut turpis elit, porta vel ex vulputate, pharetra viverra ligula. Aenean vel hendrerit diam. Proin ornare sagittis sagittis. Proin nibh nibh, lacinia a placerat elementum, feugiat vel tellus. Vestibulum eleifend, tellus nec convallis vulputate, augue ligula pulvinar tellus, non scelerisque neque arcu ac arcu. Ut consectetur vitae eros vel venenatis.
          </el-col>
        </el-row>
        <!--конец-------------------------------------------------------------------------------------------------------------------->

        <!--Этапы-------------------------------------------------------------------------------------------------------------------->
        <el-row type="flex" justify="center" class="stages-bg">
          <el-col  :span="24" class="img-col" id="stages">
            <h1>Этапы</h1>
          </el-col>
          <el-col  :span="4" :offset="1" class="img-col">
            <div>
              <el-icon :size="100"><Monitor /></el-icon>
            </div>
            <el-button type="primary" circle disabled>1</el-button>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis vulputate sit amet elit quis consectetur. Fusce sagittis velit mauris. Praesent eu nisl ut nisi mollis. 
          </el-col>
          <el-col  :span="4" :offset="1" class="img-col">
            <div>
              <el-icon :size="100"><Monitor /></el-icon>
            </div>
            <el-button type="primary" circle disabled>2</el-button>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis vulputate sit amet elit quis consectetur. Fusce sagittis velit mauris. Praesent eu nisl ut nisi mollis.
          </el-col>
          <el-col  :span="4" :offset="1" class="img-col">
            <div>
              <el-icon :size="100"><Monitor /></el-icon>
            </div>
            <el-button type="primary" circle disabled>3</el-button>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis vulputate sit amet elit quis consectetur. Fusce sagittis velit mauris. Praesent eu nisl ut nisi mollis.
          </el-col>
          <el-col  :span="4" :offset="1" class="img-col">
            <div>
              <el-icon :size="100"><Monitor /></el-icon>
            </div>
            <el-button type="primary" circle disabled>4</el-button>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis vulputate sit amet elit quis consectetur. Fusce sagittis velit mauris. Praesent eu nisl ut nisi mollis.
          </el-col>
          <el-col  :span="4" :offset="1" class="img-col">
            <div>
              <el-icon :size="100"><Monitor /></el-icon>
            </div>
            <el-button type="primary" circle disabled>5</el-button>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis vulputate sit amet elit quis consectetur. Fusce sagittis velit mauris. Praesent eu nisl ut nisi mollis.
          </el-col>
          <el-col  :span="4" :offset="1" class="img-col">
            <div>
              <el-icon :size="100"><Monitor /></el-icon>
            </div>
            <el-button type="primary" circle disabled>6</el-button>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis vulputate sit amet elit quis consectetur. Fusce sagittis velit mauris. Praesent eu nisl ut nisi mollis.
          </el-col>
          <el-col  :span="4" :offset="1" class="img-col">
            <div>
              <el-icon :size="100"><Monitor /></el-icon>
            </div>
            <el-button type="primary" circle disabled>7</el-button>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis vulputate sit amet elit quis consectetur. Fusce sagittis velit mauris. Praesent eu nisl ut nisi mollis.
          </el-col>
        </el-row>
        <!--конец-------------------------------------------------------------------------------------------------------------------->

      </el-main>
      <!--end-main-------------------------------------------------------------------------------------------------------------------->
      
    
  </el-scrollbar>

</template>



<script lang="ts" setup>
  import { ref } from 'vue'
  import { ElScrollbar } from 'element-plus'
  import Header from "@/components/Header.vue";
  


  const value = ref(0)


  const scroll = ({ scrollTop }) => {
  value.value = scrollTop
  }
</script>


<style scoped>
h1{
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
}
</style>