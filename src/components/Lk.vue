<template>
  <el-scrollbar ref="scrollbarRef" height="100vh" always @scroll="scroll">
  <Header/>

  <div class="common-layout">
  <el-container>


    <el-aside width="auto">
      <div class="stages-bg">
      <el-avatar :size="100"
        src="https://avatars.mds.yandex.net/i?id=a58aa42c311bff2d24a063699f0a546bfc2db3996a074653-12471101-images-thumbs&n=13"
      />
      <el-divider border-style="double" />
      <h1>ФИО</h1>
      <el-divider border-style="double" />
      <h1>Учебное заведение</h1>
      <el-divider border-style="double" />
      <h1>номер телефона</h1>
      <el-divider border-style="double" />
      <h1>Почта</h1>
      <el-divider border-style="double" />
      <div>
        <el-button type="primary" plain round >Редактировать</el-button>
      </div>
      </div>
      </el-aside>


      <el-main>
        <h1>Команда</h1>
        <el-timeline >
          <el-timeline-item
          v-for="(activity, index) in activities"
          :key="index"
          :timestamp="activity.name"
          >
            {{ activity.Role }}
          </el-timeline-item>
        </el-timeline>
      </el-main>


      <el-aside width="20%">
        <el-countdown format="DD [days] HH:mm:ss" :value="value2">
          <template #title>
            <div style="display: inline-flex; align-items: center">
              <el-icon style="margin-right: 4px" :size="12">
                <Calendar />
              </el-icon>
              Still to go until next month
            </div>
          </template>
        </el-countdown>
        <div class="countdown-footer">{{ value2.format('YYYY-MM-DD') }}</div>
      </el-aside>
    </el-container>
  
  
  </div>
</el-scrollbar>
</template>
   
   
   
<script lang="ts" setup>
    import Header from "@/components/Header.vue";  
    import { ref } from 'vue'
    import { ElScrollbar } from 'element-plus'
    import dayjs from 'dayjs'
    import { Calendar } from '@element-plus/icons-vue'

  
    const value2 = ref(dayjs().add(1, 'month').startOf('month'))

    

    const valueS = ref(0)


    const scroll = ({ scrollTop }) => {
    valueS.value = scrollTop
    }

    const activities = [
  {
    Role: 'Team leader',
    name: 'Name',
  },
  {
    Role: 'Participant',
    name: 'Name',
  },
  {
    Role: 'Participant',
    name: 'Name',
  },
  {
    Role: 'Participant',
    name: 'Name',
  },
  {
    Role: 'Participant',
    name: 'Name',
  },
  {
    Role: 'Participant',
    name: 'Name',
  },
]
    
   
   

   
</script>
   
   
<style scoped>

.stages-bg{
  border: 5px, solid, #3980FF;
  background: #5b97ff;  
  border-radius: 20px;
  text-align: center;
}

.el-avatar{
  margin: 10px;
}

h1{
    font-size: 30px;
    margin: 10px;
  }

.el-button{
  margin-bottom: 10px;
}

.team{
  width: auto;
}

.el-timeline-item{
  font-size: 20px;
}



</style>