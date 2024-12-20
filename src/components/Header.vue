<template>
  <!--header-------------------------------------------------------------------------------------------------------------------->
  <el-header>
        <el-row type="flex" justify="center" :gutter="20">
          <el-col :span="1">
            <div class="row-bg">
              <el-icon class="is-loading" :size="30" color="#409efc" @click="Main()">
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
              <el-button type="primary" plain circle class="LK" @click="Lk()">
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

</template>


<script lang="ts" setup>
import { ref } from 'vue'
  import { Sunny, Moon } from '@element-plus/icons-vue'
  const value2 = ref(false)
  const loading2 = ref(false)

import { useRouter } from 'vue-router';

  


const router = useRouter();

function Lk() {
  router.push({
    path: `/lk`  // Корректный путь
  });
}

function Main() {
  router.push({
    path: `/`  // Корректный путь
  });
}
  

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

<style scoped>
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
