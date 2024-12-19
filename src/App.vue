<template>
  <div class="common-layout">
    <el-container>

      <!--header-------------------------------------------------------------------------------------------------------------------->
      <el-header>
        <el-row type="flex" justify="center" :gutter="20">
          <el-col :span="1">
            <div class="row-bg">
              <el-icon class="is-loading" :size="30" color="#409efc">
                <Loading />
              </el-icon>
            </div>
          </el-col>
          <h3 class="logo">So So Logo</h3> 
          <h3 class="number">8 (***) ***-**-**</h3> 
          <p class="mail">Help@mail.ru</p>
          <el-switch
            v-model="value2"
            class="ml-2"
            size="large"
            :loading="loading2"
            :before-change="beforeChange2"
            style="--el-switch-on-color: #a0cfff; --el-switch-off-color: #373737"
            :active-action-icon="Sunny"
            :inactive-action-icon="Moon"
          />
          <el-col :xs="1" :sm="3" :md="5" :lg="6"  >
            <div class="row-bg">
              <el-button type="primary" plain round><el-icon><Promotion /></el-icon></el-button>
              <el-button type="primary" plain round>Registration</el-button>
              <el-button type="primary" plain round>Join</el-button>
              <el-button type="primary" plain circle class="LK">
                <el-avatar :size="25"
                  src="https://avatars.mds.yandex.net/i?id=a58aa42c311bff2d24a063699f0a546bfc2db3996a074653-12471101-images-thumbs&n=13"
                />
              </el-button>
            </div>
          </el-col>
        </el-row>
      </el-header>
      <!--src="https://cube.elemecdn.com/0/88/03b0d39583f48206768a7534e55bcpng.png"-->
      <!--end-header-------------------------------------------------------------------------------------------------------------------->

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
              <img src="./assets/img/hack1.png" alt="" class="img">
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

      <!--footer-------------------------------------------------------------------------------------------------------------------->
      <el-footer>
        
      </el-footer>
      <!--end-footer-------------------------------------------------------------------------------------------------------------------->

    </el-container>
  </div>
</template>


<script lang="ts" setup>
  import { ref } from 'vue'
  import { Sunny, Moon } from '@element-plus/icons-vue'
  
   

  const value2 = ref(false)
  const loading2 = ref(false)

const beforeChange2 = () => {
  loading2.value = true
  return new Promise((resolve) => {
    setTimeout(() => {
      loading2.value = false
      return resolve(true)
    }, 1000)
  })
}

</script>

<style>

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

.LK{
  padding: 10px;
}

/*.el-avater{
  margin: 10px;
}*/

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
  background-image: url("./assets/img/bg.png") ;  
  border-radius: 20px;
}
.logo{
  margin: 0px 15px;
}
.number{
  margin: 0px 15px;
}

.mail{
  margin: 0px 15px;
}
</style>
