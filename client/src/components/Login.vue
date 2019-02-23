<template>
    <div class="login">
      <div class="container">
        <div class="row">
          <div class="col-md-8 m-auto">
            <h1 class="display-4 text-center">登录</h1>
            <p class="lead text-center">使用已有的账户登录</p>
            <form @submit.prevent="submit" autocomplete="off" method="post">
              <div class="form-group">
                <input 
                  type="email" 
                  class="form-control form-control-lg" 
                  placeholder="邮箱地址" 
                  name="email"
                  v-model="user.email"
                />
              </div>
              <div class="form-group">
                <input 
                  type="password" 
                  class="form-control form-control-lg" 
                  placeholder="密码" 
                  name="password"
                  v-model="user.password"
                />
              </div>
              <input type="submit" class="btn btn-info-btn-block mt-4">
            </form>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  name: 'Login',
  data() {
      return {
        user: {
          email:"",
          password:""
        }
      };
  },
      methods: {
        submit() {
            console.log(this.user.name);
        }
      },
  };

</script>

<style scoped>

</style>

