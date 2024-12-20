<template>
<Header/>
   

  <div class="wrapper">
    <el-main class="main-container">
      <h1>Регистрация</h1>
      <el-form :model="form" ref="form" @submit.prevent="register">
        <el-form-item
          label="Логин:"
          prop="login"
          :rules="[{ required: true, message: 'Пожалуйста, введите логин.', trigger: 'blur' }]"
        >
          <el-input v-model="form.login"></el-input>
        </el-form-item>
        <el-form-item
          label="Емайл:"
          prop="email"
          :rules="[
            {
              type: 'email',
              required: true,
              message: 'Пожалуйста, введите правильный емайл.',
              trigger: 'blur',
            },
          ]"
        >
          <el-input v-model="form.email"></el-input>
        </el-form-item>
        <el-form-item
          label="Пароль:"
          prop="password"
          :rules="[{ required: true, message: 'Пожалуйста, введите пароль.', trigger: 'blur' }]"
        >
          <el-input type="password" v-model="form.password"></el-input>
        </el-form-item>
        <el-form-item
          label="Подтвердите пароль:"
          prop="confirm_password"
          :rules="[
            { required: true, message: 'Пожалуйста, подтвердите пароль.', trigger: 'blur' },
            { validator: confirmPassword, trigger: 'blur' },
          ]"
        >
          <el-input type="password" v-model="form.confirm_password"></el-input>
        </el-form-item>
        <el-form-item class="upload-files" label="Прикрепить файлы:">
          <el-upload v-model:file-list="fileList" :before-upload="handleBeforeUpload">
            <el-button type="button">Выбрать файл</el-button>
          </el-upload>
        </el-form-item>
        <div class="link-container">
          <el-link type="primary">Скачать документ для заполнения</el-link>
        </div>
        <div class="button-container">
          <el-button class="button-register" type="primary" @click="register"
            >Зарегистрироваться</el-button
          >
          <el-button class="button-move-to-login" type="button" @click="move_to_login"
            >Войти в существующий аккаунт</el-button
          >
        </div>
      </el-form>
    </el-main>
  </div>
</template>

<script >
    import { useRouter } from 'vue-router';
    import Header from "@/components/Header.vue";
    const router = useRouter();
    export default {
  data() {
    return {
      form: {
        login: '',
        email: '',
        password: '',
        confirm_password: '',
      },
      fileList: [],
    }
  },
  methods: {
    register() {
      this.$refs.form.validate((valid) => {
        if (valid) {
          console.log('Form is valid:', this.form) // если всё заполнено то работай
        } else {
          console.error('Form validation failed')
          alert('Заполните недостающие поля!')
        }
      })
    },
    move_to_login() {
      this.$router.push({ name: 'LoginPage' });
    },
    confirmPassword(rule, value, callback) {
      if (value !== this.form.password) {
        callback(new Error('Пароли не совпадают.'))
      } else {
        callback()
      }
    },
    handleBeforeUpload(file) {
      if (file.size > 1000000) {
        this.$message.error('Файл слишком большой')
        return false
      }
      return true
    },
  },
}
</script>

<style scoped>
html,
body {
  height: 100%;
  background-color: white;
}

.wrapper {
  display: flex;
  height: 100vh;
  justify-content: center;
  align-items: center;
}

.main-container {
  background-color: white;
  box-shadow: 5px 5px 20px black;
  max-width: 500px;
  margin: 0 auto;
  padding: 20px;
  text-align: center;
}

.button-container {
  display: flex;
  justify-content: space-between;
}

.upload-files {
  margin-bottom: 0;
}

.link-container {
  padding: 0px 15px 15px 15px;
  vertical-align: middle;
}
</style>